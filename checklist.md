# ISO/IEC 42001 Readiness Checklist

> 🇷🇺 [Читать на русском](./ru/checklist.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** A structured self-assessment against ISO/IEC 42001:2023 requirements. Run it honestly — no one is watching but you. You will get a snapshot: where you are ready, where work lies ahead, where you have not started.
>
> **How to use it.** For each item, mark one of three statuses:
> - ✅ **Done** — document exists, process is operating, you can show it to an auditor
> - 🟡 **Partial** — exists but is not formalized or does not cover the full scope
> - ❌ **No** — does not exist or is not operating
>
> If 70 %+ are ✅ — you are ready for Stage 1. 40–70 % ✅ — you need a gap analysis and 4–6 months of work. < 40 % ✅ — a full implementation project lies ahead.

---

## Contents

- [A. Management requirements (Clauses 4–10)](#a-management-requirements-clauses-410)
  - [4. Context of the organization](#4-context-of-the-organization)
  - [5. Leadership](#5-leadership)
  - [6. Planning](#6-planning)
  - [7. Support](#7-support)
  - [8. Operation](#8-operation)
  - [9. Performance evaluation](#9-performance-evaluation)
  - [10. Improvement](#10-improvement)
- [B. Annex A controls](#b-annex-a-controls)
  - [A.2 AI policies](#a2-ai-policies)
  - [A.3 Internal organization](#a3-internal-organization)
  - [A.4 Resources for AI systems](#a4-resources-for-ai-systems)
  - [A.5 Impact assessments](#a5-impact-assessments)
  - [A.6 AI system lifecycle](#a6-ai-system-lifecycle)
  - [A.7 Data for AI systems](#a7-data-for-ai-systems)
  - [A.8 Information for stakeholders](#a8-information-for-stakeholders)
  - [A.9 Use of AI systems](#a9-use-of-ai-systems)
  - [A.10 Third parties and customers](#a10-third-parties-and-customers)
- [Result interpretation](#result-interpretation)

---

## A. Management requirements (Clauses 4–10)

### 4. Context of the organization

- [ ] **4.1.** Internal and external factors affecting the AIMS are identified and documented (market, regulators, technology, culture).
- [ ] **4.2.** Stakeholders and their requirements regarding AI systems are identified (customers, regulators, employees, society).
- [ ] **4.3.** The **scope** of the AI management system is defined and documented: which AI systems, products, sites, legal entities are included.
- [ ] **4.4.** A register exists covering all AI systems the organization develops, provides, or uses — including third-party API integrations (OpenAI, Anthropic, Google, etc.).
- [ ] **4.5.** The organization's role under ISO/IEC 42001 is defined: AI Producer, AI Provider, AI Customer, AI User, or a combination.

### 5. Leadership

- [ ] **5.1.** Top management demonstrates commitment to the AIMS: AI Policy is signed, budget allocated, owners assigned.
- [ ] **5.2.** An **AI Policy** is approved — a formal document with the organization's principles for AI, available to all employees.
- [ ] **5.3.** The AI Policy is aligned with other corporate policies (security, privacy, ethics, ESG).
- [ ] **5.4.** An AIMS owner is appointed at C-suite level or reporting directly to the CEO (typically CISO, CPO, or a new AI Governance Lead).
- [ ] **5.5.** Roles and responsibilities for the AIMS are defined and documented: AIMS owner, AI system owners, auditor, incident response lead.

### 6. Planning

- [ ] **6.1.** A formal **AI risk assessment** has been performed and documented — separate from classical security risks, focused on model errors, discrimination, drift, hallucinations.
- [ ] **6.2.** Each significant AI system has an **AI System Impact Assessment** scheduled or completed (impact on individuals and society).
- [ ] **6.3.** Measurable AIMS objectives (KPIs) and target dates are defined.
- [ ] **6.4.** Changes to the AIMS are planned for significant events (new model launch, regulatory change, incident).
- [ ] **6.5.** AI risk acceptance criteria and the management approval process are defined.

### 7. Support

- [ ] **7.1.** Sufficient resources (people, budget, infrastructure) are allocated to operate the AIMS.
- [ ] **7.2.** Competence requirements for AIMS roles are defined; competencies are evidenced (training, experience, certifications).
- [ ] **7.3.** Awareness program: employees know the AI Policy, their responsibilities, and the channels for reporting concerns.
- [ ] **7.4.** Internal and external communication channels for AI matters are defined.
- [ ] **7.5.** AIMS documented information is controlled (versioning, access control, currency, archiving).

### 8. Operation

- [ ] **8.1.** Operational planning: AIMS processes are implemented and operating; changes are controlled.
- [ ] **8.2.** AI risk assessment is repeated upon significant changes and at least annually.
- [ ] **8.3.** AI System Impact Assessment is performed before launching every new system and after significant changes.
- [ ] **8.4.** AI risk treatments are defined and applied; their effectiveness is tracked.
- [ ] **8.5.** AI system lifecycle is managed (see A.6 below): from requirements to retirement.

### 9. Performance evaluation

- [ ] **9.1.** AIMS and AI system performance metrics are defined; data is collected regularly.
- [ ] **9.2.** At least one **internal audit** of the AIMS has been performed by an independent person; findings and corrective actions are documented.
- [ ] **9.3.** At least one **management review** has been conducted with minutes and decisions on file.
- [ ] **9.4.** Stakeholder feedback (users, employees, customers) is collected and reviewed.
- [ ] **9.5.** Effectiveness of risk treatments and Annex A controls is analyzed and documented.

### 10. Improvement

- [ ] **10.1.** A documented process exists for handling nonconformities and AI incidents.
- [ ] **10.2.** Corrective actions are taken with root cause analysis.
- [ ] **10.3.** Improvements are made to the AIMS based on audits, incidents, and feedback.
- [ ] **10.4.** An incident register and lessons learned are maintained and accessible to the AIMS team.

---

## B. Annex A controls

38 controls in 9 areas. Each must have its applicability and justification recorded in the **Statement of Applicability (SoA)**.

### A.2 AI policies

- [ ] **A.2.2.** AI Policy is approved with the organization's principles and commitments regarding AI.
- [ ] **A.2.3.** AI Policy does not conflict with other policies (security, privacy, ethics, HR).
- [ ] **A.2.4.** A schedule for periodic AI Policy review is established (at least annually plus on significant changes).

### A.3 Internal organization

- [ ] **A.3.2.** Specific accountabilities are assigned for each AI system and for the AIMS as a whole.
- [ ] **A.3.3.** A working channel exists for employees, users, and third parties to report concerns about AI systems (email, form, anonymous channel).

### A.4 Resources for AI systems

- [ ] **A.4.2.** A maintained **AI system resource register** exists: models, datasets, tools, infrastructure, people.
- [ ] **A.4.3.** Each dataset is documented: source, volume, collection date, categories of personal data, license, restrictions.
- [ ] **A.4.4.** Tooling for development, testing, and deployment of AI systems is documented.
- [ ] **A.4.5.** Compute and infrastructure resources (GPUs, servers, cloud) running models are documented.
- [ ] **A.4.6.** Competence of people working with AI is evidenced (training, experience, evaluation) for every key role.

### A.5 Impact assessments

- [ ] **A.5.2.** A formal **AI System Impact Assessment process** is defined: when to perform it, who performs it, criteria, who approves.
- [ ] **A.5.3.** Impact assessment results are documented and accessible to stakeholders on request.
- [ ] **A.5.4.** Each significant AI system has an assessment of impact on individuals (discrimination, wrong decisions, rights violations).
- [ ] **A.5.5.** Impact on society and the environment is assessed (filter bubbles, manipulation, sustainability, accessibility).

### A.6 AI system lifecycle

- [ ] **A.6.1.1.** Design and development objectives for AI systems are defined and documented.
- [ ] **A.6.1.2.** "Responsible development" objectives are defined (e.g., explainability, robustness, fairness).
- [ ] **A.6.1.3.** Ethics, safety, and fairness criteria are embedded in the development process at each stage.
- [ ] **A.6.2.2.** Each AI system has a formal **specification**: what the system shall do, what it shall not do, acceptance criteria.
- [ ] **A.6.2.3.** Design and development documentation is maintained at all stages: architecture, key decisions, justifications.
- [ ] **A.6.2.4.** **Verification and validation** of AI systems is performed: conformance to specification and fitness for purpose.
- [ ] **A.6.2.5.** Pre-launch a deployment checklist is executed and the system owner approves go-live.
- [ ] **A.6.2.6.** Operating AI systems are continuously monitored: performance, anomalies, **model drift**, feedback.
- [ ] **A.6.2.7.** Each AI system has up-to-date technical documentation, audit-accessible.
- [ ] **A.6.2.8.** **Event logs** for AI systems are maintained; retention is sufficient for incident investigation (90 days minimum, often 1–3 years).

### A.7 Data for AI systems

- [ ] **A.7.2.** Requirements for data used in development and improvement of AI systems are defined.
- [ ] **A.7.3.** All data sources and the legal basis for their use are documented (licenses, consents, contracts).
- [ ] **A.7.4.** Data quality is controlled: accuracy, completeness, currency, representativeness.
- [ ] **A.7.5.** **Data lineage** is tracked: where data came from, how it was transformed, who had access.
- [ ] **A.7.6.** Data preparation processes are documented and reproducible.

### A.8 Information for stakeholders

- [ ] **A.8.2.** AI system documentation is accessible not only to developers but to users and operators.
- [ ] **A.8.3.** External reporting is in place: regulators, customers, society receive timely and accurate information about AI use.
- [ ] **A.8.4.** A documented procedure exists for notifying stakeholders of **AI incidents** (timelines, recipients, channels).
- [ ] **A.8.5.** Affected parties (candidates, customers, patients) receive relevant information about AI system operation and access to explanations or appeals.

### A.9 Use of AI systems

- [ ] **A.9.2.** Responsible-use processes are defined for the organization (what is allowed, what is not, how it is controlled).
- [ ] **A.9.3.** Objectives for AI usage in each business function are defined (why we use it, what problem we solve).
- [ ] **A.9.4.** For each AI system, intended use and explicit limitations (what it is NOT for) are recorded.

### A.10 Third parties and customers

- [ ] **A.10.2.** Allocation of responsibilities with third parties (AI suppliers, outsourced services, customers) is documented in contracts.
- [ ] **A.10.3.** When selecting AI suppliers (OpenAI, Anthropic, Google, etc.), their AI management policies, terms of service, and data handling are reviewed.
- [ ] **A.10.4.** Customers are provided with information and tools for responsible use of your AI system (documentation, limits, recommendations).

---

## Result interpretation

Count your ✅ out of 66 items:

| Share of ✅ | What it means | What to do next |
|-------------|----------------|------------------|
| **80–100 %** | You are practically ready for Stage 1 | Close remaining items, run an internal audit, select a certification body |
| **60–79 %** | Solid foundation; systematic gap analysis needed | 3–4 months of focused work on priority sections; start picking a certification body in parallel |
| **40–59 %** | Some elements exist, but the AIMS is not running as a system | 6–8 months of intensive work; an external gap analysis and implementation plan are advisable |
| **20–39 %** | Near-zero start, with isolated processes (often inherited from ISO 27001) | 9–12 months; a full implementation project with a dedicated AIMS lead is needed |
| **< 20 %** | The AIMS does not exist as a system | 12–18 months; consider starting with ISO 27001 first, then 42001 |

---

## What to do with this result

> 📩 **Free 15-minute consultation in Telegram**
> Tell me your ✅ percentage and which items hurt the most. I will help you understand where to start in your specific situation, how to scope, and how long it realistically takes.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview](./README.md)
- [Executive FAQ](./faq.md)
- [Step-by-step implementation guide](./implementation-guide.md)
- [Cost and timeline](./cost-timeline.md)
---

*This checklist version corresponds to ISO/IEC 42001:2023 (December 2023).*
*If you already hold ISO/IEC 27001, about 40 % of these items are already covered by your ISMS.*
