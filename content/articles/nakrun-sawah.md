---
title: "MVP: NakRun - Running Event Web Application"
description: "I built a production-level MVP for a running event in just 2 weeks of development. A lot of challenges, problem solving and learning experience I have been through in this project."
published: 2025/12/30
slug: "nakrun-sawah-2025"
---

---

![NakRun Group](/articles/nakrun-group.jpeg)

# Solving Event Hustle in Just 2 Weeks

Last November, I had the chance to help a running event team build a web application to support their event operations. Nothing overly complex, but something practical that actually made their workload easier on event day.

Like most event teams, they were already using external platforms for registrations and orders. The problem wasn’t the tools themselves, it was everything around them. Data was scattered, tracking was manual, and merch collection day was always the most stressful part as they need to keep everything in control.

So the idea was straightforward: **centralize everything and make the process smoother for both the team and the runners**.

> I want the participants to come during collection day, show their QR code to the counter, collection team will scan and verified their details and merch. Then done! Hustle free, fast and precise.

From idea to deployment, the whole thing was completed in **just two weeks**.

The key was not over-engineering:

* **Focus on what actually mattered for the event**
* **Keep flows simple**
* **Ship something reliable instead of something fancy**

---

# What Is The Problem?

Before the system existed, a lot of things were done manually or across different platforms:

* Participant and order data lived elsewhere
* Staff had to manually verify orders during merch collection
* Data is not centralized, leading to confusion and data errors
* Long queues formed easily when things got busy
* It was hard for the management team to see real-time progress

One of the challenges is I had to restructure the data from the external platforms into a well-structured database. Some issues such as phone number no formatted correctly, name is not validated and not stored properly, data column misleading, etc.

When you’re dealing with hundreds (or thousands) of runners, even small delays quickly turn into chaos.

![NakRun Group](/articles/nakrun-meeting.jpeg)

---

# The Solution

Instead of reinventing the whole event flow, we focused on the most critical parts.

The system was built to:

* Pull in data from external platforms
* Let the team manage users, orders, and events in one place
* Simplify merchandise collection using QR codes

The merch collection flow was intentionally kept as simple as possible:

1. Runners receive a confirmation email after submitting their event registration
2. The email includes a unique QR code
3. On collection day, they show the QR code at the counter
4. The admin scans it, the system verifies the order
5. Merch is collected and marked as done

No paper lists. No manual searching. No guessing.

---

# Why This Worked Well

This approach solved a lot of small but painful problems:

* Collection became faster and more predictable
* Duplicate or invalid claims were avoided
* The team could see live collection stats
* Management finally had a clear overview of what was happening

Most importantly, the system reduced stress on event day — which is honestly the biggest win.

---

# Tech Stack (Keeping It Practical)

The stack was intentionally simple and familiar, so development could move fast:

* **Laravel** for the backend engine
* **Vue.js** my go to preference in web application
* **Mailtrap** for email blasting in production
* **Laravel Nightwatch** for system monitoring
* **DigitalOcean** to host the application & for deployment

Laravel handled the data, business logic, and QR verification, while Vue kept the admin side responsive and easy to use. DigitalOcean was more than enough to keep things stable during the event.

![Mailtrap](/articles/nakrun-mailtrap.jpeg)
_This is example where I monitor the email delivery using Mailtrap in production._

> I learned a lot in terms of preparing for mail sending in production, the required configuration, especially the limitations on how to work around the limitation until everything works. The behaviour in real-world traffic is totally different from development & testing experience.

___
## **Security Use Case**
![Nightwatch](/articles/nakrun-nightwatch.png)
_Im using Laravel Nightwatch to monitor the traffic in the web application._
![Security Issue](/articles/nakrun-security.jpeg)
_In this exact example, it shows the HTTP requests where there are attempts to scan my web application using method we call **fuzzing** or **directory brutforce**. So to mitigate this attempt, I manually block the source IP Address as I didn't set any WAF_

---

## **Final Thoughts**

This project was a good reminder that you don’t always need complex systems to make a big impact. Sometimes, a small, well-thought-out tool can completely change how a team operates on the ground.

Seeing the system being used smoothly on event day made the tight timeline totally worth it.

![NakRun participant](/articles/nakrun-participant.jpeg)

---
## **Project Snapshot**

<div style="display: flex; gap: 12px; overflow-x: auto;">
    <img src="/articles/nakrun-demo1.jpeg" width="200" />
    <img src="/articles/nakrun-demo2.jpeg" width="200" />
    <img src="/articles/nakrun-demo3.jpeg" width="200" />
    <img src="/articles/nakrun-demo4.jpeg" width="200" />
</div>
---

