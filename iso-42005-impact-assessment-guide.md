# ISO/IEC 42005:2025 — AI System Impact Assessment Guide

> 🇷🇺 [Читать на русском](./ru/iso-42005-impact-assessment-guide.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** ISO/IEC 42005:2025 was published in April 2025 and closes a practical gap in ISO/IEC 42001: exactly how to perform the **AI System Impact Assessment (AISIA)** required by controls A.5.2–A.5.5. It is not a certifiable standard — it is normative guidance. 42001 auditors rely on 42005 when evaluating Annex A.5. Lacking a documented AISIA process aligned to 42005 is one of the most frequent Stage 2 nonconformities.

---

## Contents

- [1. What 42005 is and why it matters](#1-what-42005-is-and-why-it-matters)
- [2. Mapping to ISO 42001 Annex A.5 controls](#2-mapping-to-iso-42001-annex-a5-controls)
- [3. When to perform an AISIA](#3-when-to-perform-an-aisia)
- [4. Triage: full or simplified assessment](#4-triage-full-or-simplified-assessment)
- [5. AISIA structure: 8 required components](#5-aisia-structure-8-required-components)
- [6. Who performs and who approves](#6-who-performs-and-who-approves)
- [7. Relation to DPIA, HRIA, FRIA](#7-relation-to-dpia-hria-fria)
- [8. Worked example for a typical SaaS](#8-worked-example-for-a-typical-saas)

---

## 1. What 42005 is and why it matters

ISO/IEC 42005:2025 "Information technology — Artificial intelligence (AI) — AI system impact assessment" was published in April 2025. It is **guidance** (not certifiable) and provides the methodology for performing and documenting AISIAs.

**The gap it closes:** before 42005, organisations had control A.5 in 42001 ("assess AI impact on individuals and society") without a method. Auditors at Stage 2 routinely received "we discussed it in a meeting, no risks identified" as documentation. 42005 closes that gap.

**How it differs from classic risk assessment:**
- Risk assessment (Clause 6 in 42001, ISO/IEC 23894) is about risks **to the organisation**.
- AISIA is about consequences of AI operation for **individuals, groups, society, and the environment**.

AISIAs often surface risks the organisation considered acceptable because there was no direct financial damage to it.

---

## 2. Mapping to ISO 42001 Annex A.5 controls

| Control | What 42001 requires | What 42005 adds |
|---------|---------------------|-----------------|
| A.5.2 | A process for impact assessment must exist | Concrete methodology (8 components) |
| A.5.3 | Results must be documented | Document template, review cadence |
| A.5.4 | Assessment of impact on individuals | Methodology at the individual level |
| A.5.5 | Assessment of societal impact | Methodology at the group and societal level |

A 42001 auditor may require 42005 conformance as evidence for control A.5, even though 42005 itself is not certifiable.

---

## 3. When to perform an AISIA

42005 requires AISIAs at **four lifecycle moments**:

1. **Before launching a new AI system** (design phase).
2. **On significant change**: new model, new data, new use case, new market.
3. **On a recurring basis** in operation — at minimum annually for high-risk systems, every 2–3 years for low-risk.
4. **After an incident** that may indicate a missed risk.

Documentation of every AISIA must be retained for the life of the system plus at least 3 years after retirement.

---

## 4. Triage: full or simplified assessment

42005 acknowledges that full AISIAs are not needed for every AI system. The standard introduces **triage** based on risk level:

| Risk level | When it applies | AISIA depth |
|------------|-----------------|-------------|
| **High-risk** | Decisions about people: hiring, credit, healthcare, justice, education access | Full: all 8 components, board-level approval |
| **Medium-risk** | Affects specific groups, non-critical for rights | Simplified: key components, AIMS owner approval |
| **Low-risk** | Internal automation without people-facing effects | Brief: 2–3 pages, product owner approval |
| **Minimal** | Pure automation (e.g., OCR without decisioning) | Recorded in the inventory, no AISIA required |

The triage criteria must be documented in the AISIA policy. It is one of the first artefacts an auditor will ask for.

---

## 5. AISIA structure: 8 required components

A 42005-conformant AISIA must minimally contain:

1. **AI system description.** Purpose, scope, architecture, data, models, version.

2. **Context of use.** Where, by whom, under what conditions. What alternatives exist (what existed before AI).

3. **Stakeholders.** Directly affected (users), indirectly affected (society, environment), beneficiaries.

4. **Impact identification.** Positive and negative. Direct and indirect. Individual and systemic. Including **foreseeable misuse**.

5. **Severity and likelihood assessment.** A scale (typically 1–5 on each axis). Severity covers irreversibility, scale, distribution. Likelihood is based on testing data and analogous systems.

6. **Mitigation measures.** Technical, organisational, informational. Each significant impact gets a specific measure with owner and deadline.

7. **Residual risk.** Post-mitigation. Decision: accept, transfer, continue mitigation, abandon the system.

8. **Monitoring plan.** Metrics, frequency, review triggers, accountable owner.

42005 recommends document length: 5–10 pages for medium-risk, 15–30 pages for high-risk.

---

## 6. Who performs and who approves

42005 requires a **multi-disciplinary team**:

- **AI Product Owner / Project Lead** — runs the assessment.
- **Technical SME (ML lead, data scientist)** — evaluates the technical side.
- **Legal / Compliance / DPO** — evaluates legal risks.
- **Domain expert** — understands the use context (e.g., a clinician for HealthTech).
- **Stakeholder representative** (external or internal) — represents affected parties.

For high-risk systems, 42005 recommends including an **independent external expert** (academic, civil society) at least at the review stage.

**Approval levels:**
- Low-risk — product owner.
- Medium-risk — AIMS owner or CISO.
- High-risk — C-level or board.

Without formal sign-off, the system must not be deployed to production.

---

## 7. Relation to DPIA, HRIA, FRIA

AISIA does not replace other impact assessments but can integrate them into a unified process:

| Assessment | Regulation | What AISIA adds |
|------------|------------|-----------------|
| **DPIA** (Data Protection Impact Assessment) | GDPR Article 35 | AISIA extends to non-privacy impacts (discrimination, manipulation, safety) |
| **HRIA** (Human Rights Impact Assessment) | UN Guiding Principles | AISIA adds technical focus on AI specifics |
| **FRIA** (Fundamental Rights Impact Assessment) | EU AI Act Article 27 for high-risk deployers | AISIA is the base; FRIA adds the European legal framing |
| **ESG / sustainability assessment** | Internal ESG frameworks | AISIA extends to model carbon footprint |

In practice, for high-risk systems, an **integrated assessment** — a single document with sections per required format — works best. It simplifies upkeep and reduces duplication.

---

## 8. Worked example for a typical SaaS

Scenario: a SaaS startup ships an AI resume-screening feature for HR customers.

**Triage:** high-risk (hiring decision = EU AI Act Annex III point 4; NYC Local Law 144; control A.5.4 is especially strict).

**Stakeholders:**
- Direct: candidates, HR managers, hiring managers.
- Indirect: customer companies, society (labour market).
- Indirect negative: groups historically discriminated in hiring.

**Identified impacts (examples):**
- Positive: faster hiring, lower HR workload.
- Negative: discrimination by age / gender / nationality; false negative candidates; reduced transparency to candidates; foreseeable misuse — customer using only the AI score without human review.

**Mitigation measures:**
- Quarterly bias audit on a representative sample.
- Contractual ban on use without human-in-the-loop.
- Transparency: automatic notification to the candidate that AI was used, right to explanation and appeal.
- Logging of all scoring decisions to enable incident review.

**Residual risk:** medium — accept, monitor, review quarterly.

**Monitoring plan:** false-negative rate by demographic group, monthly drift detection, candidate feedback through an open channel.

**Approval:** CEO + CISO + Head of Product.

---

## Downloadable template

An AISIA Markdown template aligned with ISO/IEC 42005:2025 will be added at `templates/ai-impact-assessment.md`.

---

## Need help with your AISIA?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss the right assessment depth for your AI system, what to include in triage, and how to integrate AISIA with DPIA / FRIA.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [AI Impact Assessment template](./templates/ai-impact-assessment.md)
- [ISO/IEC AI family of standards](./family-of-standards.md)
---

*Sources: ISO/IEC 42005:2025 "Information technology — Artificial intelligence (AI) — AI system impact assessment" (April 2025); ISO/IEC 42001:2023 Annex A.5; ISO Responsible AI governance and impact standards package; CMS Law — "ISO/IEC 42005:2025 — A New Blueprint for Legal and Commercial Leaders Navigating AI Risk and Governance"; Nemko Digital — "ISO IEC 42005 AI Impact Assessment Guide 2025".*
