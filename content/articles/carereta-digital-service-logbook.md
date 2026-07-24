---
title: "SaaS: CareReta - Digital Service Book for Malaysian Drivers"
description: "I built and launched CareReta, a digital car service logbook SaaS for Malaysian drivers — solo, part-time, and validated before every line of code. Here's the story, the stack, and the lessons."
published: 2026/07/24
slug: "carereta-digital-service-logbook"
---

---

![CareReta Landing Page](/articles/carereta-hero.png)

# Care + Kereta = CareReta

Every Malaysian driver knows this moment: you're at the workshop, the mechanic says "Boss, this part kena tukar dah" — and you genuinely cannot remember whether you replaced it last month or three years ago. The physical service book? Somewhere in the glove compartment, faded, or lost when you changed cars.

That frustration became [CareReta](https://carereta.my/) — a digital car service logbook built for Malaysian car owners, families, and kereta sewa operators. The name says it all: Care + Kereta.

Unlike my previous MVP sprints, this one is a full SaaS product — live, in beta, with 70+ registered users and 58+ cars on the platform. And I built it solo, working 2–3 hours a day around everything else in life.

The core principle that made that possible:

* **Validate before building** — manual trials before code, go/no-go criteria before every phase
* **Ship in thin slices** — every feature broken into phases with explicit out-of-scope lists
* **Only claim what's confirmed true** — the anti-scam positioning demands it

---

# What Is The Problem?

Malaysia has one of the highest car ownership rates in Asia, and Proton/Perodua dominate the roads — yet both still rely on manual physical service books. The reality for most owners:

* Service receipts pile up in the glove compartment until they fade or disappear
* Nobody remembers the last oil change date or mileage — it's all guesswork
* When selling the car, there's no proof of maintenance history — buyers just have to trust you
* Worst of all: workshop upselling. Without records, you can't push back when someone tells you a part "needs replacing" — even if you replaced it recently

Then there's the kereta sewa (car rental) side. Small operators running 5–15 cars manage their entire business through WhatsApp messages and paper notebooks — no service tracking per car, no pre/post rental photo evidence, no idea which car is profitable and which is a money pit.

Two very different users, one shared root cause: no structured record of what happened to the car.

---

# The Solution

CareReta is a mobile-first web app that replaces the physical service book:

1. **Add your car** — plate and model, and the service schedule is pre-filled for Proton/Perodua
2. **Log a service** — snap the workshop receipt and let OCR read it, or type it manually in seconds
3. **Get reminded** — CareReta calculates by distance and time, so reminders arrive not too early, not too late

![Know Your Car feature](/articles/carereta-know-your-car.png)
_"Know Your Car" breaks every part down into plain language — what it does, common issues, and how much it typically costs to service._

The features that make it more than a note-taking app:

* **Duplicate part alert** — if a workshop wants to replace something you just replaced, CareReta flags it. This is the anti-scam heart of the product.
* **Next service predictor** — based on your mileage pattern and a seeded parts catalogue (sourced from official Proton/Perodua service booklets only)
* **Beginner guide** — every part comes with a plain-language explanation of what it does and why it matters
* **Rental layer** — booking management, renter profiles, and pre/post rental photo logs for kereta sewa operators

![CareReta records and dashboard](/articles/carereta-records.png)

The brand positioning is deliberate: pro-transparency, anti-scam. That means no scraped data, no unverified claims, no shortcuts that would undermine the very trust the product is selling.

---

# Why This Approach Worked

The biggest risk for a solo founder isn't bad code — it's building the wrong thing. So every feature goes through the same gate:

* **Manual trial first, code second.** Before building the workshop collaboration flow, I tested it manually with real workshops — zero code written until the behaviour was proven.
* **Kill/continue thresholds written before data arrives.** It's too easy to rationalize weak signals after the fact. Writing the criteria down first keeps me honest.
* **True activation is the first service record logged** — not signup. Vanity metrics don't pay bills.

This discipline is why the product shipped at all on a part-time schedule. Every hour had to count.

---

# Tech Stack (Keeping It Practical)

Familiar tools, boring choices, fast shipping:

* **Laravel 13** — backend engine, multi-tenancy via native Teams
* **Vue 3 + TypeScript + Inertia.js** — SPA feel without maintaining a separate API
* **Tailwind CSS 4 + shadcn-vue** — mobile-first UI, usable at 375px
* **MySQL 8** — UUID keys everywhere, soft deletes on anything a user would cry about losing
* **AWS EC2 with Docker + Caddy** — the app itself
* **Vercel** — the marketing site, kept separate so it stays fast and free
* **Resend** — transactional email
* **Billplz / DuitNow** — Malaysian payment rails, because Stripe isn't how Malaysians pay

Multi-tenancy rides on Laravel's native Teams feature — every vehicle, service record, and booking scopes to the authenticated team, never trusting IDs from request input. One schema serves every tier from free solo users to fleet operators, gated purely by plan.

---

## The Zero-Idle-Cost OCR Ladder

The most interesting engineering constraint in this project: receipt scanning must cost nothing when nobody is using it.

A solo bootstrapped SaaS can't afford a cloud OCR bill that ticks up with every experiment. So instead of one OCR solution, CareReta uses a three-tier degradation ladder:

1. **Tesseract.js in the browser** — free, runs client-side, zero server cost. Handles clean printed receipts.
2. **Live Text paste fallback** — if auto-scan fails, users on modern phones can select text directly from the photo and paste it. The OS does the OCR for free.
3. **AWS Textract** — reserved for paid tiers only, where the revenue justifies the per-scan cost.

The parser on top is where the real work lives: Malaysian workshop invoices have their own vocabulary — Proton/Perodua part names, oil viscosity formats, handwritten totals — with price-gating rules to reject nonsense extractions before they pollute a user's logbook.

> The lesson: the constraint was the design. "Zero idle cost" forced an architecture that's actually more resilient than a single cloud API call — because there's always a fallback.

---

## Final Thoughts

CareReta is still in beta, and the roadmap is long — fuel logging, insurance renewal reminders, workshop collaboration flows. But the foundation is proving itself: real users, real cars, real service records being logged by drivers who used to keep receipts in a plastic bag.

The biggest takeaway isn't technical. It's that a solo developer with 2–3 hours a day can ship a real SaaS — if every feature earns its way in before it's built.

If you drive in Malaysia and your service book is currently "somewhere in the car" — [carereta.my](https://carereta.my/) is waiting.

---
## **Project Snapshot**

<div style="display: flex; gap: 12px; overflow-x: auto;">
    <img src="/articles/carereta-hero.png" width="200" />
    <img src="/articles/carereta-know-your-car.png" width="200" />
    <img src="/articles/carereta-records.png" width="200" />
    <img src="/articles/carereta-dashboard.png" width="200" />
</div>
---
