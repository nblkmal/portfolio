---
title: "Your Own Free Personal Cloud LLM: A Step-by-Step Guide"
description: "Deploy Ollama on AWS EC2 using Docker Compose with a LiteLLM proxy for a private inference endpoint."
published: 2026/03/15
slug: "personal-cloud-llm"
---

---

# Your Own Free Personal Cloud LLM

![Logos](/articles/personal-llm.png)

Running your own **cloud-hosted Ollama server** gives you a private inference endpoint that you can use across your development tools — Laravel apps, CLI tools, editors, or automation workflows — without relying on third-party APIs.

In this guide, we will deploy **Ollama on AWS EC2 using Docker Compose with a LiteLLM proxy**, allowing us to:

* Use **AWS promotional credits (e.g. $200 free credits)** for GPU inference
* Expose a **standard OpenAI-compatible API**
* Add a **proxy layer for better security and control**
* Maintain a **reproducible infrastructure setup**
* Use the same setup in **cloud and local development**

The result is a **personal AI inference server in the cloud**.

---

# Architecture Overview

Instead of exposing Ollama directly, we place **LiteLLM as a proxy layer**.

```text
                 Local Machine
                        │
                        │
        ┌───────────────▼───────────────┐
        │        LiteLLM Gateway        │
        │   (OpenAI + Anthropic APIs)   │
        └───────────────┬───────────────┘
                        │
        ┌───────────────┼───────────────┐
        │                               │
   Ollama Models                    Redis Cache
        │                               │
        ▼                               ▼
   llama3 / qwen2 / etc           Response caching
```

Benefits of using a proxy layer:

* Do **not expose Ollama directly**
* Provide **OpenAI-compatible API**
* Add **API keys and authentication**
* Add **rate limiting / logging**
* Enable **future model routing**

External access:

```text
http://<EC2_PUBLIC_IP>:4000/v1/chat/completions
```

---

# Prerequisites

Before starting, ensure you have:

* An AWS account with **promotional credits**
* Basic knowledge of **SSH**
* Docker and Docker Compose familiarity

Optional:

* AWS CLI
* SSH key pair configured

---

# Step 1 — Launch an EC2 Instance

Navigate to **AWS Console → EC2 → Launch Instance**.

Recommended configuration.

### AMI

```
Ubuntu Server 22.04 LTS
```

### Instance Type

GPU instances work best for inference.

Recommended:

| Instance    | GPU       | VRAM | Notes        |
| ----------- | --------- | ---- | ------------ |
| g4dn.xlarge | NVIDIA T4 | 16GB | Good balance |

This instance supports most **7B models** comfortably.

### Important Note: AWS vCPU Quota for GPU Instances

New AWS accounts often have a **default vCPU quota of 0 for GPU instance families**.  
If you attempt to launch a GPU instance such as `g4dn.xlarge`, you may see an error like:


This means your account is **not yet allowed to run GPU instances**.

To resolve this, request a quota increase.

#### Steps

1. Open **AWS Console → Service Quotas**
2. Search for: Running On-Demand G and VT instances
3. Click **Request quota increase**
4. Set the value to **at least 4 vCPUs** (required for `g4dn.xlarge`)

Approval usually takes **a few minutes to several hours** depending on your account.

Once approved, you can proceed to launch the GPU instance normally.


### Storage

```
100GB gp3
```

LLM models can take several gigabytes.

---

# Step 2 — Configure Security Group

Allow inbound access:

| Port | Purpose     |
| ---- | ----------- |
| 22   | SSH         |

For better security:
Create an SSH Tunnel

From your laptop:

```
ssh -i your-key.pem \
-L 4000:localhost:4000 \
ubuntu@<EC2_PUBLIC_IP>
```

Now your local machine exposes:

```
http://localhost:4000
```

which securely forwards to the EC2 LiteLLM service. In this setup I personally keep it simple and did'nt configure any API Key since it is not shared by anyone, just me.

---

# Step 3 — Connect to the Server

SSH into the server.

```bash
ssh ubuntu@<EC2_PUBLIC_IP>
```

Update packages.

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Step 4 — Check or Install NVIDIA Drivers (GPU Only)

If you use GPU instances:

```bash
sudo apt install -y nvidia-driver-535
```

Reboot:

```bash
sudo reboot
```

Verify:

```bash
nvidia-smi
```

---

# Step 5 — Install Docker

Install Docker and Docker Compose.

```bash
sudo apt install -y docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker
```

Allow current user to use Docker:

```bash
sudo usermod -aG docker $USER
```

Reconnect to SSH afterward.

---

# Step 6 — Install NVIDIA Container Toolkit

Allow Docker containers to access GPU.

```bash
distribution=$(. /etc/os-release;echo $ID$VERSION_ID)

curl -s -L https://nvidia.github.io/libnvidia-container/gpgkey | sudo apt-key add -

curl -s -L https://nvidia.github.io/libnvidia-container/$distribution/libnvidia-container.list \
| sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list

sudo apt update
sudo apt install -y nvidia-container-toolkit
```

Restart Docker.

```bash
sudo systemctl restart docker
```

---

# Step 7 — Create Project Directory

```bash
mkdir cloud-ollama
cd cloud-ollama
```

---

# Step 8 — Create LiteLLM Configuration

Create a configuration file.

```
litellm-config.yaml
```

Example configuration:

```yaml
model_list:
  - model_name: llama3
    litellm_params:
      model: ollama/llama3
      api_base: http://ollama:11434
```

This tells LiteLLM to forward requests to the **internal Ollama service**.

---

# Step 9 — Create Docker Compose Configuration

Create:

```
docker-compose.yml
```

Example configuration:

```yaml
version: "3.9"

services:

  ollama:
    image: ollama/ollama
    container_name: ollama
    restart: unless-stopped
    volumes:
      - ollama-data:/root/.ollama
    networks:
      - ai
    deploy:
      resources:
        reservations:
          devices:
            - capabilities: [gpu]

  redis:
    image: redis:7
    container_name: redis
    restart: unless-stopped
    networks:
      - ai

  litellm:
    image: ghcr.io/berriai/litellm:main
    container_name: litellm
    volumes:
      - ./litellm-config.yaml:/app/config.yaml
    command: --config /app/config.yaml --port 4000
    depends_on:
      - ollama
      - redis
    networks:
      - ai

volumes:
  ollama-data:

networks:
  ai:
```

Key points:

* Ollama runs **inside an internal Docker network**
* LiteLLM acts as the **public API gateway**
* Only **port 4000** is exposed externally

This architecture improves security and flexibility.

---

# Step 10 — Start the Stack

Run:

```bash
docker compose up -d
```

Verify:

```bash
docker ps
```

Expected containers:

```
ollama
litellm
redis
```

---

# Step 11 — Download a Model

Pull the model inside the Ollama container.

Example:

```bash
docker exec -it ollama ollama pull llama3
```

Other useful models:

| Model          | Use               |
| -------------- | ----------------- |
| llama3         | general assistant |
| deepseek-coder | coding            |
| qwen2.5        | reasoning         |

---

# Step 12 — Validate the Deployment

We will test the **OpenAI-compatible endpoint exposed by LiteLLM**.

### Simple CURL Test

Run from your **local machine**.

```bash
curl http://<EC2_PUBLIC_IP>:4000/v1/chat/completions \
-H "Content-Type: application/json" \
-d '{
"model": "llama3",for
"messages": [
  {"role": "user", "content": "Explain Laravel service container"}
]
}'
```

If everything is working correctly, the API will return a response generated by the model.

---

# Optional: Secure Access with SSH Tunnel

Instead of exposing the API publicly, create an SSH tunnel.

```bash
ssh -L 4000:localhost:4000 ubuntu@<EC2_IP>
```

Then access:

```
http://localhost:4000
```

This avoids exposing the API to the internet.

---

# Managing AWS Credit Usage

GPU instances can consume credits quickly.

Typical pricing example:

```
g4dn.xlarge ≈ $0.52/hour
```

With **$200 promotional credits**:

```
$200 / 0.52 ≈ 380 hours
```

To save cost:

```
Start instance → develop → stop instance
```

Stopping the instance prevents compute charges.

---

# Final Thoughts

Running your own **Cloud Ollama** gives you:

* Full control over AI models
* A reusable AI backend for multiple projects
* OpenAI-compatible API endpoints
* Reduced dependency on external AI providers

With AWS promotional credits, you can experiment with running your own **AI inference infrastructure** at minimal cost.

Your EC2 instance effectively becomes **your own personal AI platform** for development, experimentation, and automation.
