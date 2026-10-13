# Integrated Management System: ISO/IEC 42001 + 27001 + 9001 and beyond

> 🇷🇺 [Читать на русском](./ru/integrated-management-system.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** Annex D of ISO/IEC 42001 maps directly to ISO 9001 (quality), ISO/IEC 27001 (security), ISO 31000 (risk), ISO 37301 (compliance). This is the foundation for an Integrated Management System (IMS) — a single process foundation with separate top-level policies and SoAs. IMS yields 30–50 % reduction in compliance-team load and 30–50 % savings on combined audits.

---

## Contents

- [1. What an IMS is](#1-what-an-ims-is)
- [2. 42001 Annex D: mapping](#2-42001-annex-d-mapping)
- [3. IMS architecture for an AI company](#3-ims-architecture-for-an-ai-company)
- [4. What to merge, what to keep separate](#4-what-to-merge-what-to-keep-separate)
- [5. Combined audits](#5-combined-audits)
- [6. Cases](#6-cases)

---

## 1. What an IMS is

An Integrated Management System is **internal process organization**, not a separate certificate. The idea: a common process foundation on which standard-specific requirements stack.

IMS works because all modern ISO management standards are built on Annex SL High-Level Structure: identical clauses 4–10, identical concepts (risk, context, stakeholders, documented information, corrective actions).

Standards most commonly combined into an IMS:
- ISO 9001 — quality
- ISO/IEC 27001 — information security
- ISO/IEC 27701 — privacy
- ISO 14001 — environment
- ISO 22301 — business continuity
- ISO 13485 — medical devices
- ISO 37301 — compliance
- ISO/IEC 42001 — AI
- ISO 45001 — occupational health and safety

---

## 2. 42001 Annex D: mapping

Annex D (informative appendix to ISO/IEC 42001:2023) shows direct correspondences between 42001 and:

- **ISO 9001:2015** — shared clauses 4–10 structure, "context", "leadership", "risk-based thinking".
- **ISO/IEC 27001:2022** — Annex SL, risk management, SoA, internal audit, management review. About 40 % overlap.
- **ISO 31000:2018** — risk management methodology. ISO/IEC 23894 (AI risk) is built on 31000.
- **ISO 37301:2021** — compliance management, regulator reporting.

Annex D is **informative**, providing recommendations rather than requirements.

---

## 3. IMS architecture for an AI company

Typical IMS architecture for a SaaS holding 27001 + 42001 + 27701:

```
                    ┌────────────────────────────────┐
                    │   Management Board / CEO       │
                    │   (shared leadership Cl. 5)    │
                    └──────────────┬─────────────────┘
                                   │
        ┌──────────────────────────┼──────────────────────────┐
        │                          │                          │
┌───────▼────────┐        ┌────────▼────────┐        ┌───────▼────────┐
│  CISO / AIMS   │        │     CPO/DPO     │        │  Head of QMS   │
│     Lead       │        │                 │        │                │
└───────┬────────┘        └────────┬────────┘        └───────┬────────┘
        │                          │                          │
   27001 SoA                  27701 SoA                 9001 controls
   42001 SoA                  GDPR DPIA                  
                                                              
        ┌─────────────────────────────────────────────────────┐
        │       Shared processes (on one HLS):                │
        │  • Context and stakeholders (Cl. 4)                 │
        │  • Document control (Cl. 7.5)                       │
        │  • Internal audit (Cl. 9.2)                         │
        │  • Management review (Cl. 9.3)                      │
        │  • Nonconformity & corrective action (Cl. 10.1)     │
        │  • Risk management methodology                      │
        │  • Supplier management                              │
        │  • Awareness & training                             │
        │  • Communication                                    │
        │  • Change management                                │
        └─────────────────────────────────────────────────────┘
```

---

## 4. What to merge, what to keep separate

### Merge (one process across standards)

- **Document control** — shared policy, shared template, single versioning.
- **Internal audit program** — one program, one team, different criteria in checklists.
- **Management review** — one session, agenda with per-standard blocks.
- **Nonconformity and corrective action** — one process, one tracker.
- **Risk management methodology** — shared scales, shared register format. Risk objects and categories differ.
- **Supplier management** — shared due diligence. AI-vendor checklists (A.10.3) are specific.
- **Training & awareness** — one LMS, different courses.
- **Communication** — shared channels.

### Keep separate

- **Top-level policies** — Information Security Policy, AI Policy, Privacy Policy, Quality Policy.
- **Statement of Applicability** — per-standard SoA (can live in one file with tags).
- **Object inventories** — information assets, AI systems, personal-data processings.
- **Metrics and KPIs** — per-standard.

### Hybrid

- **Risk register** — shared file with categories: information / AI / privacy / quality. Each entry tagged with applicable standards.

---

## 5. Combined audits

CBs can perform combined audits across multiple standards. Conditions:

- One CB accredited for all standards in scope.
- One scope statement.
- Combined SoA with tags.
- One risk register.

**Savings:**
- 27001 + 42001 combined: 30–50 % vs two separate audits.
- 27001 + 27701 + 42001 combined: 40–60 %.
- 9001 + 27001 + 42001 combined: 40–55 %.

**Combined-audit-active CBs:**
- **BSI** — all ISO standards, including 27001 + 42001 + 27701 in one engagement.
- **Schellman** — 27001 + 42001, SOC 2 + 27001, SOC 2 + 42001.
- **A-LIGN** — same.
- **DNV** — especially strong in 9001 + 14001 + 45001 IMS audits.
- **TÜV Nord/Rheinland** — IMS for manufacturing.

---

## 6. Cases

**Microsoft 365 Copilot** — combined 27001 + 27701 + 42001 SoA in one engagement (Mastermind / IAS, March 2025).

**Workday** — 27001 + 27701 + 42001 in one IMS structure. 12 product lines in one scope, one 42001 certificate on top of existing ones (Schellman, 2025).

**Anthropic** — 27001 + 27701 + 27017 + 27018 + SOC 2 + ISO 42001. Combined audit cycle, Schellman (January 2025).

**IBM** — 27001 + 27017 + 27018 + 27701 + 42001. The mature IMS is the reason the 42001 audit took 3 months (kickoff → certification).

---

## IMS benefits in numbers

Per DQS and ISMS.online:

- **30–50 % reduction** in compliance-team load.
- **30–50 % savings** on CB fees in combined audits.
- **40–60 % faster** time-to-certification for the second and subsequent standards.
- **20–40 % fewer documents** thanks to merged documentation.

---

## Need help designing your IMS?

> 📩 **Free 15-minute consultation in Telegram**
> We map your compliance landscape and propose an IMS architecture minimising duplication.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [ISO/IEC 42001 structure](./structure.md)
- [ISO 27001 comparison](./comparison-iso-27001.md)
- [ISO/IEC AI family of standards](./family-of-standards.md)
- [Cost and timeline](./cost-timeline.md)

---

*Sources: ISO/IEC 42001:2023 Annex D; Annex SL ISO/IEC Directives Part 1; ISO 9001:2015; ISO/IEC 27001:2022; ISO/IEC 27701:2019; ISO 31000:2018; ISO 37301:2021; ISO 22301; ISO 13485; ISO 14001; ISO 45001; DQS Integrated Management System Practice; ISMS.online; BSI Combined Audit Guide; Schellman; A-LIGN; DNV; TÜV; Microsoft Trust Center; Anthropic Privacy Center; Workday Trust; IBM Think.*
