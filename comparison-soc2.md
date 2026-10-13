# ISO/IEC 42001 vs SOC 2: for the US market

> 🇷🇺 [Читать на русском](./ru/comparison-soc2.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** SOC 2 is the principal compliance framework for US enterprise buyers. ISO/IEC 42001 covers AI-specific ground SOC 2 does not address. Most auditors (Schellman, A-LIGN, Coalfire) offer combined SOC 2 + ISO 42001 audits at 30–50 % discount. Best pattern for a US SaaS: SOC 2 Type II as the base, ISO 42001 as the AI overlay.

---

## Contents

- [1. Main differences](#1-main-differences)
- [2. Trust Services Criteria and Annex A of 42001](#2-trust-services-criteria-and-annex-a-of-42001)
- [3. Combined SOC 2 + ISO 42001 audit](#3-combined-soc-2--iso-42001-audit)
- [4. What to choose in different scenarios](#4-what-to-choose-in-different-scenarios)

---

## 1. Main differences

| Parameter | SOC 2 | ISO/IEC 42001 |
|-----------|-------|----------------|
| Type | Attestation (AICPA SSAE 18) | Certification (ISO/IEC) |
| Jurisdiction | US (historically), global as de facto standard | International |
| Auditor | CPA firm | ANAB/UKAS-accredited CB |
| Object | Trust Services Criteria (Security, Availability, Confidentiality, Processing Integrity, Privacy) | AI management system |
| Validity | Type I — point-in-time; Type II — period (typically 6–12 months) | 3 years |
| Management system | Not required as a formal construct | Mandatory (Annex SL) |
| Annex A controls | TSC criteria (~64–195 depending on scope) | 38 controls |
| Public/private | SOC 2 report is confidential, delivered under NDA | Certificate is public |
| Best for | US enterprise B2B, especially finance, healthcare, SaaS | AI providers, Microsoft SSPA, EU AI Act |

---

## 2. Trust Services Criteria and Annex A of 42001

SOC 2 covers 5 categories of **Trust Services Criteria (TSC)**:

- **Security (Common Criteria)** — mandatory.
- **Availability** — optional.
- **Confidentiality** — optional.
- **Processing Integrity** — optional.
- **Privacy** — optional.

| TSC | Annex A 42001 | Overlap |
|-----|----------------|---------|
| CC1 Control Environment | A.2.2 AI Policy, A.3.2 Roles | High |
| CC2 Communication | Clause 7.4 | High |
| CC3 Risk Assessment | Clause 6.1, A.5 AISIA | Medium (SOC 2 covers classic risks; 42001 adds AI) |
| CC4 Monitoring | Clause 9.1, A.6.2.6 | High |
| CC5 Control Activities | Annex A controls | Medium |
| CC6 Logical/Physical Access | A.4 Resources | High (for security) |
| CC7 System Operations | A.6 Lifecycle | Medium (42001 is deeper on AI lifecycle) |
| CC8 Change Management | Clause 6.3, A.6.2.5 | High |
| CC9 Risk Mitigation | A.5 + A.6 | Medium |
| Availability | A.6.2.6 Operation | Medium |
| Processing Integrity | A.6.2.4 V&V | High (42001 adds AI specifics) |

**What SOC 2 does not have (but 42001 does):**
- AI System Impact Assessment (A.5).
- Human oversight levels (A.6.1.2).
- Annex A.7 Data for AI (lineage, provenance).
- Annex A.8 Information for stakeholders (AI-specific disclosures).

**What 42001 does not have (but SOC 2 does):**
- Detailed Privacy criteria (when P category applies).
- Detailed physical security controls.
- Deeper vendor management formalism.

---

## 3. Combined SOC 2 + ISO 42001 audit

CBs active in combined SOC 2 + ISO 42001:
- **Schellman** — market leader, first ANAB-accredited CB for 42001.
- **A-LIGN**.
- **Coalfire**.
- **BDO**, **EY CertifyPoint**.

**Savings:** 30–50 % vs. two separate audits. This works because:
- One scope statement for both.
- One risk register (with an AI section).
- One internal audit program.
- One management review with an AI block.
- Combined SoA tagged SOC 2 / ISO 42001.

**Timeline:** combined audit for a 50–200 FTE SaaS — 6–12 months from kickoff to SOC 2 report and 42001 certificate.

**Combined budget:** $80–250 K in year 1 depending on size and maturity.

---

## 4. What to choose in different scenarios

### US market only, B2B SaaS

**Start:** SOC 2 Type II. The cybersecurity-first buyer expects SOC 2.
**After 6–12 months:** add ISO 42001 once AI features are present in the product.

### EU market and/or Microsoft SSPA

**Start:** ISO 27001 + ISO 42001. SOC 2 does not cover Microsoft SSPA Section K AI specifics and does not grant presumption of conformity under EU AI Act.

### Both US and EU enterprise

**Start:** combined SOC 2 + ISO 27001 + ISO 42001. Maximum coverage.

### Healthcare with PHI

**Start:** SOC 2 + HIPAA. ISO 42001 — when AI features influence medical decisions.

### FinTech, banking

**Start:** SOC 1 (financial reporting) + SOC 2 + ISO 27001. ISO 42001 — for AI models in scoring/AML/KYC.

---

## Need help choosing SOC 2 vs ISO 42001?

> 📩 **Free 15-minute consultation in Telegram**
> We map your customers' jurisdictions and compliance asks, then propose a minimal sufficient set.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [ISO 27001 comparison](./comparison-iso-27001.md)
- [EU AI Act comparison](./comparison-eu-ai-act.md)
- [Microsoft SSPA — supplier requirements](./supplier-requirements.md)
- [Cost and timeline](./cost-timeline.md)

---

*Sources: AICPA SSAE 18; SOC 2 Trust Services Criteria 2017 (updated 2022); ISO/IEC 42001:2023 Annex A; Schellman SOC 2 + ISO 42001 guides; A-LIGN; Coalfire; BDO; EY CertifyPoint; Vanta SOC 2 vs ISO 42001 comparison; Drata; Sprinto.*
