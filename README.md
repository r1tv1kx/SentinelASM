<div align="center">

# Sentinel

**Point it at a domain. Get back a plain-English security assessment.**

No security expertise required — just a domain name.

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen?style=for-the-badge)](https://sentinel-frontend-3kx1.onrender.com)
&nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### [**Try it live → sentinel-frontend-3kx1.onrender.com**](https://sentinel-frontend-3kx1.onrender.com)

</div>

---

## Contents

- [What is Sentinel?](#what-is-sentinel)
- [Scan modules](#scan-modules)
- [What you get](#what-you-get)
- [Frontend features](#frontend-features)
- [Stack](#stack)
- [Deployment](#deployment)

## What is Sentinel?

**Sentinel** is a full-stack attack surface management platform. Enter any domain, and the backend orchestrates **ten independent scan modules** in parallel, streams progress live over WebSockets, and rolls everything into one transparent **0–100 security score** — with a plain-English explanation of what's actually wrong and how to fix it.

No dashboards full of jargon. No raw scanner output to decode. Just the answer: *is this domain safe, and what should I fix first?*

## Scan modules

| Module | What it checks |
|---|---|
| **WHOIS** | Domain registration & ownership details |
| **DNS** | Record configuration & misconfigurations |
| **SSL/TLS** | Certificate validity & cipher strength |
| **HTTP Security Headers** | CSP, HSTS, X-Frame-Options, and more |
| **Port Scanning** | Exposed services on the target |
| **Technology Fingerprinting** | Frameworks, CMS, and libraries in use |
| **Subdomain Enumeration** | Discovering the full external footprint |
| **Email Authentication** | SPF, DKIM, DMARC configuration |
| **CVE Matching** | Known vulnerabilities in detected tech |
| **Redirect-Chain Analysis** | Where a link actually takes you |

All ten run concurrently, so a full assessment comes back in the time it takes the slowest module to finish — not the sum of all ten.

## What you get

- **A transparent 0–100 security score** with risk level — every point is traceable back to a finding, not a black box
- **Live progress over WebSockets** as each of the ten modules completes
- **AI-generated executive summary** (OpenAI, with a graceful template fallback if no API key is set)
- **Prioritized, effort-estimated recommendations** — know what to fix first and how long it'll take
- **A downloadable PDF report** to share with your team or client

## Frontend features

- JWT-authenticated accounts
- Scan history, with re-scan & diff comparison to track what changed over time
- **Quick Wins panel** — the highest-impact fixes, surfaced first
- **Fake-Link Checker** — a standalone tool that traces a pasted URL's full redirect chain and flags phishing-style tricks: off-domain hops, punycode lookalikes, link shorteners, and hidden meta-refreshes — before you ever click it

## Stack

| Layer | Tech |
|---|---|
| Backend | FastAPI + SQLAlchemy / PostgreSQL |
| Frontend | React + TypeScript + Tailwind CSS |
| Real-time | WebSockets |
| AI layer | OpenAI (template fallback if unset) |

## Deployment

Run it however suits you:

- **Docker Compose** — spin the whole stack up locally or self-host it
- **Render Blueprint** — one-click deploy straight to production

---

<div align="center">

**[Launch Sentinel →](https://sentinel-frontend-3kx1.onrender.com)**

</div>
