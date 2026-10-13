# ISO/IEC 42001 Annex A: all controls explained

> 🇷🇺 [Читать на русском](./ru/annex-a-controls.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** Annex A of ISO/IEC 42001 is **38 normative controls** across **9 areas** (A.2–A.10). The controls are a reference set — you are not required to implement all of them. You run a risk assessment and an impact assessment (AISIA), select the applicable controls, and record each one in a **Statement of Applicability (SoA)** — "applicable + how implemented" or "not applicable + why". Below, for every control: what it requires, what evidence to prepare, who owns it, and where teams most often stumble at audit.

---

## Contents

- [How Annex A works](#how-annex-a-works)
- [A.2 — AI policies](#a2--ai-policies)
- [A.3 — Internal organization](#a3--internal-organization)
- [A.4 — Resources for AI systems](#a4--resources-for-ai-systems)
- [A.5 — Assessing impacts of AI systems](#a5--assessing-impacts-of-ai-systems)
- [A.6 — AI system life cycle](#a6--ai-system-life-cycle)
- [A.7 — Data for AI systems](#a7--data-for-ai-systems)
- [A.8 — Information for interested parties](#a8--information-for-interested-parties)
- [A.9 — Use of AI systems](#a9--use-of-ai-systems)
- [A.10 — Third parties and customers](#a10--third-parties-and-customers)
- [How an auditor checks Annex A controls](#how-an-auditor-checks-annex-a-controls)
- [Statement of Applicability: how to document it](#statement-of-applicability-how-to-document-it)

---

## How Annex A works

Three things to understand before the control-by-control walkthrough.

**Not all controls are mandatory.** Clause 6.1.3 states plainly: Annex A controls are a reference, not an exhaustive list. You start from the risks and impacts of your specific AI systems — you do not implement 38 controls "just in case".

**The selection is captured in the SoA.** For every control, the Statement of Applicability records a decision: applicable (with a reference to how it is implemented) or not applicable (with justification). An empty justification column is the single most common audit finding.

**Annex B tells you how to implement.** Annex A states the control; Annex B (informative) gives practical guidance for each one — recommendations, examples, what to look for. Keep Annex B close during the first months of implementation.

Each area below has a control table. The "Owner · frequency" column is a typical role split and how often evidence is refreshed; yours may differ.

---

## A.2 — AI policies

Top level: a written AI policy, its alignment with the company's other policies, and regular review.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.2.2** AI policy | An AI policy approved by top management and communicated to staff | Signed AI Policy, distribution/attestation log, approval minutes | CAIO / CISO · ≥1×/yr + on change |
| **A.2.3** Alignment with other policies | The AI policy is consistent with ISMS, privacy, ethics; links are described | Mapping "AI Policy ↔ ISMS / Privacy / Ethics", alignment minutes | Head of Compliance · 1×/yr |
| **A.2.4** Review of the AI policy | The policy is reviewed on schedule and when the context changes | Review log, management decisions, next-review date | AIMS Owner · 1×/yr |

---

## A.3 — Internal organization

Who is responsible for what, and how concerns are escalated.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.3.2** Roles and responsibilities | AI roles and authorities are defined and allocated | Org chart, RACI, AI-role job descriptions, AI Governance Board charter | HR + CAIO · on change + 1×/yr |
| **A.3.3** Reporting of concerns | There is a channel to raise concerns about AI systems | AI Steering Committee Terms of Reference, meeting minutes | AI Governance Board · quarterly |

---

## A.4 — Resources for AI systems

The five resource types an AIMS cannot live without: people, data, tooling, compute, budget.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.4.2** Resource documentation | Resources for AI systems are documented and allocated | Resource plan (FTE, budget, compute) approved by top management | CAIO · 1×/yr |
| **A.4.3** Data resources | Data used by systems is inventoried and classified | Data inventory, classification, lineage register | Data Steward · continuous |
| **A.4.4** Tooling resources | Development/operation tools and libraries are inventoried | Tool/library list (MLflow, Evidently, SageMaker), license tracker | MLOps Lead · on change |
| **A.4.5** System and computing resources | Infrastructure is sufficient for development, operation, monitoring | Cloud/infra inventory, capacity plan | CTO · 1×/yr |
| **A.4.6** Human resources | People have the required competencies | Competence matrix, training records | CHRO · 1×/yr |

---

## A.5 — Assessing impacts of AI systems

The block unique to 42001: assessing the impact of an AI system on individuals, groups and society (AISIA). 27001 has nothing like it.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.5.2** Impact assessment process | The AISIA process is defined: when it triggers, by which criteria | AISIA methodology, trigger criteria | AI Ethics Lead · 1×/yr + on change |
| **A.5.3** Documentation of AISIA | Each system has an impact-assessment record | AISIA record per system, with sign-offs | Product Owner · per system |
| **A.5.4** Impact on individuals and groups | Impact on individuals and vulnerable groups is assessed | Demographic impact analysis, bias-testing logs | Ethics + Data Science · per system/release |
| **A.5.5** Societal impact | Society-level risks are assessed (environment, jobs, widespread misuse) | Societal-risk analysis | Ethics Lead · per system |

---

## A.6 — AI system life cycle

The largest area: responsible development from objective-setting to event logging in production.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.6.1.2** Objectives for responsible development | Development objectives are set per system | Development-objectives doc per system | Product Owner · per system |
| **A.6.1.3** Processes for responsible development | Responsible-development "AI gates" are built into the SDLC | SDLC-AI policy, CI/CD gate description | Head of Eng · per release |
| **A.6.2.2** Requirements and specification | Functional requirements for the system are approved | Specifications, change log | PM · per release |
| **A.6.2.3** Design and development | The design is documented, including human oversight | Design docs + HITL/HOTL description | Solution Architect · per release |
| **A.6.2.4** Verification and validation | The system is tested for accuracy, fairness, robustness, adversarial | V&V plan, test reports | QA + ML eng · per release |
| **A.6.2.5** Deployment | Deployment passes a go/no-go control | Deployment checklist, sign-off | MLOps · per release |
| **A.6.2.6** Operation and monitoring | The system is monitored in production (drift, incidents) | Monitoring dashboard, alert logs, incident reports | SRE / MLOps · continuous |
| **A.6.2.7** Technical documentation | Model card, data card, system documentation exist | Model card, data card, system documentation | ML eng · per release |
| **A.6.2.8** Event logging | Inputs/outputs and feedback are logged; decisions are reconstructable | Prod logs (input/output hashes, feedback), retention ≥12 months | MLOps · continuous |

---

## A.7 — Data for AI systems

Data management across the whole path: acquisition, quality, provenance, preparation.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.7.2** Data for development and enhancement | Data requirements for training and fine-tuning are defined | Data governance policy, acquisition records | Data Steward · continuous |
| **A.7.3** Data acquisition | Source and rights to the data are clear | Provenance records, license log | Data Eng · per dataset |
| **A.7.4** Quality of data | Data is measured for completeness, representativeness, bias | Data quality metrics, bias check | Data Steward · per dataset + drift |
| **A.7.5** Data provenance | Data lineage is traceable | Lineage diagrams, DataHub / Collibra export | Data Eng · continuous |
| **A.7.6** Data preparation | Transformations and preprocessing are documented | Preprocessing pipeline docs | ML eng · per version |

---

## A.8 — Information for interested parties

What you communicate, and how, to users, regulators and other parties.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.8.2** Documentation for users | Users understand they interact with AI and how to use it | User guide, transparency notice | Technical Writer · per release |
| **A.8.3** External reporting | There is a process for external disclosure (incl. to the regulator) | Incident disclosure templates (e.g. AI Act Art. 73 for the EU) | Legal + IR · per incident |
| **A.8.4** Communication of incidents | Interested parties are notified of incidents | Incident communications log | Comms + Legal · per incident |
| **A.8.5** Information for interested parties | Stakeholder requirements are captured and reflected | Stakeholder register with their requirements | AIMS Owner · 1×/yr |

---

## A.9 — Use of AI systems

Responsible use: rules for staff, intended use, monitoring of actual use.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.9.2** Processes for responsible use | Acceptable-use rules for AI (incl. external services) exist | Acceptable Use Policy + training records | HR + Security · 1×/yr |
| **A.9.3** Intended use | Each system documents what it is intended for | Intended-use documentation per system | Product Owner · per system |
| **A.9.4** Monitoring of actual use | Real usage is tracked; shadow AI is caught | Usage analytics, anomaly detection | Security / MLOps · continuous |

---

## A.10 — Third parties and customers

Responsibility across the chain: AI suppliers and customer-facing work.

| Control | What it requires | Evidence | Owner · frequency |
|---------|------------------|----------|-------------------|
| **A.10.2** Allocating responsibilities | Responsibility for AI is allocated in supplier contracts | Contracts with AI-addendum, RACI with suppliers | Procurement + Legal · per contract |
| **A.10.3** Suppliers | Suppliers go through due diligence and monitoring | Supplier register, due-diligence questionnaire, SLA, monitoring records | Vendor Manager · onboarding + annual |
| **A.10.4** Customers | Customers understand the AI decision and can contest it | Customer transparency notices, feedback and redress channels | Customer Success · continuous |

---

## How an auditor checks Annex A controls

An auditor does not read your policy — they ask you to show that the control works in practice. Typical Stage 2 questions by area:

- **A.2.2:** "Show me top management's signature and the record of distributing the policy to staff."
- **A.4.3:** "Show me the provenance of training dataset X. What license?"
- **A.5.3:** "Show me the AISIA for a specific AI system Y."
- **A.6.2.3:** "How is HITL/HOTL implemented in the interface?"
- **A.6.2.6:** "Show me the drift metric for the last 30 days."
- **A.6.2.8:** "Can you reconstruct a specific decision the system made, from the logs?"
- **A.9.2:** "What Acceptable Use Policy governs ChatGPT for your staff?"
- **A.10.2:** "Show me the AI-addendum to your contract with OpenAI/Anthropic."

The logic is always the same: a control counts not because a document exists, but because there is evidence that the process is alive.

A detailed walkthrough of the 15 most common nonconformities and how to close them before Stage 2 is in [`common-audit-findings.md`](./common-audit-findings.md).

---

## Statement of Applicability: how to document it

The SoA is the table that links risks to controls. For each of the 38 controls:

1. **Applicable / not applicable** — the decision on the control.
2. **Justification** — why. For applicable ones: which risk it addresses. For not-applicable ones: the risk does not arise / the control is covered another way / an external requirement does not apply.
3. **How implemented** — a reference to the procedure, document or system.
4. **Status** — implemented / in progress / planned.

The most common mistake is an empty justification column for excluded controls. An auditor reads that as "the control was never considered", not "it was deliberately excluded". The justification must be risk-based: not "we don't need it", but "this risk does not arise in our scope, because …".

For a scope template and the link to the impact assessment, see [`checklist.md`](./checklist.md) and [`iso-42005-impact-assessment-guide.md`](./iso-42005-impact-assessment-guide.md).

---

## Need help selecting controls and building the SoA?

> 📩 **Free 15-minute consultation in Telegram**
> We review your AI systems, help you determine the applicable Annex A controls, and build a Statement of Applicability that passes the audit.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [ISO/IEC 42001 structure](./structure.md)
- [Top 15 common audit findings](./common-audit-findings.md)
- [Readiness checklist](./checklist.md)
- [Impact assessment guide (ISO 42005)](./iso-42005-impact-assessment-guide.md)
- [Glossary](./glossary.md)

---

*Sources: ISO/IEC 42001:2023 (Annex A, Annex B); ISO/IEC 42005:2025; ISO/IEC 23894:2023; Schellman; A-LIGN; BSI; risk3sixty; RSI Security; Glocert; Cloud Security Alliance; Sprinto; Vanta; Coalfire; Reconn; EU Commission AI Literacy FAQ.*
