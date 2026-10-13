# Public Registry of ISO/IEC 42001 Certified Organizations

> 🇷🇺 [Читать на русском](./ru/certified-companies.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** A curated list of organizations that have publicly announced ISO/IEC 42001:2023 certification. Sources: company press releases, Trust Centers, accredited certification body blogs. The list is **not exhaustive** — ISO maintains no public registry; many companies do not disclose certification. If you spot a gap — [open an Issue](https://github.com/easy-standart/iso-42001-guide/issues/new).

> **Last updated:** see commit history. Refreshed monthly.

---

## Contents

- [Summary statistics](#summary-statistics)
- [Chronological list](#chronological-list)
- [By industry](#by-industry)
- [By certification body](#by-certification-body)
- [Scope patterns](#scope-patterns)

---

## Summary statistics

- **Early 2026:** ~40 publicly announced certificates.
- **Mid 2026:** estimated 100+ (per BCG, A-LIGN, Schellman reporting).
- **Hyperscaler coverage:** 5 of top-10 cloud providers already certified.
- **Big 4 / consulting:** KPMG (December 2025), BCG (January 2026); EY, Deloitte, PwC, McKinsey — no public announcements at the time of update.

---

## Chronological list

### 2024

| Company | Date | Scope | Certification body | Source |
|---------|------|-------|--------------------|--------|
| Synthesia | September 2024 | AI Video Generation Platform | A-LIGN | Press release |
| Amazon Web Services | November 2024 | Bedrock, Q Business, Textract | Schellman | AWS Security Blog |
| Google Cloud | December 2024 | Vertex AI, Gemini, Document AI | Not disclosed | Google Cloud Trust Center |
| Cognizant | December 2024 | AI services portfolio | DNV | Press release |

### 2025

| Company | Date | Scope | Certification body | Source |
|---------|------|-------|--------------------|--------|
| Anthropic | January 2025 | Claude (API + Enterprise) | Schellman | Trust Center |
| Workday | 2025 | AI/ML used across Workday platform | Schellman | Press release |
| Microsoft | March 2025 | Microsoft 365 Copilot | Mastermind (IAS) | Microsoft Trust Center |
| Microsoft | July 2025 | Azure AI Foundry, Security Copilot | Mastermind (IAS) | Microsoft Trust Center |
| 6 Clicks | August 2025 | GRC platform with AI | A-LIGN | Press release |
| Microsoft | September 2025 | Copilot Studio, GitHub Copilot | Mastermind (IAS) | Microsoft Trust Center |
| IBM | September 2025 | Granite (open-source models) | Schellman | IBM blog |
| Integral Ad Science | October 2025 | Ad measurement AI | Schellman | Press release |
| Meltwater | November 2025 | Media intelligence AI | A-LIGN | Press release |
| KPMG International | December 2025 | Global structure | Schellman | KPMG press release |

### 2026

| Company | Date | Scope | Certification body | Source |
|---------|------|-------|--------------------|--------|
| CM.com | January 2026 | Conversational AI platform | A-LIGN | Press release |
| CrowdStrike | January 2026 | Charlotte AI (cybersecurity AI) | A-LIGN | Press release |
| BCG | January 2026 | Global structure (one of first 100) | Schellman | BCG news |
| Datamatics | January 2026 | AI services portfolio | TÜV Nord | Press release |
| Evisort | February 2026 | Contract AI platform | A-LIGN | Press release |
| AI Clearing | February 2026 | Construction AI | A-LIGN | Press release |
| ORO Labs | February 2026 | Procurement AI | Schellman | Press release |
| Mimecast | February 2026 | Email security AI | A-LIGN | Press release |
| Spektr | March 2026 | KYC/AML AI | BSI | Press release |
| Thoropass | March 2026 | Compliance AI platform | Schellman | Press release |
| Kandji | March 2026 | Apple device management AI | A-LIGN | Press release |
| Vanta | March 2026 | Trust management AI | A-LIGN | Press release |
| Stackaware | March 2026 | AI security platform | A-LIGN | Press release |
| Ema Unlimited | April 2026 | Enterprise AI agents | Schellman | Press release |

---

## By industry

### Cloud / Hyperscalers
AWS, Google Cloud, Microsoft (multiple Copilot products), IBM.

### AI/ML providers
Anthropic, Synthesia, Ema Unlimited.

### Cybersecurity
CrowdStrike, Mimecast, Stackaware.

### GRC / Compliance
6 Clicks, Vanta, Thoropass.

### FinTech / KYC
Spektr.

### HR / Workforce
Workday.

### Marketing / Media
Meltwater, Integral Ad Science.

### Legal / Contracts
Evisort.

### Devices / IT Management
Kandji.

### Construction
AI Clearing.

### Consulting
KPMG International, BCG, Cognizant.

### Conversational / SMS
CM.com.

---

## By certification body

### A-LIGN (most active CB for 42001)
Synthesia, 6 Clicks, Meltwater, CrowdStrike, CM.com, Evisort, AI Clearing, Mimecast, Kandji, Vanta, Stackaware.

### Schellman (first ANAB-accredited)
Anthropic, AWS, Workday, IBM, Integral Ad Science, BCG, ORO Labs, Ema Unlimited, KPMG International, Thoropass.

### Mastermind (IAS-accredited)
Microsoft (multiple Copilot products).

### BSI (triple-accredited: ANAB + UKAS + RvA)
Spektr.

### DNV
Cognizant.

### TÜV Nord
Datamatics.

---

## Scope patterns

Public scope statements reveal three patterns:

### Pattern 1: Per product / service (dominant)
Most companies certify a **specific product**, not the whole organisation. Examples:
- AWS — Bedrock, Q Business, Textract separately.
- Microsoft — M365 Copilot, Azure AI Foundry, Security Copilot, Copilot Studio, GitHub Copilot — each a separate certificate with its own SoA.
- Google Cloud — Vertex AI, Gemini, Document AI.

**Why:** lower audit-failure risk, cheaper first certificate, marketing clarity ("our product X is certified").

### Pattern 2: By organisational function
Anthropic — certified "Claude API + Enterprise" — not a product per se, but a block of organisational functions around the product.

### Pattern 3: Global structure
KPMG International, BCG — certify the whole organisation globally. Fits large consultancies where AI tools are used cross-functionally.

### Scope expansion at recertification
- Integral Ad Science: initial certificate on a narrow scope → recertification (February 2026) added "Quality Attention" and "Ad Fraud solutions".
- Microsoft: each new Copilot product gets its own certificate without recertifying existing ones.

---

## What this means for your company

Three takeaways:

1. **Narrow scope is the norm, not the exception.** Do not try to certify the whole company at once. One product, one BU, one region — that is the standard pattern.

2. **Marketing impact compounds with multiple certificates.** Microsoft gets PR mileage from each new Copilot certificate. You can plan a roadmap: one certificate this year, scope expansion in two years.

3. **The "first hundred" window is closing.** Early 2026 — ~40 companies. End of 2026 — estimated 150–200. End of 2027 — 500+. After 2027 this stops being a marketing differentiator.

---

## Want to be on this list?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss your situation: how to scope, which CB fits your market, realistic timelines.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [ANAB-accredited certification bodies](./anab-accredited-cbs.md)
- [Detailed public case studies](./case-studies.md)
- [Supplier requirements at Microsoft and other hyperscalers](./supplier-requirements.md)

---

*If you spot an inaccuracy or want to add a company — [open an Issue](https://github.com/easy-standart/iso-42001-guide/issues/new). Include: company, date, scope, certification body, link to press release or Trust Center.*

*Sources: press releases and Trust Centers of listed companies; BSI, DNV, Schellman, A-LIGN, Coalfire, TÜV blogs; BCG news (27 January 2026); CrowdStrike Holdings IR (22 January 2026); CM.com press (6 January 2026); A-LIGN client list.*
