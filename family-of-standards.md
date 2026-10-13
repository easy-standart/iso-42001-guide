# ISO/IEC AI family of standards

> 🇷🇺 [Читать на русском](./ru/family-of-standards.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** ISO/IEC 42001 is not a lone standard but the core of an ecosystem of 35+ published standards from **ISO/IEC JTC 1/SC 42**. Six of them directly complement 42001: 22989 (terminology, normative reference), 23053 (ML framework), 23894 (risk management), 42005 (impact assessment), 42006 (CB requirements), 5338 (lifecycle processes). Knowing the family saves implementation time and helps build the SoA correctly.

---

## Contents

- [1. ISO/IEC JTC 1/SC 42](#1-isoiec-jtc-1sc-42)
- [2. Six key standards](#2-six-key-standards)
- [3. Other related standards](#3-other-related-standards)
- [4. Normative status of references in 42001](#4-normative-status-of-references-in-42001)
- [5. What was published in 2025](#5-what-was-published-in-2025)

---

## 1. ISO/IEC JTC 1/SC 42

Subcommittee **SC 42 "Artificial intelligence"** was established in 2017 as the first horizontal SC in ISO/IEC JTC 1 ("Information technology"). By early 2026 SC 42 has >35 published standards and dozens in development.

Working Groups:
- **WG 1** — Foundational standards.
- **WG 2** — Data.
- **WG 3** — Trustworthiness.
- **WG 4** — Use cases and applications.
- **WG 5** — Computational approaches and characteristics.

Adjacent SCs with overlaps: SC 27 (security), SC 38 (cloud), SC 41 (IoT).

---

## 2. Six key standards

### ISO/IEC 22989:2022 — AI concepts and terminology

- 60 pages. Published July 2022.
- **The only normative reference in ISO/IEC 42001.**
- Sections: AI concepts (5), AI system life cycle (6, 8 phases), AI ecosystem (7), application areas (8).
- **Trustworthiness properties (§5.15):** transparency, explainability, controllability, robustness, reliability, resilience, accuracy, safety, security, privacy.
- **Roles (§5.19):** AI provider, AI producer, AI customer, AI partner, AI subject, AI relevant authority.
- Amendment **DAmd 1 "Generative AI"** is at Close of voting (document 88145) — GenAI terminology will be added as a separate amendment.

### ISO/IEC 23053:2022 — Framework for AI Systems Using ML

- 36 pages. Published June 2022.
- ML pipeline: task definition → data acquisition → processing → model training → V&V → deployment → operation.
- ML types: supervised, unsupervised, semi-supervised, reinforcement, transfer learning.
- Neural networks and their kinds.
- Amendment **DAmd 1 "Generative AI"** at Close of voting.

### ISO/IEC 23894:2023 — Guidance on risk management

- Published February 2023. Adopted in Europe as **EN ISO/IEC 23894:2024**.
- Mirrors ISO 31000:2018 structure.
- **Annex A** — objectives relevant to AI (value, ethics, performance, trustworthiness).
- **Annex B** — catalogue of AI-specific risk sources (~19 categories): environment complexity, model opacity, data drift, adversarial impacts, hardware issues, system failure, reproducibility.
- **Annex C** — risk management process mapping to lifecycle phases.
- Recommended in 42001 for clauses 6.1 and 8.2.

### ISO/IEC 42005:2025 — AI System Impact Assessment

- 39 pages. Published by ISO/IEC in 2025 (sources cite April–May 2025).
- **The first international standard dedicated to AISIA.**
- 10-step process: scope definition → roles & responsibility → thresholds → execution → analysis → documentation → oversight → monitoring → integration into AIMS → update.
- **Annex A** — mapping to ISO/IEC 42001 (Clause 6.1.4, 8.4, Annex A.5, Annex B.5).
- **Annex B** — relationship with ISO/IEC 23894.
- **Annex C** — taxonomy of potential harm and benefit, templates.
- Harmonised with Canada AIA and NIST AI RMF functions.
- Can be used as "due diligence evidence" for **EU AI Act Article 27 (FRIA)**.

Detailed guide to 42005 — [`iso-42005-impact-assessment-guide.md`](./iso-42005-impact-assessment-guide.md).

### ISO/IEC 42006:2025 — Requirements for AIMS CBs

- Published by ISO/IEC on **7 July 2025** (the BS ISO/IEC 42006:2025 edition, ISBN 978 0 539 26262 9, is dated 31 July 2025).
- Counterpart of ISO/IEC 27006 (for 27001 CBs) but for AIMS.
- Complements ISO/IEC 17021-1 with: auditor competence, coverage of all Annex A controls, certification decision criteria, certification maintenance.
- **Before 42006, the 42001 certification market operated without a unified accreditation standard.** Microsoft, Synthesia and others were certified in 2024 without 42006.
- 42006 closes the gap, increasing trust in certificates.

### ISO/IEC 5338:2023 — AI system life cycle processes

- Published December 2023.
- Defines 30+ AI system lifecycle processes (requirements, development, V&V, operations, retirement).
- Aligned with ISO/IEC/IEEE 15288 (system life cycle).
- Informative reference (bibliography) in 42001.

---

## 3. Other related standards

| Standard | Purpose | Status | Year |
|----------|---------|---------|------|
| **ISO/IEC TR 24028:2020** | Overview of trustworthiness in AI | Published (TR) | 2020 |
| **ISO/IEC TR 24029-1:2021** | Robustness of neural networks — Part 1: Overview | Published (TR) | 2021 |
| **ISO/IEC 24029-2:2023** | Part 2: Formal methods | Published | 2023 |
| **ISO/IEC 5339:2024** | Guidance for AI applications | Published | 2024 |
| **ISO/IEC 5259-1...5:2024–2025** | Data quality for analytics and ML | Various | 2024–2025 |
| **ISO/IEC 12792** | Transparency taxonomy | Published | 2025 |
| **ISO/IEC TS 6254** | Methods of explainability | Published (TS) | 2025 |
| **ISO/IEC TR 20226** | Environmental sustainability | Published (TR) | 2025 |
| **ISO/IEC 42007** | Conformity assessment schemes | In development | 2026 expected |

### Trustworthiness standards (via WG 3)

ISO/IEC TR 24028:2020 defines **trustworthiness** as "the ability to meet stakeholder expectations in a verifiable way" and lists properties: reliability, robustness, safety, security, privacy, transparency, fairness, accountability.

ISO/IEC TR 24029-1/2 — neural-network robustness assessment methods: statistical, formal, and empirical.

---

## 4. Normative status of references in 42001

| Standard | Status in 42001 |
|----------|-----------------|
| ISO/IEC 22989:2022 | Normative reference (Section 2) |
| ISO/IEC 23053:2022 | Bibliography (informative) |
| ISO/IEC 23894:2023 | Bibliography (informative) |
| ISO/IEC TR 24028:2020 | Bibliography (informative) |
| ISO/IEC TR 24029-1:2021 | Bibliography (informative) |
| ISO/IEC 24029-2:2023 | Bibliography (informative) |
| ISO/IEC 5338:2023 | Bibliography (informative) |
| ISO/IEC 5339:2024 | Bibliography (informative) |
| ISO/IEC 42005:2025 | Not in bibliography (published after 42001), but 42005 itself references 42001 |
| ISO/IEC 42006:2025 | Not in bibliography; 42006 references 42001 |

**Only 22989 is mandatory.** All others are recommended, not required for certification. In practice, auditors expect you to use 23894 (risks) and 42005 (impact assessment) as the methodology base.

---

## 5. What was published in 2025

2025 marked an inflection point for the family:

- **ISO/IEC 42005:2025** — AI System Impact Assessment (May/June).
- **ISO/IEC 42006:2025** — CB requirements (31 July).
- **ISO/IEC 12792** — Transparency taxonomy.
- **ISO/IEC TS 6254** — Methods of explainability.
- **ISO/IEC TR 20226** — Environmental sustainability.
- **ISO/IEC 42007** (in development) — Conformity assessment schemes.

All complement ISO/IEC 42001, none replace it. In 12–18 months some are expected to enter the updated 42001 bibliography at the next systematic review (planned 2028).

---

## Read next

- [ISO/IEC 42001 structure](./structure.md)
- [Glossary](./glossary.md)
- [ISO 42005 Impact Assessment guide](./iso-42005-impact-assessment-guide.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)

---

*Sources: ISO/IEC JTC 1/SC 42 standards catalogue; ISO/IEC 22989:2022 (document 74296); ISO/IEC 23053:2022 (74438); ISO/IEC 23894:2023 (77304); ISO/IEC 42005:2025; ISO/IEC 42006:2025 / BS ISO/IEC 42006:2025; ISO/IEC TR 24028:2020; ISO/IEC TR 24029-1:2021; ISO/IEC 24029-2:2023; ISO/IEC 5338:2023; ISO/IEC 5339:2024; ISO/IEC 12792; ISO/IEC TS 6254; ISO/IEC TR 20226; BSI Knowledge; digital.nemko; ITEH; ISMS.online; risk3sixty; KPMG; Oxebridge; CMS Law-Now; Scrut; Prompt Security; libertify; INCITS; AI Standards Hub; verifywise.ai; SAP Community; ANAB.*
