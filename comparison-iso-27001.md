# ISO/IEC 42001 vs ISO/IEC 27001: reuse and savings

> 🇷🇺 [Читать на русском](./ru/comparison-iso-27001.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** ISO/IEC 42001 and ISO/IEC 27001 share the Annex SL structure and around **40 % of requirements**. If a company already operates 27001, the path to 42001 shrinks by an estimated **40–60 %** (consulting/CB figures, not audited benchmarks). The marginal cost of bolt-on 42001 to an existing 27001 — **$25–60 K in year 1** vs. $60–150 K from scratch. An Integrated Management System (IMS) adds another 30 % via a shared risk register, SoA, internal audit program, and management review.

---

## Contents

- [1. Structural comparison](#1-structural-comparison)
- [2. Reused 100 %](#2-reused-100)
- [3. Reused partially](#3-reused-partially)
- [4. Added new](#4-added-new)
- [5. Annex A: 93 controls of 27001 vs 38 controls of 42001](#5-annex-a-93-controls-of-27001-vs-38-controls-of-42001)
- [6. Combined audit and Integrated Management System](#6-combined-audit-and-integrated-management-system)
- [7. Routes from different starting points](#7-routes-from-different-starting-points)

---

## 1. Structural comparison

| Parameter | ISO/IEC 27001:2022 | ISO/IEC 42001:2023 |
|-----------|---------------------|---------------------|
| Focus | Information security | AI system management |
| Object of protection | Information assets (CIA) | AI systems and their impact |
| Annex A | 93 controls in 4 themes | 38 controls in 9 areas |
| Statement of Applicability | Yes | Yes |
| Risk assessment | Information risks | AI risks + AISIA |
| Unique elements | Vulnerabilities, cryptography | Model drift, bias, human-in-the-loop |
| PDCA cycle | Yes | Yes |
| Annex SL | Yes | Yes |
| Normative reference | ISO/IEC 27000 (terminology) | ISO/IEC 22989 (terminology) |
| Guidance standard | ISO/IEC 27002 (controls guidance) | Annex B of 42001 (controls guidance, embedded) |
| Certificate validity | 3 years | 3 years |

---

## 2. Reused 100%

These processes and artefacts carry over without change:

- **Document and record control** (clause 7.5). Procedures, templates, versioning, retention.
- **Internal audit** (clause 9.2). Program, criteria, checklists, reporting.
- **Management review** (clause 9.3). Agenda extends with an AI block; format remains.
- **Nonconformity and corrective action** (clause 10.1). One process for both.
- **Training and awareness** (clauses 7.2, 7.3). LMS, awareness program format.
- **Communication** (clause 7.4). Channels, RACI matrix.
- **Change management** (clause 6.3). One process.

---

## 3. Reused partially

- **Risk management.** Methodology (likelihood × consequence, scale) carries over. Risk objects and taxonomy differ. For 42001 you add an AI risk register separately (or an AI section in the existing one).
- **Supplier management.** Contracts and due-diligence process carry over. For AI vendors (OpenAI, Anthropic, Google Cloud) you add specific items: DPA with no-training opt-out, provider AI Policy, AI incident notification.
- **Incident management.** Base process carries over. For AI you add a separate classification (see [`templates/ai-incident-response.md`](./templates/ai-incident-response.md)).
- **Asset management.** 27001 information asset register expands to an AI system register with extra fields (see [`templates/ai-system-card.md`](./templates/ai-system-card.md)).

---

## 4. Added new

Elements absent in 27001 that require fresh work:

### AI Policy (control A.2.2)

A separate document. Linked to the Information Security Policy via cross-references, not duplicating it.

### AI systems register (control A.4.2)

Not covered by the 27001 information asset register. Specific fields: model version, data source, license, owner, human oversight level, AISIA status.

### AI System Impact Assessment (controls A.5.2–A.5.5)

No 27001 analogue. Entirely new methodology per ISO/IEC 42005:2025. Details — [`iso-42005-impact-assessment-guide.md`](./iso-42005-impact-assessment-guide.md).

### AI system lifecycle (controls A.6.1.1–A.6.2.8)

10 controls. Covers design objectives, responsible-development objectives, V&V, deployment, operation, monitoring, technical documentation, event logging. 27001 covers these partially via A.8 Asset management and A.14 System acquisition / development / maintenance (old numbering), without AI specifics.

### Data for AI systems (controls A.7.2–A.7.6)

Data quality, lineage, provenance, preparation. 27001 covers only access control and confidentiality.

### Human oversight levels (control A.6.1.2 + Clause 7)

Human-in-the-loop, human-on-the-loop, human-in-command. A new concept absent in 27001.

---

## 5. Annex A: 93 controls of 27001 vs 38 controls of 42001

ISO 27001:2022 Annex A (post-2022 reform):

- **A.5** Organizational controls (37 controls)
- **A.6** People controls (8)
- **A.7** Physical controls (14)
- **A.8** Technological controls (34)

ISO 42001:2023 Annex A:

- **A.2** Policies (3)
- **A.3** Internal organization (2)
- **A.4** Resources (5)
- **A.5** Impact assessment (4)
- **A.6** Lifecycle (10)
- **A.7** Data (5)
- **A.8** Stakeholder information (4)
- **A.9** Use (3)
- **A.10** Third parties (3)

**Overlap (examples):**

| 27001 | 42001 | Common ground |
|-------|--------|---------------|
| A.5.1 Policies | A.2.2 AI Policy | Policy structure, approval, review |
| A.5.2 Information security roles | A.3.2 Roles | Roles, RACI |
| A.5.13 Labelling of information | A.7.3 Data sources | Data categorization |
| A.5.19 Supplier management | A.10.3 Suppliers | Due diligence, contracts |
| A.5.23 Cloud services | A.4.5 Compute resources | Cloud infrastructure |
| A.5.24 Incident management | A.8.4 AI incident | Base response process |
| A.5.30 ICT continuity | A.6.2.6 Operation | Availability |
| A.5.32 Intellectual property rights | A.7.3 Data licenses | Data licensing |
| A.6.3 Awareness | Clause 7.3 | Training and awareness |
| A.8.32 Change management | Clause 6.3, A.6.2.5 | Change control |

About **40 % of 27001 controls** are reflected in 42001. About **50 % of 42001 controls** are reflected in 27001.

---

## 6. Combined audit and Integrated Management System

### Combined audit

CBs can audit 27001 + 42001 simultaneously — 30–50 % cheaper than two separate audits. Conditions:

- One CB accredited for both standards.
- One scope statement combining both.
- One Statement of Applicability tagging controls as 27001 + 42001.
- One risk register split into information risks and AI risks.

CBs active in combined audit: BSI, Schellman, A-LIGN, DNV, Coalfire.

### Integrated Management System (IMS)

IMS is an internal process organization, not a certificate. Idea: a common process foundation on which standard-specific requirements stack.

**IMS architecture for 27001 + 42001:**

- One Information & AI Governance Council.
- Shared risk register with categories: information / AI / privacy.
- Shared internal audit program.
- Shared management review with an AI agenda block.
- Shared document control policy.
- Shared supplier management process.
- Separate top-level policies (Information Security Policy + AI Policy).
- Separate SoAs per standard.

**IMS savings** (per DQS, ISMS.online): 30 %+ reduction in compliance team load at steady state.

More in [`integrated-management-system.md`](./integrated-management-system.md).

---

## 7. Routes from different starting points

### 27001 in place, no AIMS

**Goal:** add AIMS, minimise cost.

- Month 1: gap analysis + AIMS scope statement.
- Month 2: AI Policy, AI risk register, AI systems register.
- Month 3: AISIA for high-risk systems, Annex A controls, SoA.
- Month 4: internal audit, remediation.
- Month 5–6: combined Stage 1 + Stage 2.

**Budget:** $25–60 K in year 1. 3-year TCO $80–160 K.

### No 27001 and no AIMS

**Goal:** start both at once.

- Month 1–2: shared context, AI Policy + Information Security Policy.
- Month 3–5: both risk registers, both control registers.
- Month 6–9: AISIA, V&V, technical controls.
- Month 10–12: internal audit, remediation.
- Month 13–18: combined Stage 1 + Stage 2.

**Budget:** $200–325 K over 3 years.

### SOC 2 in place, no 27001 and no AIMS

See [`comparison-soc2.md`](./comparison-soc2.md).

---

## Need help with the 27001 → 42001 route?

> 📩 **Free 15-minute consultation in Telegram**
> We assess your current compliance map and propose the minimum path to 42001 reusing existing processes.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [ISO/IEC 42001 structure](./structure.md)
- [Integrated Management System (Annex D mapping)](./integrated-management-system.md)
- [Cost and timeline](./cost-timeline.md)
- [SOC 2 comparison](./comparison-soc2.md)

---

*Sources: ISO/IEC 27001:2022; ISO/IEC 27002:2022; ISO/IEC 42001:2023 Annex D; BSI Combined Audit Guide; DQS Integrated Management System Practice; ISMS.online; Schellman; A-LIGN; CertBetter; Reconn; Glocert; Cycore.*
