# ISO/IEC 42001:2023 structure

> 🇷🇺 [Читать на русском](./ru/structure.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** ISO/IEC 42001 is built on Annex SL High-Level Structure (like ISO 27001, ISO 9001, ISO 13485). 10 requirement clauses, PDCA cycle, four annexes (Annex A normative, B/C/D informative). The only normative reference is ISO/IEC 22989:2022 (terminology). Annex B provides per-control guidance.

---

## Contents

- [1. Annex SL and overall architecture](#1-annex-sl-and-overall-architecture)
- [2. 10 requirement clauses](#2-10-requirement-clauses)
- [3. PDCA cycle in AIMS](#3-pdca-cycle-in-aims)
- [4. Annex A — 38 normative controls](#4-annex-a--38-normative-controls)
- [5. Annex B — guidance](#5-annex-b--guidance)
- [6. Annex C — 11 objectives and risk sources](#6-annex-c--11-objectives-and-risk-sources)
- [7. Annex D — integration with other standards](#7-annex-d--integration-with-other-standards)
- [8. Normative and informative references](#8-normative-and-informative-references)

---

## 1. Annex SL and overall architecture

Annex SL is the High-Level Structure (HLS) ISO applies to all modern management system standards. It allows multiple standards to integrate in one organization with minimum duplication.

Standards on the same HLS:
- ISO 9001 (quality)
- ISO 14001 (environment)
- ISO 27001 (information security)
- ISO 27701 (privacy)
- ISO 13485 (medical devices)
- ISO 22301 (business continuity)
- ISO 37301 (compliance)
- ISO/IEC 42001 (AI)

All have clauses 1–3 (introduction), 4–10 (requirements), Annex A (controls).

---

## 2. 10 requirement clauses

| Clause | Title | Requirement |
|--------|--------|--------------|
| 1 | Scope | Description of the standard's scope |
| 2 | Normative references | ISO/IEC 22989:2022 (the only normative reference) |
| 3 | Terms and definitions | Additional terms |
| **4** | **Context of the organization** | External/internal factors (4.1), stakeholders (4.2), AIMS scope (4.3), AIMS as a system (4.4) |
| **5** | **Leadership** | Top-management leadership and commitment (5.1), AI Policy (5.2), roles and responsibilities (5.3) |
| **6** | **Planning** | Risk and opportunity actions (6.1), AI objectives (6.2), change planning (6.3) |
| **7** | **Support** | Resources (7.1), competence (7.2), awareness (7.3), communication (7.4), documented information (7.5) |
| **8** | **Operation** | Operational planning and control (8.1), AI risk assessment (8.2), AI risk treatment (8.3), AI system impact assessment (8.4) |
| **9** | **Performance evaluation** | Monitoring, measurement, analysis, evaluation (9.1), internal audit (9.2), management review (9.3) |
| **10** | **Improvement** | Nonconformities and corrective actions (10.1), continual improvement (10.2) |

Clauses 4–10 are **mandatory** — what the auditor checks. Clauses 1–3 are descriptive.

### 42001-unique subclauses (not in 27001)

- **6.1.4 AI system impact assessment** — mandatory assessment of impact on individuals, groups, society.
- **8.4 AI system impact assessment (operational)** — operational AISIA application.
- **8.3 AI risk treatment** — AI risk treatment separate from risk treatment under 8.2.

---

## 3. PDCA cycle in AIMS

PDCA (Plan-Do-Check-Act) is the foundation of any ISO management system. In 42001:

- **Plan** — clauses 4–7 (context, leadership, planning, support).
- **Do** — clause 8 (operations, including AISIA and risk treatment).
- **Check** — clause 9 (monitoring, internal audit, management review).
- **Act** — clause 10 (nonconformities, corrective actions, improvements).

Certification confirms the cycle is operating, not that you filled in documents once.

---

## 4. Annex A — 38 normative controls

Annex A contains **38 controls** grouped into **9 control objective groups** (A.2–A.10):

| Group | Title | Controls |
|---------|--------|----------|
| **A.2** | AI policies | 3 |
| **A.3** | Internal organization | 2 |
| **A.4** | Resources for AI systems | 5 |
| **A.5** | Impact assessments | 4 |
| **A.6** | AI system lifecycle | 9 |
| **A.7** | Data for AI systems | 5 |
| **A.8** | Information for stakeholders | 4 |
| **A.9** | Use of AI systems | 3 |
| **A.10** | Third parties and customers | 3 |

**Not all 38 controls are mandatory.** Clause 6.1.3 states explicitly: Annex A controls are reference, not exhaustive, not mandatory. The organization runs risk assessment + AISIA → selects controls → documents the **Statement of Applicability (SoA)** with a justification for each: "applicable + how implemented" or "not applicable + justification".

Detailed walkthrough of each control — in [`annex-a-controls.md`](./annex-a-controls.md).

---

## 5. Annex B — guidance

Annex B (informative) provides **practical guidance** for implementing each Annex A control. Its structure mirrors Annex A but adds recommendations, examples, and common pitfalls.

Annex B is especially useful for:
- AIMS leads in the first 3–6 months of implementation.
- Internal auditors building the evidence pack.
- Certifying CBs building the audit plan.

---

## 6. Annex C — 11 objectives and risk sources

Annex C (informative) defines **11 organizational objectives** for assessing AIMS maturity:

1. Accountability
2. AI expertise
3. Availability and quality of training data
4. Environmental impact
5. Fairness
6. Maintainability
7. Privacy
8. Robustness
9. Safety
10. Security
11. Transparency and explainability

Plus a taxonomy of **AI-specific risk sources** (~19 categories): operating environment complexity, model opacity, data drift, adversarial impacts, hardware issues, system failure, reproducibility, etc.

Annex C is inspired by Annex A and B of ISO/IEC 23894.

---

## 7. Annex D — integration with other standards

Annex D (informative) shows **mapping** of ISO/IEC 42001 to other ISO standards:

- ISO 9001 (quality)
- ISO/IEC 27001 (information security)
- ISO 31000 (risk management)
- ISO 37301 (compliance)

This is the foundation for an **Integrated Management System (IMS)** covering multiple standards. More in [`integrated-management-system.md`](./integrated-management-system.md).

---

## 8. Normative and informative references

### Normative reference (the only one)

**ISO/IEC 22989:2022** "Artificial intelligence concepts and terminology" — for all terms and definitions (roles, lifecycle, trustworthiness properties).

### Informative references (bibliography)

- **ISO/IEC 23053:2022** — Framework for AI Systems Using ML.
- **ISO/IEC 23894:2023** — Guidance on risk management.
- **ISO/IEC TR 24028:2020** — Overview of trustworthiness in AI.
- **ISO/IEC TR 24029-1:2021** + **ISO/IEC 24029-2:2023** — Robustness of neural networks.
- **ISO/IEC 5338:2023** — AI system life cycle processes.
- **ISO/IEC 5339:2024** — Guidance for AI applications.

After ISO/IEC 42001 was published, new standards appeared that are not in the bibliography but materially complement 42001:
- **ISO/IEC 42005:2025** — AI System Impact Assessment.
- **ISO/IEC 42006:2025** — Requirements for CBs auditing AIMS.

More in [`family-of-standards.md`](./family-of-standards.md).

---

## Read next

- [Standard overview (42001)](./README.md)
- [ISO/IEC AI family of standards](./family-of-standards.md)
- [Glossary](./glossary.md)
- [Annex A — 38 controls](./annex-a-controls.md)
- [Readiness checklist](./checklist.md)

---

*Sources: ISO/IEC 42001:2023; ISO/IEC 22989:2022; ISO/IEC 23053:2022; ISO/IEC 23894:2023; ISO/IEC 42005:2025; ISO/IEC 42006:2025; ISO/IEC TR 24028:2020; ISO/IEC TR 24029-1:2021; ISO/IEC 24029-2:2023; ISO/IEC 5338:2023; ISO/IEC 5339:2024; Annex SL ISO/IEC Directives Part 1; ITEH ISO/IEC 42001 preview; ISMS.online; risk3sixty; KPMG; Oxebridge.*
