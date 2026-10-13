# Top 15 Common ISO/IEC 42001 Stage 2 Audit Findings

> 🇷🇺 [Читать на русском](./ru/common-audit-findings.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** Analysis of typical nonconformities that auditors (Schellman, A-LIGN, Coalfire, BSI) find during Stage 2 first-time ISO/IEC 42001 audits. For each: the affected control, signs, what evidence the auditor expects, common mistakes, and how to close. Based on public CB content from 2024–2026.

> **Context.** Most companies receive 1–3 minor nonconformities and 0–1 major at their first audit. That is **normal**. A major blocks certification until remediation. A minor must be remediated within 30–90 days.

---

## Contents

- [How nonconformity classification works](#how-nonconformity-classification-works)
- [Top 15 findings](#top-15-findings)
- [Distribution by clause area](#distribution-by-clause-area)
- [How to avoid these findings](#how-to-avoid-these-findings)

---

## How nonconformity classification works

| Type | What it means | Action |
|------|---------------|--------|
| **Major nonconformity** | Systematic failure of a requirement or breakdown of a key AIMS process. E.g., no AI Policy, no risk assessment. | No certificate issued until closed. A partial reaudit may be required. Closure typically within 90 days. |
| **Minor nonconformity** | Isolated gap or incomplete compliance. E.g., a document outdated by 2 months, a single record missing. | Certificate issued, but closure required before the next surveillance. Typically 30–90 days. |
| **Observation / OFI** | Not a violation but a recommendation. | No obligation, but recorded in the improvement plan. |

The auditor's goal is not to fail you but to verify the AIMS actually operates. A good CB helps surface weak spots early (at Stage 1) rather than at Stage 2.

---

## Top 15 findings

### 1. Incomplete AI system inventory (A.4.2)

**Signs:** the company registers its "own" models but forgets:
- AI accessed via third-party APIs (OpenAI, Anthropic, Google Cloud) inside the product.
- AI features within employee SaaS tools (Notion AI, Slack AI, GitHub Copilot).
- Shadow AI (see separate document).

**What the auditor wants:** a single inventory where each AI system has owner, version, use case, data flow, review date.

**How to close:** run an inventory exercise across departments, collect the all-hands AI tool list, add to the inventory. 30–60 days.

---

### 2. Undocumented or formulaic AI risk assessment (Clause 6.1)

**Signs:** "we have a classic infosec risk assessment, we included AI risks in it." Reality: AI specifics (drift, bias, hallucinations, foreseeable misuse) are not analysed.

**What the auditor wants:** a distinct risk register with explicit AI risk separation, methodology (e.g., ISO/IEC 23894), mapping to specific AI systems from the inventory.

**How to close:** run an AI risk assessment workshop with engineering + legal + product. Use NIST AI RMF or ISO/IEC 23894 taxonomy. 60–90 days.

---

### 3. AI Impact Assessment without societal dimension (A.5.5)

**Signs:** impact assessment was done "for the paperwork", looks only at business risks. Societal and systemic impact not assessed.

**What the auditor wants:** AISIA per ISO/IEC 42005 with explicit analysis of impact on individuals, groups, society. Foreseeable misuse — mandatory.

**How to close:** rework AISIA along the 8-component 42005 structure for high-risk systems. Bring in an external reviewer for high-risk. 30–90 days.

---

### 4. No drift detection evidence (A.6.2.6)

**Signs:** policies say "we monitor drift" — in practice no configured metrics, no alerting, no review logs.

**What the auditor wants:** a concrete dashboard or reports with metrics (drift score, deviation, performance over time), review cadence, documented response to detected drift.

**How to close:** deploy Fiddler / Arize / Evidently or a custom MLflow-based solution. Document thresholds, alerting, response. 60–90 days (allowing for integration).

---

### 5. Human oversight levels not documented (A.6.1.2 + Clause 7)

**Signs:** for each AI system the level (human-in-the-loop, on-the-loop, in-command) is not explicitly defined.

**What the auditor wants:** in the system card or AISIA — a justified oversight level, named human, tools to intervene, training of those humans.

**How to close:** for each system in the inventory define the level, add to documentation, train operators. 30 days.

---

### 6. Third-party AI not in supplier management (A.10.3)

**Signs:** OpenAI API used in the product but absent from the supplier register. DPA not signed. Training opt-out not verified.

**What the auditor wants:** OpenAI, Anthropic, Google Cloud, every AI provider — in the supplier register with DPA, compliance assessment, monitoring.

**How to close:** audit all AI vendors, sign DPAs (or confirm existing contract terms), populate supplier records. 30–60 days.

---

### 7. Bias audit performed once, not repeated (A.5.4)

**Signs:** bias assessment done at development on test data. Not repeated on production data.

**What the auditor wants:** recurring bias audits (quarterly for high-risk, at minimum annual for others), on real production data, with documented results and actions.

**How to close:** set up a recurring bias audit process, fold into operations rhythm, document the first cycle. 60–90 days.

---

### 8. AI system logs retained under 90 days (A.6.2.8)

**Signs:** log retention follows standard IT defaults of 7–30 days.

**What the auditor wants:** retention sufficient for incident investigation. For high-risk systems — typically 1+ year. For regulated industries — possibly 5+ years.

**How to close:** extend retention, write a dedicated AI data retention policy, ensure log immutability. 30 days.

---

### 9. Internal audit not conducted or formulaic (Clause 9.2)

**Signs:** at Stage 2 the first AIMS internal audit has either not happened or was done formally by the team that designed the system.

**What the auditor wants:** at least one internal audit by an independent person, documented plan, report, corrective actions.

**How to close:** run an internal audit before Stage 2 (in-house via an independent reviewer, or via an external consultant). 30 days with a plan in place.

---

### 10. Management review formulaic or missing (Clause 9.3)

**Signs:** management review "discussed at standup", no minutes retained. Decisions not recorded.

**What the auditor wants:** structured meeting with top management, agenda per Clause 9.3 (policy, incidents, risks, KPIs), documented decisions, follow-up actions.

**How to close:** run a full management review, record minutes, file actions in a tracker. 30 days.

---

### 11. AI Policy not communicated to employees (Clause 7.3, A.2.2)

**Signs:** policy signed by the CEO, sits in a shared drive. On employee surveys — "heard of it, did not read it."

**What the auditor wants:** evidence of training (LMS reports, attendance, signed acknowledgements), employee awareness of the Policy (via surveys), periodic refreshers.

**How to close:** roll out mandatory training on the AI Policy, capture acknowledgements, include in onboarding. 60 days.

---

### 12. Technical documentation outdated (A.6.2.7)

**Signs:** documentation describes the architecture of the model/system from two versions back.

**What the auditor wants:** current documentation synchronized with the production system.

**How to close:** audit the documentation, update, introduce a mandatory update procedure on every release. 30–60 days.

---

### 13. No process for AI incidents (Clause 10 + A.8.4)

**Signs:** the general (infosec) incident response exists. AI-specific incidents (model discrimination, hallucination in production, jailbreak) are handled as ordinary bugs.

**What the auditor wants:** a distinct AI incident response procedure with triggers, escalation, stakeholder notifications, root cause analysis, regulator notifications (where applicable).

**How to close:** draft the AI incident response playbook (see template in templates/), run a tabletop exercise, document. 30–60 days.

---

### 14. Concern reporting channel not operating (A.3.3)

**Signs:** the policy lists `ai-concerns@company.com`, in practice no one monitors it.

**What the auditor wants:** a functional channel with a named owner, response SLA, evidence of handled reports.

**How to close:** assign owner, set up monitoring, work through accumulated reports, document the process. 30 days.

---

### 15. Scope statement too broad or vague (Clause 4.3)

**Signs:** scope says "all AI systems of the company" without an explicit list. At Stage 2 it turns out some systems are not ready.

**What the auditor wants:** a clear scope with explicit in-scope / out-of-scope, justification for each group, explicit mapping to business functions.

**How to close:** rewrite scope before Stage 1. If surfaced at Stage 2 — usually major nonconformity. Closure time depends on the work needed to bring systems into compliance.

---

## Distribution by clause area

| Clause area | Share of typical findings |
|-------------|----------------------------|
| A.4 Resources | ~20 % |
| A.5 Impact Assessment | ~15 % |
| A.6 Lifecycle | ~20 % |
| A.10 Third parties | ~10 % |
| Clauses 6, 9, 10 (management requirements) | ~25 % |
| A.2, A.3, A.7, A.8, A.9 | ~10 % |

Takeaway: 65 % of all findings are in management and lifecycle areas. The key is not "more documents" but a system that actually operates.

---

## How to avoid these findings

Five practical tips:

### 1. Always run a Stage 0 / pre-audit gap analysis

2–3 months before Stage 1, bring in an external expert (could be from your future certification team) to walk through a checklist. 80 % of future nonconformities are visible in advance.

### 2. Internal audit is not a formality

Run an internal audit by an independent person 30–60 days before Stage 1. Use the same criteria the certification auditor will use. Findings closed there are your "free" remediation.

### 3. Documentation should be alive, not just exist

Do not write policies "for the shelf". Every process should be backed by operational evidence: training, tickets, logs, reports, updates.

### 4. Start with a narrow scope

Narrow scope (one product, one BU) gives you two advantages: you finish preparation properly, and the audit runs faster. Expansion comes at recertification.

### 5. Do not skimp on consulting for the first certificate

A good external consultant with 42001-certification experience saves 2–3× their fee by preventing major nonconformities. For the first certificate this is critical.

---

## Need help preparing for Stage 2?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss your situation: where the likely weak spots are, what is critical to close before Stage 2, what plan is left.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [Readiness checklist](./checklist.md)
- [Accredited certification bodies](./anab-accredited-cbs.md)
- [Step-by-step implementation guide](./implementation-guide.md)
---

*Sources: Schellman — "Lessons Learned from Auditing & Implementing ISO 42001" and "Guide to ISO 42001 Certification"; Glocert — "Common ISO 42001 Nonconformities"; A-LIGN, Coalfire public materials; Vanta — "ISO 42001 audit guide"; Elevate Consult — "Final Audit & Evidence Collection for ISO 42001 AIMS".*
