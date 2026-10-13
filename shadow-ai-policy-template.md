# Shadow AI Policy: Template and Implementation Guide

> 🇷🇺 [Читать на русском](./ru/shadow-ai-policy-template.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** Shadow AI is the uncontrolled use of external AI tools (ChatGPT, Claude, Gemini, Perplexity, Copilot) by employees without company approval. Cyberhaven and LayerX research shows 70–85 % of companies have active shadow AI. It is a direct risk of data leakage, NDA breach, IP exfiltration, and noncompliance with 42001 controls A.2.2, A.9.2, A.10.3. This document is a ready-to-use policy template with three strategies (ban / sandbox / control) and an enforcement workflow.

---

## Contents

- [1. What Shadow AI is and the scale of the problem](#1-what-shadow-ai-is-and-the-scale-of-the-problem)
- [2. Real-world leak cases](#2-real-world-leak-cases)
- [3. Three strategies: ban / sandbox / control](#3-three-strategies-ban--sandbox--control)
- [4. Acceptable AI Use Policy template](#4-acceptable-ai-use-policy-template)
- [5. Approved and prohibited tool lists](#5-approved-and-prohibited-tool-lists)
- [6. Approval process for new AI tools](#6-approval-process-for-new-ai-tools)
- [7. Employee training program](#7-employee-training-program)
- [8. Monitoring and enforcement](#8-monitoring-and-enforcement)
- [9. Mapping to ISO/IEC 42001](#9-mapping-to-isoiec-42001)

---

## 1. What Shadow AI is and the scale of the problem

Shadow AI is any use of AI tools by employees without explicit approval, inventory registration, or controls. Typical examples:

- A marketer pastes a press release draft into ChatGPT for editing.
- A developer sends a source code snippet to Copilot/Cursor.
- A lawyer uploads a contract draft to Claude for analysis.
- An HR manager asks ChatGPT to write a candidate rejection.
- A finance analyst uses ChatGPT to summarise a quarterly report.

**Research numbers (2025–2026):**
- Cyberhaven: 70 % of employees use external LLMs at work; 11 % of content sent to ChatGPT is confidential.
- LayerX Security: 87 % of AI tools in a typical company are unsanctioned.
- IBM Cost of a Data Breach 2025: average cost of an AI-related data leakage incident is $4.8 M.

For a 42001 AIMS this is a **critical hole**: you cannot satisfy A.4.2 (resource register), A.5 (Impact Assessment), or A.10.3 (supplier control) for tools you do not know exist.

---

## 2. Real-world leak cases

| Company | Date | What happened |
|---------|------|---------------|
| **Samsung Semiconductor** | April 2023 | Engineers pasted source code and meeting notes into ChatGPT. Samsung banned public LLMs on company devices. |
| **JP Morgan Chase** | February 2023 | Restricted ChatGPT after detecting regular employee queries. |
| **Apple** | May 2023 | Internally banned ChatGPT and Copilot over leakage concerns. |
| **Disney, Universal** | 2024 | Blocked ChatGPT after reports that scripts had appeared in training data. |
| **OpenAI title bug** | March 2023 | A bug in ChatGPT exposed other users' chat titles to a random user. |
| **Microsoft Copilot accidental exposure** | 2024 | Corporate data of one tenant surfaced in another's responses through misconfigured RBAC. |

These are the public ones. The real incident count is multiples higher and undisclosed.

---

## 3. Three strategies: ban / sandbox / control

### Strategy A: Full ban

Fit for: banks under strict regulation, defence contractors, healthcare with PHI.

- All public LLMs blocked on corporate devices.
- Employees use only approved enterprise tools.
- DLP and proxy filtering for monitoring.

Pros: maximum data protection. Cons: high compliance overhead, risk of shadow IT through personal devices, productivity loss.

### Strategy B: Sandbox

Fit for: mid-size companies, SaaS, legal, consulting.

- An internal enterprise tool is deployed (Microsoft 365 Copilot, OpenAI Enterprise, Anthropic Claude for Work).
- External tools allowed only from the approved whitelist.
- Corporate data is processed in the enterprise environment with no-training guarantees.

Pros: balance of security and productivity. Cons: high license cost ($30–60 per user/month).

### Strategy C: Controlled freedom

Fit for: startups, R&D teams, creative industries with low regulation.

- Any AI tool allowed for non-confidential tasks.
- Clear rules: what can and cannot be uploaded.
- Enforcement via awareness and training, not blocks.

Pros: minimum overhead, high productivity. Cons: relies on employee discipline.

**Recommendation for most 50–500 person SaaS companies:** Strategy B (sandbox).

---

## 4. Acceptable AI Use Policy template

```markdown
# Acceptable AI Use Policy

Version: 1.0
Approval date: [DATE]
Owner: [ROLE — typically CISO or AIMS Lead]
Applies to: all employees, contractors, and interns of [COMPANY].

## 1. Purpose and scope

This policy sets the rules for using artificial intelligence tools ("AI Tools") for work purposes. It applies to any AI use through company devices, networks, and accounts, as well as personal devices for work tasks.

## 2. Principles

1. **Transparency.** Any use of AI to produce client-facing or public content must be disclosed.
2. **Data protection.** Confidential data is not sent to AI Tools without approval.
3. **Accountability for outputs.** The employee is accountable for the accuracy and applicability of AI-generated content.
4. **Compliance.** AI use must comply with GDPR, NDAs, contractual obligations, and applicable law.

## 3. Allowed without additional approval

- Use of whitelisted tools (see section 5) for work tasks.
- Drafting of publicly available information (marketing materials, social posts without insider data).
- Translation and editing of texts containing only public information.
- Coding assistance not involving company or client IP.
- Research on general topics not tied to specific client projects.

## 4. Not allowed without explicit AIMS Lead approval

- Uploading to public AI:
  - Personal data (anything under GDPR).
  - Confidential client or partner information.
  - Company source code.
  - Pre-disclosure financial data.
  - Strategic documents.
  - NDA-protected information.
- Using AI for automated people decisions (hiring, firing, evaluation, access) without human-in-the-loop.
- Publishing AI-generated content without AI-use disclosure for client or public materials.
- Using AI for deepfakes, manipulative content, or impersonation.

## 5. Approved tools (whitelist)

See the separate register at [REGISTER LINK]. Updated quarterly.

All whitelisted tools have passed:
- Legal review (DPA, terms, training opt-out).
- Security assessment.
- AISIA for high-risk scenarios.

## 6. Requesting a new tool

If you need a tool not on the whitelist:
1. Describe the use case in the form at [FORM LINK].
2. AIMS Lead reviews within 5 business days.
3. Decision is recorded in the tool register.

## 7. Incidents

If you accidentally upload confidential data to an AI:
1. Report to AIMS Lead via [CHANNEL] immediately.
2. Do not attempt to "undo" — you cannot.
3. Capture incident details (what, when, where).
4. AIMS Lead determines next steps (customer notification, regulator, remediation).

No disciplinary action will follow **reporting** an incident. Discipline may follow **concealment**.

## 8. Control and enforcement

- DLP systems monitor attempts to send data to unsanctioned AI tools.
- Quarterly shadow-AI report is presented at management review.
- Policy violations follow the general disciplinary process.

## 9. Training

All employees complete AI awareness training:
- On hire (as part of onboarding).
- Annually (mandatory refresh).
- On significant policy changes.

## 10. Policy review

The policy is reviewed:
- At minimum annually.
- On the emergence of new AI tool categories.
- After a material AI incident.
- On regulatory changes.
```

---

## 5. Approved and prohibited tool lists

Sample whitelist/blacklist for a typical SaaS:

**Approved (enterprise, no-training):**
- Microsoft 365 Copilot (Enterprise tenant)
- OpenAI ChatGPT Enterprise / Team
- Anthropic Claude for Work
- Google Workspace Gemini (Enterprise)
- GitHub Copilot Business / Enterprise
- Cursor Pro (for development)

**Conditionally allowed (non-confidential tasks only):**
- Perplexity Pro (research, no document uploads)
- DeepL (translation of public content)
- Grammarly Business (with no-training configured)

**Prohibited:**
- ChatGPT Free / Plus (non-Enterprise)
- Claude Free
- Gemini Free
- Any public deepfake generators.
- Any AI tools from vendors without a public DPA and privacy policy.

---

## 6. Approval process for new AI tools

Steps:

1. **Request** from an employee or team.
2. **Legal review:** DPA, training opt-out, jurisdiction, subprocessors.
3. **Security review:** auth, SSO, data flow, retention.
4. **Privacy review:** DPIA mini-template.
5. **Cost and use-case review:** ROI vs alternatives.
6. **AIMS Lead decision:** approve / approve with restrictions / reject.
7. **Record in the register** and update the policy.

Turnaround: 5 business days for standard tools, 15 for high-risk.

---

## 7. Employee training program

Minimum 30 minutes per employee per year:

- What Shadow AI is and why it is dangerous.
- Real-world leak cases.
- What is allowed and what is not under company policy.
- How to request approval for a new tool.
- How to report an incident.

For high-access employees (engineering, legal, finance) — a 1-hour extended module walking through concrete use cases.

---

## 8. Monitoring and enforcement

**Technical controls:**
- DLP rules at endpoint and network levels.
- Browser extension monitoring for known AI domains.
- SSO with access control to approved AI tools.
- Logging of enterprise AI tool requests for investigation.

**Organisational controls:**
- Quarterly shadow AI report at management review.
- Anonymous reporting channel for incidents.
- "AI policy awareness" KPI in annual reviews.

**Disciplinary measures:**
- First violation — training and warning.
- Second — formal written notice.
- Systematic disregard — standard disciplinary actions.

---

## 9. Mapping to ISO/IEC 42001

Shadow AI Policy directly satisfies:

| 42001 Control | What Shadow AI Policy covers |
|---------------|------------------------------|
| **A.2.2** AI Policy | It is itself part of the AI Policy |
| **A.4.2** Resource register | Prohibits use of tools not in the register |
| **A.5.2** Impact Assessment | Requires AISIA when adding new tools |
| **A.7.3** Data collection | Controls what flows into AI tools |
| **A.9.2** Responsible use processes | Direct match |
| **A.9.3** Responsible use objectives | Direct match |
| **A.9.4** Intended use | Direct match |
| **A.10.3** Suppliers | Requires legal review of every AI vendor |

Without a Shadow AI Policy, these controls are nearly impossible to close for a modern company.

---

## Need help drafting your policy?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss your situation: which strategy to pick, how to adapt the template to your team, how to set up enforcement.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [GenAI/LLM-specific controls](./genai-llm-specific-controls.md)
- [AI Incident Response template](./templates/ai-incident-response.md)
- [Vendor risk assessment for AI](./vendor-risk-assessment-ai.md)
---

*Sources: Cyberhaven "Generative AI in the Workplace" (2025); LayerX Security "State of GenAI in the Enterprise" (2025); IBM "Cost of a Data Breach 2025"; public reporting on Samsung, JP Morgan, Apple, Microsoft incidents.*
