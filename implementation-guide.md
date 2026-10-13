# How to implement ISO/IEC 42001: a step-by-step guide

> 🇷🇺 [Читать на русском](./ru/implementation-guide.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** A phase-by-phase route from the decision to certify to the certificate in hand. Not a checklist (that lives [here](./checklist.md)) and not a budget (that lives [here](./cost-timeline.md)) — this is the sequence of work: what you do first, what it produces, who owns it, and where teams stumble. Aligned with the 10 clauses and 38 Annex A controls of ISO/IEC 42001:2023.
>
> **Who it is for.** The person who will actually run the project — CISO, DPO, Head of AI Governance, or a founder wearing all three hats. Read it once end to end, then use it as a map.

---

## Contents

- [The shape of the project](#the-shape-of-the-project)
- [Phase 0. Decision and scope](#phase-0-decision-and-scope)
- [Phase 1. Context and leadership (clauses 4–5)](#phase-1-context-and-leadership-clauses-45)
- [Phase 2. Planning (clause 6)](#phase-2-planning-clause-6)
- [Phase 3. Operation (clauses 7–8)](#phase-3-operation-clauses-78)
- [Phase 4. Evaluation (clause 9)](#phase-4-evaluation-clause-9)
- [Phase 5. Certification audit](#phase-5-certification-audit)
- [Phase 6. Keeping the certificate (clause 10)](#phase-6-keeping-the-certificate-clause-10)
- [Who does the work](#who-does-the-work)
- [The five mistakes that cost the most time](#the-five-mistakes-that-cost-the-most-time)
- [Timeline at a glance](#timeline-at-a-glance)
- [What to do in the next 90 days](#what-to-do-in-the-next-90-days)

---

## The shape of the project

ISO/IEC 42001 is built on Annex SL — the same skeleton as ISO 27001 and ISO 9001. So the work follows the PDCA cycle, not a random pile of tasks:

- **Plan** — clauses 4–6: understand context, set up leadership, assess risks and impacts, decide which Annex A controls apply.
- **Do** — clauses 7–8: put resources, competence and the controls into operation.
- **Check** — clause 9: monitor, run an internal audit, hold a management review.
- **Act** — clause 10: fix nonconformities, improve.

If you have certified an ISO 27001 ISMS before, the rhythm is familiar. The new muscle is thinking in terms of **AI system impacts on people and society**, not only risks to the organization. That single shift is what the certificate actually certifies.

Two things to fix in your head before you start:

1. **Annex A is a reference, not a shopping list.** Clause 6.1.3 is explicit — you start from the risks and impacts of your specific AI systems and justify what applies in a Statement of Applicability. You do not implement all 38 controls "just in case" ([details](./annex-a-controls.md)).
2. **The certificate covers a scope, not the whole company.** A narrow, honest scope (one product, the AI systems that matter) is faster, cheaper, and easier to defend than "all AI everywhere".

---

## Phase 0. Decision and scope

**Goal:** know why you are doing this and what exactly gets certified.

Before any documents, answer three questions:

- **What triggers this?** An enterprise RFP that demands it, Microsoft SSPA Sensitive Use, EU AI Act exposure, or a competitive edge you want to hold first. The trigger sets the deadline and the scope. See the [executive FAQ](./faq.md) if you are still deciding whether you need it at all.
- **What is in scope?** List every AI system you build, buy, or embed. Mark which ones make or inform decisions about people (hiring, credit, access, moderation). Those are the ones an auditor will care about most.
- **Do you have ISO 27001?** If yes, 40–60 % of the management-system work transfers and you build 42001 as a bolt-on. If no, plan to run them together — many controls overlap ([comparison](./comparison-iso-27001.md)).

**Output of Phase 0:** a one-page scope statement (which entity, which AI systems, which sites) and a named project owner with executive backing. Use the [AIMS scope statement template](./templates/aims-scope-statement.md).

---

## Phase 1. Context and leadership (clauses 4–5)

**Goal:** the organization understands its AI context and top management is visibly on the hook.

- **Clause 4 — Context.** Document internal and external issues, interested parties (customers, regulators, data subjects, society), and finalize the AIMS scope. Build an AI system inventory — you cannot govern what you have not listed.
- **Clause 5 — Leadership.** Top management publishes the **AI Policy**, assigns roles and authorities, and commits resources. This is not a formality: auditors open Stage 1 by testing whether leadership can explain the policy in their own words.

**Common trap:** a policy copied from a template that no executive has read. Write it so your CEO can defend it.

**Output of Phase 1:** approved AIMS scope, AI system inventory, signed AI Policy, a roles-and-responsibilities map.

---

## Phase 2. Planning (clause 6)

**Goal:** you know your AI risks and impacts, and you have decided what to do about them. This is the heart of the standard.

- **6.1.2 — AI risk assessment.** Assess risks to the organization from its AI systems, on a documented and repeatable method.
- **6.1.4 — AI impact assessment.** The clause with no ISO 27001 analogue: assess impacts on **individuals, groups, and society** — fairness, safety, transparency, misuse. ISO/IEC 42005 is the how-to ([guide](./iso-42005-impact-assessment-guide.md)); use the [AI impact assessment template](./templates/ai-impact-assessment.md) to run one.
- **6.1.3 — Statement of Applicability (SoA).** For each of the 38 Annex A controls, decide: applicable or not, and why. The SoA links your risks and impacts to the controls you will operate. It is the single most-scrutinized document in the audit.
- **6.2 — AI objectives.** Set measurable objectives (bias thresholds, incident response times, review cadence) and a plan to reach them.

**Output of Phase 2:** documented risk assessment, at least one AI impact assessment, an approved SoA, measurable AI objectives.

---

## Phase 3. Operation (clauses 7–8)

**Goal:** the controls you chose are not on paper — they are running.

- **Clause 7 — Support.** Resources, competence (train the people who touch AI systems), awareness, communication, and document control. This is where the AIMS becomes real to the wider team.
- **Clause 8 — Operation.** Execute the plans from clause 6: operate the Annex A controls, run impact assessments for new or changed AI systems, manage AI suppliers and third-party models. If you buy or fine-tune external models, your [supplier requirements](./supplier-requirements.md) and an [AI incident response process](./templates/ai-incident-response.md) belong here.

**Common trap:** controls documented but never operated — no logs, no evidence, no owner. An auditor asks "show me the last time this ran", not "show me the policy".

**Output of Phase 3:** operating controls with evidence, trained staff, managed AI suppliers, an incident response process that has been tested at least once.

---

## Phase 4. Evaluation (clause 9)

**Goal:** prove the system works, and catch gaps before the auditor does.

- **9.1 — Monitoring and measurement.** Track your AI objectives and control performance.
- **9.2 — Internal audit.** An independent pass over the whole AIMS against the standard. Findings here are cheap; the same findings in Stage 2 are expensive.
- **9.3 — Management review.** Top management reviews results, incidents, objectives, and decides on changes and resources. Minute it properly — auditors read these minutes closely ([template](./templates/management-review-minutes.md)).

**Output of Phase 4:** monitoring records, a completed internal audit with a corrective-action log, documented management review minutes.

---

## Phase 5. Certification audit

**Goal:** an accredited certification body (CB) confirms the AIMS meets ISO/IEC 42001.

The audit runs in two stages ([how to pick a CB](./anab-accredited-cbs.md)):

- **Stage 1 (1–2 days).** Documentation review and readiness check. The CB reads your scope, policy, SoA, risk and impact assessments, and confirms you are ready for Stage 2. You get a list of gaps to close.
- **Stage 2 (2–5 days for a small company, up to ~30 for enterprise).** The main audit: interviews, evidence, controls in operation. Duration is driven by audit-days under IAF MD 5.
- **Findings.** Address nonconformities (major must be fixed before the certificate; minor get a corrective-action plan).
- **Certificate.** Valid three years, subject to surveillance.

**Common trap:** treating Stage 1 as a formality. It is your last cheap chance to find gaps — use it.

**Output of Phase 5:** a Stage 1 report actioned, Stage 2 passed, an ISO/IEC 42001 certificate. See real [case studies](./case-studies.md) and the [findings that fail companies](./common-audit-findings.md).

---

## Phase 6. Keeping the certificate (clause 10)

**Goal:** the AIMS keeps improving and survives surveillance.

- **10.1 — Continual improvement.** Feed incidents, monitoring, and reviews back into the system.
- **10.2 — Nonconformity and corrective action.** Every incident and finding gets a root cause and a fix that sticks.
- **Surveillance audits (years 2 and 3)** — roughly one-third of the initial audit.
- **Re-certification (year 4)** — a lighter repeat of the full cycle.

**Output of Phase 6:** an operating improvement loop, passed surveillance audits, ongoing 0.25–0.5 FTE of AIMS work.

---

## Who does the work

You do not need a large team. A typical setup:

- **Project owner / AIMS lead** — CISO, DPO, or Head of AI Governance. Runs the project, owns the SoA and management review.
- **Executive sponsor** — signs the policy, unblocks resources, faces the auditor in Stage 1.
- **AI / ML leads** — supply system details, own technical controls, run impact assessments on their systems.
- **Legal / compliance** — regulatory mapping (EU AI Act, sector rules), supplier contracts.
- **Fractional advisor (optional)** — an external AI-governance specialist for 4–6 months where in-house depth is thin. Cheaper than hiring, faster than learning it cold ([budgets](./cost-timeline.md)).

---

## The five mistakes that cost the most time

1. **Scope too wide.** "All AI everywhere" triples the work and the audit. Start narrow.
2. **Skipping the impact assessment.** Clause 6.1.4 is what makes 42001 different from 27001. Auditors go straight to it.
3. **Policy no one has read.** A template AI Policy the leadership cannot explain fails Stage 1.
4. **Controls on paper only.** No evidence, no logs, no owner — a documented control is not an operating control.
5. **Treating GRC tooling as the strategy.** A platform speeds the paperwork; it does not decide your scope, risks, or SoA. Those are judgment calls.

---

## Timeline at a glance

| Starting point | Realistic duration |
|----------------|--------------------|
| Mature ISO 27001, one AI system | 3–6 months |
| Multiple AI systems | 4–9 months |
| From scratch, small organization | 6–12 months |
| Enterprise, complex AI portfolio | 12–18 months |

Durations track [cost-timeline.md](./cost-timeline.md); the biggest variable is how much of an ISO 27001 management system you already run.

---

## What to do in the next 90 days

1. Write the one-page scope statement (Phase 0) — pick a narrow, defensible scope.
2. List every AI system and mark the ones that make decisions about people.
3. Run the [readiness checklist](./checklist.md) and measure your ✅ share.
4. Draft the AI Policy and get an executive to actually read and sign it.
5. Run one AI impact assessment on your highest-stakes system ([template](./templates/ai-impact-assessment.md)).
6. Shortlist 2–3 accredited CBs and ask for indicative Stage 1 / Stage 2 quotes.

---

## Need a hand with the plan?

> 📩 **Free 15-minute consultation in Telegram**
> We map your scope, tell you honestly whether to run 42001 as a bolt-on to 27001 or together, and sketch a realistic timeline for your situation.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [Standard structure — 10 clauses and Annex A](./structure.md)
- [Readiness checklist](./checklist.md)
- [Annex A controls explained](./annex-a-controls.md)
- [AI impact assessment guide (ISO 42005)](./iso-42005-impact-assessment-guide.md)
- [Cost and timeline](./cost-timeline.md)
- [Common audit findings](./common-audit-findings.md)
- [Accredited certification bodies](./anab-accredited-cbs.md)

---

*Sources: ISO/IEC 42001:2023 (clauses 4–10, Annex A); ISO/IEC 42005:2025 (AI impact assessment); IAF MD 5 (audit-day determination). Internal cross-references to this repository's checklist, cost model, Annex A guide, and case studies.*
