# ISO/IEC 42001 ↔ EU AI Act: article-by-article mapping

> 🇷🇺 [Читать на русском](./ru/comparison-eu-ai-act.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** By common consulting estimates ISO/IEC 42001 covers roughly 40–50 % of EU AI Act requirements, mostly the organizational and management layer (risk management, documentation, monitoring). The certificate does not grant presumption of conformity under Article 40 (see [prEN 18286](./pren-18286-vs-iso-42001.md)), but it materially reduces work on Art. 9, 10, 14, 15, 17, 72. This document maps the 13 key articles and the status of the Digital Omnibus on AI (proposed 19 November 2025, in force 27 July 2026).

---

## Contents

- [1. The nature of the 40–50 % overlap](#1-the-nature-of-the-4050-overlap)
- [2. Article-by-article mapping](#2-article-by-article-mapping)
- [3. AI Act application phases](#3-ai-act-application-phases)
- [4. Digital Omnibus on AI and "stop-the-clock"](#4-digital-omnibus-on-ai-and-stop-the-clock)
- [5. GPAI Code of Practice (10 July 2025)](#5-gpai-code-of-practice-10-july-2025)
- [6. Fines](#6-fines)
- [7. Practical takeaways](#7-practical-takeaways)

---

## 1. The nature of the 40–50% overlap

EU AI Act is a **product safety regulation**. ISO/IEC 42001 is a **management system** standard. They operate at different layers. The often-cited **40–50 %** figure is an aggregated estimate from consultancies and certification bodies, not a number published by a regulator or ISO — treat it as an order of magnitude.

What 42001 covers:
- Management layer (clauses 4–10): context, leadership, planning, support, operations, evaluation, improvement.
- 38 Annex A controls: policies, resources, AISIA, lifecycle, data, stakeholder information, use, third parties.

What 42001 **does not** cover:
- Regulatory procedures: classification of high-risk per Annex III, conformity assessment, registration in the EU AI Office database.
- Specific quantitative requirements for accuracy, robustness, cybersecurity.
- Specific retention period (10 years per Art. 18).
- Notification windows for serious incidents (15 days; 72 hours for systemic-risk GPAI).
- Deepfake and synthetic content watermarking (Art. 50).

42001 is the foundation on which AI Act compliance is built. The full path runs through [prEN 18286](./pren-18286-vs-iso-42001.md), which once published in the OJ will grant presumption of conformity.

---

## 2. Article-by-article mapping

| AI Act article | Requirement | 42001 clauses and controls | Coverage | What is not covered |
|---|---|---|---|---|
| **Art. 4** AI literacy | Adequate AI literacy for supplier and deployer personnel | Cl. 7.2 (competence), 7.3 (awareness), A.3.2 (roles) | High | Specific educational requirements, documented literacy evidence |
| **Art. 5** Prohibited practices | 8 categories of prohibited AI | No direct analogue; indirectly A.9.2 (use policy), A.5 (AISIA) | Low | Pure regulatory matter |
| **Art. 9** Risk management system (high-risk) | Continuous identification / assessment / mitigation over the lifecycle | Cl. 6.1.2 (AI risk assessment), 6.1.3 (treatment), 6.1.4 (AISIA), 8.2 (treatment implementation), 9.1 (monitoring) | Very high | "Residual risk acceptable" wording; Annex III linkage; mandatory pre-market testing |
| **Art. 10** Data and data governance | Quality, relevance, representativeness of training / validation / test datasets; bias accounting | A.7.2–A.7.6 (sources, quality, preparation, lineage), cl. 8.3 | High | Specific examination requirements for bias; categories of personal data for bias detection (Art. 10(5)) |
| **Art. 11 + Annex IV** Technical documentation | Pre-market technical documentation in a strictly defined format | Cl. 7.5 (documented information), A.6.1.2 (lifecycle documentation) | Medium | Specific Annex IV fields (model description, metrics, logic, versions, conformity assessment) |
| **Art. 12** Automatic logging | Technical system logs | A.6.2.8 (event recording), cl. 9.1 | Medium | Specific events for mandatory logging; retention (6 months – 10 years) |
| **Art. 13** Transparency and instructions for users | Instructions for use for deployers | A.8.2 (reporting), A.8.3 (external info), cl. 7.4 (communication) | High | Specific contents of instructions for use |
| **Art. 14** Human oversight | Measures for "meaningful" oversight | A.6.2.3 (V&V), A.9.2 (intended use) | High | "Four eyes" requirement, automation bias control |
| **Art. 15** Accuracy, robustness, cybersecurity | Technical lifecycle requirements | A.6.2.4 (V&V), A.7.4 (data quality), A.6.2.6 (deployment), cl. 10.2 (corrective actions) | High | Minimum quantitative levels (expected in harmonised CEN-CENELEC standards) |
| **Art. 17** Quality management system | QMS for high-risk suppliers | Clauses 4 (context), 5 (leadership), 6 (planning), 7 (support), 8 (operations), 9 (evaluation), 10 (improvement) — **the entire AIMS frame** | Maximum | Specific Art. 17(1) items: testing procedures; post-market monitoring; incident notification system |
| **Art. 18–21** Documentation retention, corrective actions | 10-year retention | Cl. 7.5, 10.1–10.2 | High | Specific 10-year period |
| **Art. 25–26** Deployer obligations | Due diligence, monitoring, registration | A.10.2–A.10.4 (third parties), A.9.2, cl. 8.5 | High | Specific obligation to register in the EU database |
| **Art. 43 + Annex VI/VII** Conformity assessment | Self-assessment or notified-body assessment | Cl. 9.2 (internal audit) — partial only | Low | Regulatory procedure absent from ISO 42001 |
| **Art. 49** Registration in the EU database | High-risk entry in the public database | — | Not covered | Pure regulatory procedure |
| **Art. 50** Transparency for certain AI systems | Deepfake, synthetic content, chatbot marking | A.8.2, cl. 7.4 | Medium | Specific watermarking technical requirements (Code of Practice expected 2026) |
| **Art. 53–55** GPAI and systemic-risk GPAI obligations | Model documentation, copyright compliance policy, systemic risk assessment | Cl. 6.1 (risks), A.5 (AISIA), A.6–A.7, A.10 | High | GPAI Code of Practice 2025 — a separate instrument (see section 5) |
| **Art. 72** Post-market monitoring | Continuous monitoring plan and implementation | Cl. 9.1, 9.3 (management review), A.6.2.6 | Medium | Specific plan as a standalone artefact |
| **Art. 73** Serious incident notification | National regulator notification | Cl. 10.1, A.8.2 | Low | 15 days (serious) and 72 hours (systemic-risk GPAI); notification channels |

**Mapping sources:** A-LIGN "Preparing for EU AI Act Compliance with ISO 42001"; Schellman/RockCyber; Glocert International; BD Emerson; Blue Arrow (Art. 17); ISACA; EU AI Compass; Vanta.

---

## 3. AI Act application phases

| Date | Obligations | Status (updated September 2026) |
|------|-------------|--------------------------|
| 1 August 2024 | Regulation 2024/1689 enters into force | Done |
| 2 February 2025 | Chapters I, II — prohibited AI practices (Art. 5) + AI literacy obligations (Art. 4) | In force |
| 2 August 2025 | GPAI provider obligations, governance, sanctions (except Art. 101) | In force |
| 2 February 2026 | Commission guidance on practical Art. 6 application (high-risk classification) | Partially done; second draft of marking Code of Practice in March 2026 |
| **2 August 2026 → 2 December 2027** | High-risk Annex III obligations, deployer obligations, conformity assessment bodies | **Postponed to 2 December 2027 by the Digital Omnibus — see section 4** |
| 2 August 2027 → 2 August 2028 | High-risk AI embedded in Annex I products (medical devices, toys, transport) + legacy GPAI compliance deadline | Postponed to 2 August 2028 by the Digital Omnibus |

---

## 4. Digital Omnibus on AI and "stop-the-clock"

On 19 November 2025 the European Commission proposed the **Digital Omnibus on AI** — a targeted amendment package to the Regulation.

**Main proposals:**

- Application of high-risk AI rules made conditional on availability of harmonised standards, common specifications, or guidance. Long-stop dates: **2 December 2027** for Annex III and **2 August 2028** for systems in regulated products.
- Application of Art. 50(2) (watermarking of synthetic content for systems deployed before 2 August 2026) postponed 6 months — to **2 February 2027**.
- Simplified QMS regime extended to broader SMEs.
- Single Entry Point (SEP) for incident reporting across GDPR, NIS2, DORA, AI Act.
- Clarification of AI Act vs sectoral legislation boundaries (MDR, IVDR).

**Outcome (as of September 2026):**

- The Digital Omnibus on AI was adopted and **entered into force on 27 July 2026** (published in the OJ on 24 July 2026).
- Application of the high-risk rules is now tied to the availability of harmonised standards, with long-stop dates of **2 December 2027** (Annex III) and **2 August 2028** (systems embedded in regulated products).
- Watermarking of synthetic content under Art. 50(2) was postponed to **2 February 2027**.

---

## 5. GPAI Code of Practice (10 July 2025)

- Published 10 July 2025 after four drafting rounds with ~1000 stakeholders.
- 1 August 2025 — Commission and AI Board confirmed adequacy.
- Three chapters: **Transparency** (all GPAI providers), **Copyright** (all), **Safety** (only systemic-risk GPAI — compute threshold 10²⁵ FLOPs; 5–15 companies globally).
- 18 July 2025 — Commission guidance on GPAI; 24 July 2025 — mandatory training data summary template.
- Signatories include Google, OpenAI, Microsoft, Anthropic, Mistral, xAI (the last on Safety only).
- Until 2 August 2026 the AI Office applies "collaborative enforcement". From 2 August 2026 — full enforcement powers.
- Code conformance maps onto ISO/IEC 42001 Annex A: A.3 (roles/policies), A.6 (lifecycle), A.7 (data), A.8 (documentation), A.10 (suppliers).

---

## 6. Fines

| Violation | Fine |
|------------|------|
| Prohibited practices (Art. 5) | Up to €35 M or 7 % global turnover |
| High-risk obligation breach | Up to €15 M or 3 % global turnover |
| Providing incorrect information to a regulator | Up to €7.5 M or 1 % |
| GPAI obligations | Up to 3 % global revenue or €15 M (for systemic-risk GPAI after 2 August 2026) |

---

## 7. Practical takeaways

1. **ISO/IEC 42001 is necessary but not sufficient for AI Act.** The certificate closes an estimated 40–50 % of requirements. The rest goes through notified-body assessment or the future harmonised standard prEN 18286.

2. **The "best-covered" articles**: Art. 9 (risk management), Art. 17 (QMS), Art. 10 (data governance), Art. 14 (oversight), Art. 15 (V&V). On these articles the AIMS lifts nearly 1:1.

3. **The "leakiest" articles**: Art. 5 (prohibitions), Art. 43 (conformity assessment), Art. 49 (registration), Art. 73 (incident reporting). Pure regulatory procedures.

4. **Stop-the-clock does not pause preparation.** Even if deadlines slip to 2027–2028, enterprise contracts already require 42001 today.

5. **What to monitor quarterly**: Digital Omnibus status, new harmonised standard drafts from CEN-CENELEC, GPAI Code of Practice updates, designation of national competent authorities.

---

## Need help shaping an AI Act compliance strategy?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss which articles apply to your product, how much of the estimated 40–50 % coverage you already have, and what to add.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [ISO 42001 vs NIST AI RMF](./comparison-nist-ai-rmf.md)
- [Standard overview](./README.md)
- [ISO 42005 — AI System Impact Assessment](./iso-42005-impact-assessment-guide.md)

---

*Sources: EU AI Act (Regulation 2024/1689); Digital Omnibus on AI proposal (19 November 2025); Council of the EU negotiating position (13 March 2026); EU Parliament plenary vote (26 March 2026); GPAI Code of Practice (10 July 2025); AI Office; A-LIGN; Schellman; RockCyber; Blue Arrow; Elevate Consult; ISACA; EU AI Compass; Vanta; BSI; PECB; Latham & Watkins; K&L Gates; Morrison Foerster.*
