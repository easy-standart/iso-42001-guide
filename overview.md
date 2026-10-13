# ISO/IEC 42001:2023 — Standard Overview

> 🇷🇺 [Читать на русском](./ru/overview.md) · ⬅ [Back to home](./README.md)

> **TL;DR.** ISO/IEC 42001:2023 is the world's first certifiable management system standard for artificial intelligence (AI Management System, AIMS). It does not impose technical requirements on models. It builds a management system around AI: policies, accountabilities, risk and impact assessment, lifecycle controls, documentation, audit. Since December 2023 it has become a de-facto requirement in Microsoft's supply chain, EU AI Act compliance work, Fortune 500 procurement, and several US states.

---

## Contents

- [1. What ISO/IEC 42001 is](#1-what-isoiec-42001-is)
- [2. Why now](#2-why-now)
- [3. Who needs the certificate](#3-who-needs-the-certificate)
- [4. Standard structure](#4-standard-structure)
- [5. Unique requirements](#5-unique-requirements)
- [6. Annex A — 9 areas, 38 controls](#6-annex-a--9-areas-38-controls)
- [7. How it differs from ISO/IEC 27001](#7-how-it-differs-from-isoiec-27001)
- [8. Path to certification](#8-path-to-certification)
- [9. Where to start](#9-where-to-start)

---

## 1. What ISO/IEC 42001 is

ISO/IEC 42001:2023 "Information technology — Artificial intelligence — Management system" was published on 18 December 2023. It is the first international management system standard built specifically for AI. Earlier frameworks (NIST AI RMF, EU AI Act precursors) existed as guidance, but none was certifiable.

**Core idea**: the standard does not prescribe which models you can train or which algorithms you can deploy. It prescribes **how an organization must manage AI**: knowing which AI systems exist, who is accountable for them, what happens when they fail, and how to manage that systematically.

In CEO language: ISO/IEC 42001 turns chaotic AI usage into a managed, transparent system. An auditor can come and verify it — and that verification has international recognition.

The standard is built on **Annex SL**, the harmonized structure shared with ISO 27001, ISO 9001, ISO 13485. That means: 10 clauses of requirements, the PDCA cycle (Plan-Do-Check-Act), Statement of Applicability, risk assessment, Annex A controls. If you have worked with any of these standards, the architecture is familiar.

---

## 2. Why now

The story of ISO/IEC 27001 is repeating itself. Faster.

### Microsoft is already requiring it

In September 2024, Microsoft released a preview of the 10th version of its **Supplier Security and Privacy Assurance (SSPA) Data Protection Requirements (DPR)**. Effective from 2025, it applies to all suppliers.

The headline change: **18 new requirements for AI system management**. If a supplier uses AI in services delivered to Microsoft, they must:

1. Declare in their SSPA profile that the service uses AI systems.
2. Pass an independent conformity assessment via a Microsoft-preferred auditor **or** provide an ISO/IEC 42001 certificate.

If the AI service falls under the **Sensitive Use** definition — ISO/IEC 42001 becomes mandatory. Sensitive Use covers services that influence hiring, credit, medical diagnosis, law enforcement, access to education or government services.

Without meeting these requirements, Microsoft does not issue a Purchase Order. The contract effectively does not start.

### Hyperscalers are already certified

| Company | Date | Scope |
|---------|------|-------|
| Amazon (AWS) | November 2024 | Bedrock, Q Business, Textract |
| Google Cloud | December 2024 | Vertex AI, Gemini, Document AI |
| Anthropic | January 2025 | Claude (API, Enterprise) |
| Microsoft | March 2025 | Microsoft 365 Copilot |
| IBM | September 2025 | Granite (open-source models) |
| KPMG International | December 2025 | Global structure |

First the large players certify. Then they require certification from suppliers. The cascade is already running.

### Regulators are referencing it

- **EU AI Act** (Regulation 2024/1689) entered into force in 2024 with phased application through 2027. ISO/IEC 42001 covers an estimated 40–50 % of its organizational requirements (risk management, documentation, monitoring). The certificate substantially reduces compliance work.
- **Colorado AI Act** (SB 205) explicitly references ISO/IEC 42001 as a benchmark control framework.

### Window of opportunity

By early 2026 about 40 organizations worldwide hold the certificate. In 12–18 months that will be hundreds, then thousands. Companies that start now land in the first cohort and gain a measurable advantage in enterprise sales.

---

## 3. Who needs the certificate

The standard applies to any organization that develops, provides, or uses AI systems. Certification is a priority for those who:

- **Supply** Microsoft, AWS, Google Cloud, Salesforce, Oracle, ServiceNow and other hyperscalers with AI-enabled features
- **Export** AI-powered SaaS to the EU
- **Sell to enterprise customers** with formal compliance requirements
- **Run AI in FinTech**: credit scoring, AML/KYC, fraud detection
- **HR-tech with AI**: sourcing, screening, performance assessment automation
- **HealthTech with AI**: diagnostics, image analysis, prediction (paired with HIPAA, ISO 13485, MDR, FDA SaMD guidance)
- **E-commerce and retail**: recommender systems, dynamic pricing
- **Internal corporate AI** in HR, legal, finance — especially under sector regulation
- **IT startups** planning to enter markets with mandatory AI compliance

In practice, any company that wants to stand out, answer enterprise security questionnaires about AI without long negotiations, and close contracts with large buyers cleanly.

---

## 4. Standard structure

ISO/IEC 42001 follows Annex SL, the shared structure of all modern ISO management standards.

### 10 clauses of requirements

| Clause | What is required | Key question for the CEO |
|--------|------------------|-------------------------|
| 4. Context of the organization | Know where AI exists in your organization and who it affects | How many AI systems are you actually using? |
| 5. Leadership | Top management is personally accountable for AI governance | Who signs the AI Policy? |
| 6. Planning | Formal risk assessment and objective setting | What happens to the business if your model starts discriminating? |
| 7. Support | People, budget, skills, documentation | Does the team have AI governance competence? |
| 8. Operation | Lifecycle controls at every stage | How do you monitor model drift? |
| 9. Performance evaluation | Regular internal and external audits | When did you last review an AI system? |
| 10. Improvement | Response cycle for nonconformities and incidents | Do you have an AI incident response process? |

Clauses 1–3 are normative references and terms — no requirements.

### PDCA cycle

Plan → Do → Check → Act. A management system is not a one-off implementation but a continuous cycle. The certificate confirms the cycle is operating, not that you filled in documents once.

### Annexes

- **Annex A** (normative) — 38 controls in 9 areas. Equivalent of Annex A in ISO 27001.
- **Annex B** (informative) — implementation guidance for each control.
- **Annex C** (informative) — 11 organizational objectives for assessing AI maturity: accountability, expertise, data quality, environmental impact, fairness, maintainability, privacy, robustness, safety, security, transparency.
- **Annex D** (informative) — sector and domain application guidance.

---

## 5. Unique requirements

ISO/IEC 42001 introduces several elements new to the ISO management family.

### AI System Impact Assessment

This is **not classical business risk assessment**. It analyses the consequences of AI operation for individuals and society. You must evaluate:

- Whom the AI may harm (individuals, groups, society, environment)
- How — discrimination, opacity, wrong decisions, downstream effects
- Not only intended use but **foreseeable misuse**

Auditors verify both the process and the documented outputs. The detailed methodology is the subject of a companion standard, ISO/IEC 42005:2025.

### Three levels of human oversight

ISO/IEC 42001 requires appropriate human oversight of AI systems; the three named modes below are a common industry framing for how much control a human keeps, not a taxonomy fixed by the standard:

1. **Human-in-the-loop** — a human makes the final decision; AI only recommends.
2. **Human-on-the-loop** — AI decides automatically; a human observes and can intervene.
3. **Human-in-command** — AI operates autonomously, but a human can shut the system down at any time.

The level depends on the system's risk profile. For higher-risk or Sensitive Use cases, in-the-loop is common.

### Data provenance and lineage

The standard demands traceability of data: source, license, quality, transformations, access history. In practice this means a dataset register and data-lineage documentation — most companies do not have this in place.

### Carbon footprint awareness

Annex C recommends accounting for the carbon footprint of training and operating models. Not strictly required for certification, but increasingly requested by ESG audits and enterprise buyers.

---

## 6. Annex A — 9 areas, 38 controls

| Area | Controls | Subject |
|------|----------|---------|
| **A.2** AI policies | 3 | AI Policy, alignment with other policies, periodic review |
| **A.3** Internal organization | 2 | Roles and responsibilities, problem reporting channel |
| **A.4** Resources for AI systems | 5 | Inventory of models, data, tooling, infrastructure, people |
| **A.5** Impact assessments | 4 | Process, documentation, individual impact, societal impact |
| **A.6** AI system lifecycle | 9 | Design through retirement: requirements, development, V&V, deployment, monitoring, documentation, logging |
| **A.7** Data for AI systems | 5 | Requirements, collection, quality, provenance, preparation |
| **A.8** Information for stakeholders | 4 | User documentation, external reporting, incidents, information for affected parties |
| **A.9** Use of AI systems | 3 | Responsible use processes, objectives, intended use |
| **A.10** Third parties and customers | 3 | Allocation of responsibilities with suppliers and customers |

For each control the organization determines applicability and justifies it in the **Statement of Applicability (SoA)** — the first document an auditor will review.

A detailed walkthrough of all 38 controls with examples and common findings is in [annex-a-controls.md](./annex-a-controls.md).

---

## 7. How it differs from ISO/IEC 27001

If you already hold ISO/IEC 27001, the path to 42001 is 40–60 % shorter. The two standards share the Annex SL structure, and roughly 40 % of requirements overlap directly.

| Parameter | ISO/IEC 27001 | ISO/IEC 42001 |
|-----------|---------------|----------------|
| Focus | Information security | AI system management |
| Object of protection | Information assets (CIA triad) | AI systems and their impact |
| Annex A | 93 controls in 4 themes | 38 controls in 9 areas |
| Statement of Applicability | Yes | Yes |
| Risk assessment | Information risks | AI risks + impact assessment |
| Unique elements | Vulnerability management, cryptography | Model drift, bias, human-in-the-loop |
| PDCA cycle | Yes | Yes |
| Annex SL structure | Yes | Yes |

What carries over:
- Policy management
- Risk management methodology (objects differ)
- Document and records control
- Internal audit
- Management review
- Supplier management
- Incident management
- Awareness and training

What is added new:
- AI Policy and alignment with other policies
- AI systems, models, datasets register
- AI System Impact Assessment
- AI lifecycle controls (10 controls in A.6)
- Human oversight levels
- Data provenance and lineage documentation

A detailed comparison is in [comparison-iso-27001.md](./comparison-iso-27001.md).

---

## 8. Path to certification

### Timeline

Typical range — 3 to 12 months from start to Stage 2 audit.

| Company | Time | Comment |
|---------|------|---------|
| IBM Granite | < 3 months | Mature 27001 program, narrow scope |
| KPMG Australia | 8 months | Global corporation |
| Darktrace | 11 months | Full product coverage |
| Synthesia | ~6 months | SaaS, ISO 27001 baseline |

The biggest accelerator is having ISO/IEC 27001. You reuse the management system, documentation, and audit processes.

### Cost

For a typical 50-person SaaS business with an existing ISO/IEC 27001:

- **With ISO/IEC 27001:** $80–160 K over the first 3 years with a narrow scope.
- **Without ISO/IEC 27001:** $200–325 K, and 12–18 months to first certificate.

Cost lines include: gap analysis, consulting, internal team time, Stage 1 + Stage 2 audit, surveillance audits in years 2 and 3. Detailed breakdown in [cost-timeline.md](./cost-timeline.md).

### Validity

3 years, like other ISO certificates. Surveillance audits in years 2 and 3. Recertification after year 3.

---

## 9. Where to start

Three steps in order:

1. **Assess readiness via the checklist** → [`checklist.md`](./checklist.md)
   You get an honest snapshot: how much work is actually ahead. Do not be discouraged by a low score — that is the norm.

2. **Read the executive FAQ** → [`faq.md`](./faq.md)
   Cost, timeline, headcount, scope, risks. CEO and investor questions need precise answers.

3. **Define a narrow scope for the first certificate.**
   Certifying the entire company at once is almost always a bad idea. Start with one product or one BU. Expand later. That is what everyone does, including Microsoft (separate certificates for M365 Copilot, Azure AI Foundry, Copilot Studio, GitHub Copilot).

---

## Need help putting this in motion?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss your situation: where to start, how to scope, how much time and budget you'll actually need.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Readiness checklist](./checklist.md)
- [Executive FAQ](./faq.md)
- [Standard structure in detail](./structure.md)
- [Annex A controls walkthrough](./annex-a-controls.md)
- [EU AI Act comparison](./comparison-eu-ai-act.md)
- [ISO/IEC 27001 comparison](./comparison-iso-27001.md)
---

*Sources: ISO/IEC 42001:2023; Microsoft SSPA DPR v10 (September 2024); EU AI Act 2024/1689; Colorado SB 205; press releases from AWS, Google Cloud, Anthropic, Microsoft, IBM, KPMG.*
