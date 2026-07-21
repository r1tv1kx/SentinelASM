# SentinelASM

**SentinelASM** is a full-stack Attack Surface Management (ASM) platform that lets anyone scan a domain and get back a plain-English security assessment — no security expertise required.

🔗 **Live app:** [sentinel-frontend-3kx1.onrender.com](https://sentinel-frontend-3kx1.onrender.com)

## What it does

Point SentinelASM at a domain and it orchestrates **ten independent scan modules** to map out the target's external attack surface:

- WHOIS lookup
- DNS records
- SSL/TLS configuration
- HTTP security headers
- Port scanning
- Technology fingerprinting
- Subdomain enumeration
- Email authentication (SPF / DKIM / DMARC)
- CVE matching
- Redirect-chain analysis

Progress streams live to the frontend over WebSockets as each module completes, and the findings are rolled into a transparent **0–100 security score** with an associated risk level.

An AI-assisted layer (OpenAI, with a graceful template fallback when no API key is configured) turns the raw findings into:

- An executive summary in plain English
- Prioritized, effort-estimated recommendations
- A downloadable PDF report

## Frontend features

The React + TypeScript + Tailwind frontend adds:

- JWT-authenticated accounts
- Scan history
- Re-scan / diff comparison to track what changed over time
- A "quick wins" panel that surfaces the highest-impact fixes first
- A standalone **Fake-Link Checker** — paste any URL and it traces the redirect chain to flag phishing-style tricks (off-domain hops, punycode, shorteners, hidden meta-refreshes) before you click it

## Stack

- **Backend:** FastAPI + SQLAlchemy/PostgreSQL
- **Frontend:** React + TypeScript + Tailwind CSS
- **Real-time updates:** WebSockets
- **AI layer:** OpenAI, with template-based fallback

## Deployment

SentinelASM can be deployed either:

- Via **Docker Compose** for local development or self-hosting, or
- As a **one-click Render Blueprint** for production
