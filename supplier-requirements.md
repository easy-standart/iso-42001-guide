# AI Supplier Requirements: Microsoft SSPA DPR v10 and the Procurement Cascade

> 🇷🇺 [Читать на русском](./ru/supplier-requirements.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** Effective 23 September 2024, Microsoft SSPA DPR v10 introduced Section K — 18 mandatory requirements for suppliers using AI Systems. An ISO/IEC 42001 certificate is explicitly accepted as a substitute for the Section K independent assessment. Under Sensitive Use it becomes mandatory. Hyperscalers (AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow) cascade similar expectations through their Supplier Codes, Responsible AI Policies, and AI Control Tower platforms. Procurement questionnaires (Shared Assessments SIG 2025/2026, CSA AICM, HECVAT 4) now map directly to Annex A of 42001. Through RFPs this reaches tier-2 and tier-3 subcontractors.

---

## Contents

- [1. What changed in Microsoft SSPA DPR v10](#1-what-changed-in-microsoft-sspa-dpr-v10)
- [2. The 18 Section K requirements in full](#2-the-18-section-k-requirements-in-full)
- [3. The ISO/IEC 42001 carve-out](#3-the-isoiec-42001-carve-out)
- [4. Sensitive Use — three criteria](#4-sensitive-use--three-criteria)
- [5. Equivalents at AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow](#5-equivalents-at-aws-google-cloud-ibm-salesforce-oracle-servicenow)
- [6. SIG, CAIQ, HECVAT — how ISO 42001 enters questionnaires](#6-sig-caiq-hecvat--how-iso-42001-enters-questionnaires)
- [7. Tenders and public procurement](#7-tenders-and-public-procurement)
- [8. The supplier-ready kit](#8-the-supplier-ready-kit)

---

## 1. What changed in Microsoft SSPA DPR v10

**Supplier Security & Privacy Assurance (SSPA)** is a joint program of Microsoft Procurement, Corporate External and Legal Affairs, and Corporate Security. It delivers the **Microsoft Supplier Data Protection Requirements (DPR)** to all suppliers processing Personal Data, Microsoft Confidential Data, or **AI Systems** in connection with a contract.

**Key dates:**

- **23 September 2024** — DPR v10 took effect. The most significant DPR update since GDPR (2018).
- Annual self-attestation is mandatory. A supplier's status flips to "Red" on breach of the 90-day window — new orders are blocked until "Green".
- Suppliers with anniversaries after 23 September 2024 receive new tasks. For AI Systems, Section K + Independent Assessment must be closed before a Purchase Order opens and any data processing begins.
- Independent assessment is performed by a firm on Microsoft's Preferred Assessors list. An "unqualified" Letter of Attestation is uploaded to the SSPA portal.

**Key v10 definitions:**

- **AI Systems** — "engineered system that applies an optimized model so that the system can, for a given set of human-defined objectives, make predictions, recommendations, or decisions". Definition explicitly covers generative AI.
- **Sensitive Use** — three criteria (see section 4).
- **Red Teaming** — purposeful testing for limits, risk surfaces, and vulnerabilities.
- **Human Oversight** — three levels: human-in-the-loop, human-on-the-loop, human-in-command.

---

## 2. The 18 Section K requirements in full

Section K applies only to suppliers providing services that use AI Systems. Numbering matches DPR v10 (items 53–70):

| # | Title | What the supplier must do |
|---|-------|---------------------------|
| 53 | AI Systems contractual terms | Special AI provisions in the contract with Microsoft. Intended Uses changes disclosed without delay, reviewed at least annually. |
| 54 | Accountability ownership | Assign a specific person/role for troubleshooting, operations, and lifecycle control. Document the mandate. |
| 55 | Annual training | Annual privacy and security training for everyone handling data in AI Systems. Content validated. |
| 56 | AI System incident response plan | Plan covering Microsoft notification, rollback, feature disable, model update procedure, customer communication. |
| 57 | Red Teaming | Red Teaming required, identified vulnerabilities closed pre-deployment. |
| 58 | Responsible AI program | Documented responsible-AI program covering disclosures and documentation. |
| 59 | Intended Uses Transparency disclosures | Intended-use documents provided to Microsoft on request. |
| 60 | Signed Agreement with AI sub-suppliers | When using AI sub-suppliers — signed contract covering data, confidentiality, IP, liability, incidents, Sensitive Uses. |
| 61 | Accountability (continuous) | Clear lines of responsibility for deployment and AI risk management. Regular monitoring and audits. |
| 62 | Risk Assessment | Risk assessment covering bias, vulnerabilities, unforeseen consequences. For Sensitive Uses — additional controls. Artefacts retained. |
| 63 | Transparency and Explainability | Disclosures on model architecture, training data, decision process. Logging of failures, distortions, hallucinations. |
| 64 | Monitoring and Adaptation | Continuous monitoring, adaptation as new risks emerge. |
| 65 | Performance & safety disclosures | Tolerable error ranges, false positive/negative per Intended Use, Sensitive Use documentation, automation-bias mitigations, model limitations, controls against jailbreaks / data poisoning / prompt extraction, accuracy evidence. |
| 66 | Update & notification | Update Intended Uses on new use cases, functionality changes, release-stage changes, new safety data, accuracy metric changes. |
| 67 | System health monitoring / SOP | SOP per system: failure reproduction, tracked events, prioritization, review cadence, time to remediate, third-party and open-source component currency control. |
| 68 | Inventory of monitoring methods | Detailed inventory: data and alerts, customer complaint mechanisms, public feedback channels. |
| 69 | Failure of Intended Use procedures | On unfit-for-purpose findings: marketing withdrawal, customer notification, gap closure or shutdown, documentation revision. |
| 70 | Demographic disparity disclosure | Identify and disclose demographic groups (including marginalised) that may receive degraded service quality. Document justifying operational factors (e.g., "background noise" for speech systems). |

Plus one Data Subjects requirement (item 24) outside Section K: the supplier maintains a record of all recipients of Microsoft Personal Data. Total 17 new in Section K + 1 in Section F = **18 new requirements in v10**.

---

## 3. The ISO/IEC 42001 carve-out

Microsoft's SSPA Program Guide v10 states explicitly: "ISO 27701 (privacy), ISO 27001 (security), and ISO 42001 for AI Systems (DPR Section K) are relied on as providing close mapping to the DPR".

What this means for a supplier:

- **A valid ISO/IEC 42001 certificate is accepted in place of the Section K independent assessment.**
- Under **Sensitive Use** scenarios, ISO/IEC 42001 becomes **mandatory** as the Independent Assessment substitute. The scenario additionally goes through Microsoft Office of Responsible AI review.
- The certificate scope and DPR version must match. v10 attestation is invalid if the supplier filed under DPR v9.

This is the first time a major enterprise buyer officially equates ISO 42001 with its own compliance program.

---

## 4. Sensitive Use — three criteria

Exact wording from the DPR v10 glossary:

> "Sensitive Use" of AI is when the reasonably foreseeable use or misuse of an AI System could affect an individual in the following ways:
> - Consequential impact on legal position or life opportunities.
> - Risk of physical or psychological injury.
> - Threat to human rights.

The same triad appears in Microsoft's Responsible AI Standard v2. Sensitive Uses review is run by the **Office of Responsible AI (ORA)** together with the **AETHER** committee.

**Escalation flow:**

- In the Impact Assessment (prompts A2.2), the team answers the three criteria. If any applies, the case escalates to ORA.
- The Sensitive Uses and Emerging Technologies program runs pre-deploy review, often layering requirements beyond the RAI Standard.
- Per Microsoft Responsible AI Transparency Report 2024, **77 %** of consultations involved generative AI.

**Restricted vs. Sensitive:**

- Restricted — disallowed scenarios (e.g., facial recognition for police body cameras — Microsoft's public refusal since 2019).
- Sensitive — allowed but requiring additional control.

---

## 5. Equivalents at AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow

No other hyperscaler has yet published an SSPA DPR v10-level document, but contracts and policies cascade similar expectations.

### AWS

- **Amazon Vendor Security Policy (AVSP)** built on ISO/IEC 27001/27002 and NIST CSF. Hard restriction: "Supplier will not develop, train, or improve any AI/ML models using Amazon Information, even if Anonymized".
- **AWS Responsible AI Policy** defines "consequential decisions" (health, judicial, housing, employment, credit, medical/legal advice) and requires human oversight and safeguards.
- **AWS Responsible AI Framework** built on 8 dimensions: fairness, explainability, privacy & security, safety, controllability, veracity & robustness, governance, transparency.
- AWS publicly calls ISO 42001 a foundational standard. Certified as a major cloud provider by April 2025.

### Google Cloud

- **Supplier Code of Conduct** sets general expectations, no AI specifics.
- **Google AI Principles** (June 2018, revised 4 February 2025) — the revision removed earlier military application bans.
- **Google Cloud Responsible AI** runs dual review: Responsible Innovation team + deal-level review.
- ISO/IEC 42001 for Google Cloud Platform, Google Workspace, and Gemini (App) — certificates published in the Cloud Compliance Center.

### IBM

- **Supplier Conduct Principles** built on the Responsible Business Alliance Code of Conduct. A social/environmental management system has been mandatory for all first-tier suppliers since 2010.
- **5 Pillars of Trustworthy AI**: fairness, robustness, privacy, explainability, transparency.
- **AI Ethics Board / Responsible Technology Board** review use cases.
- IBM committed to training 1000 suppliers on AI ethics by 2025. By end of 2023, more than 600 trained.
- **watsonx.governance** offered to customers as an automation tool.

### Salesforce

- **Global Supplier Code of Conduct** (June 2025).
- **Trusted AI Principles**: Responsibility, Accountability, Transparency, Empowerment, Inclusivity.
- **AI Acceptable Use Policy** requires UI marking of automated interactions.
- **Einstein Trust Layer**: dynamic grounding, zero data retention with LLM providers, data masking, toxicity detection, audit trail.

### Oracle

- **Supplier Code of Ethics and Business Conduct** — classical compliance document, no AI specifics.
- **CAIQ v4.0** for Oracle Cloud Infrastructure describes CCM controls, references ISO/IEC 27002, SOC 1/2/3, HIPAA, PCI.
- Supplier AI requirements formalized weakly, cascaded via privacy/security clauses and ad-hoc DPAs.

### ServiceNow

- **Code of Business Conduct and Ethics**.
- **Now Assist Guardian / AI Control Tower** — internal platform for AI stewardship, approval workflows, AI asset inventory. References EU AI Act and NIST AI RMF.
- ServiceNow has stated full EU AI Act compliance within the 24-month grace period.
- Requires ISO 27001 / SOC 2 from suppliers.

### Summary table

| Vendor | Document | AI specifics | ISO 42001 as equivalent |
|--------|----------|---------------|--------------------------|
| Microsoft | SSPA DPR v10 Section K | 18 mandatory, Sensitive Use ⇒ required | Yes, explicitly (carve-out) |
| AWS | AVSP + Responsible AI Policy | No training on Amazon data, human oversight | Not explicit (AWS itself certified) |
| Google Cloud | Supplier Code + AI Principles | Adherence to AI Principles + SAIF | Not explicit (Google itself certified) |
| IBM | Supplier Conduct Principles + Trustworthy AI | 1000-supplier training; no dedicated DPR | Not explicit |
| Salesforce | Global Supplier Code + Trusted AI Principles + AI AUP | Disclosure, Einstein Trust Layer | Not explicit (ISO 27001/27701) |
| Oracle | Supplier Code + CAIQ v4 | No standalone AI-DPR | Not stated |
| ServiceNow | Code + AI Control Tower / Now Assist Guardian | EU AI Act, NIST AI RMF | Expected via VRM |

---

## 6. SIG, CAIQ, HECVAT — how ISO 42001 enters questionnaires

### Shared Assessments SIG

- Owned by Shared Assessments (since 2005; acquired by OneTrust in 2021).
- **SIG 2025** covers 21 risk control domains, references DORA, NIS2, NIST 2.0.
- **SIG Lite 2025** — 128 questions. **SIG Core** — about 850 questions.
- **SIG Workbook 2026** (released 19 September 2025) explicitly adds ISO/IEC 42001 as a "newly relevant and rapidly maturing framework".

### Cloud Security Alliance — CAIQ v4 and AICM

- **CAIQ v4.0.2** — 261 questions across 17 CCM v4 domains. **CAIQ-Lite** — 124 questions.
- **AI Controls Matrix (AICM) v1.0** released 10 July 2025: 243 control objectives across 18 domains. Shared Security Responsibility model (CSP, Model Provider, Orchestrated Service Provider, Application Provider, AI Customer).
- **AI-CAIQ** — self-assessment questionnaire under AICM.
- **AICM ↔ ISO/IEC 42001 mapping** published 20 August 2025 alongside **STAR for AI 42001**. A certified company uploads the certificate to STAR Registry and, by adding Valid-AI-ted AI CAIQ, gets provisional STAR for AI 42001 Level 2.

### HECVAT 4

- Owned by EDUCAUSE + Internet2 + REN-ISAC.
- **HECVAT 4.1.5** released 10 February 2025: Full / Lite / On-Prem merged into a single workbook, AI-specific tab and Privacy tab added.
- **AI tab** assesses AI risk management, responsible training, AI governance, AI feature disable, protection of data from LLM training.
- 321 questions, aligned with NIST 800-53, HIPAA, PCI DSS. ISO/IEC 42001 not yet named explicitly, but the AI tab covers Annex A.

### Questionnaire-to-Annex A mapping

| Questionnaire section | Annex A 42001 | Typical question |
|------------------------|----------------|-------------------|
| SIG "AI Governance" (2025/2026) | A.2, A.3, A.4 | Is the AI Policy board-approved? Who is the AI management representative? |
| SIG "Risk Management" | A.5, A.6.1 | Is AI impact assessment performed? Documented? |
| SIG "Third-Party Management" | A.10 | Which contracts cascade AIMS to sub-suppliers? |
| CAIQ v4 "GRC" | A.2, A.3, A.9 | Documented compliance plan? |
| CAIQ v4 "HRS" | A.4.3 | Staff AI training? |
| CAIQ v4 "Data Security and Privacy" | A.7 | Training data provenance policy |
| AICM "Model Security" | A.6, A.8 | Red teaming, jailbreak protection |
| AICM "Data Security and Privacy" | A.7 | Model and training-set lineage |
| AICM "GRC" | A.2, A.3, A.9 | AI metrics, internal audit |
| HECVAT 4 AI tab | A.2, A.4, A.5, A.6, A.7, A.9 | AI disable, training data, governance |

---

## 7. Tenders and public procurement

### Timeline of ISO 42001 in tenders

- **December 2023** — ISO/IEC 42001:2023 published.
- **2024 (Q2–Q4)** — first certifications (Anthropic January 2025, Snowflake 2024, KPMG, Cognizant, Integral Ad Science, Synthesia, Microsoft Copilot, AWS, Google). Tenders treat 42001 as a "bonus".
- **Q1 2025** — ISO/IEC 42001 emerges as a scoring factor, not yet blocking.
- **Q2–Q4 2025** — large RFPs (banking, pharma, insurance, UK and US federal) begin to phrase "ISO 42001 or equivalent required". ISACA 2025 — 76 % of organisations plan to use ISO 42001 as the reference.
- **Q1 2026** — Pitchbook recorded more than 250 corporate RFPs in the EU, US, and UK with direct ISO 42001 requirements.

### Jurisdictions

- **EU: TED (Tenders Electronic Daily)** — mass channel where 42001 appears in IT procurement for state and national companies.
- **UK** — **UK ATRS** (Algorithmic Transparency Reporting Standard) mandatory for central departments since 6 February 2024. **CCS G-Cloud 15** opens September 2026 with £14 bn budget.
- **US** — **OMB M-25-21** and **M-25-22** (April 2025) restructured federal AI procurement. ISO 42001 is embedded indirectly through the NIST AI RMF crosswalk.
- **Asia** — Singapore (IMDA AI Verify), Japan, Korea — point cases mentioning 42001.

### Competitive advantage

From public cases 2025–2026:

- Time-to-contract is shortened by 4–8 weeks on average when the certificate is present.
- Win rate in enterprise deals with AI features grows 15–30 % at equal price.
- 60–80 % of standard security/AI questionnaire items are pre-answered.

---

## 8. The supplier-ready kit

Minimum set you need to enter hyperscaler supply chains and answer SIG/CAIQ/HECVAT without negotiation.

**Documents:**

- AIMS Scope Statement (Clause 4.3) — [template](./templates/aims-scope-statement.md).
- AI Policy approved by C-level.
- AI systems register — [template](./templates/ai-system-card.md).
- Statement of Applicability over 38 Annex A controls.
- AI Risk Register (per ISO/IEC 23894).
- AISIA for every high-risk system (per [ISO/IEC 42005:2025](./iso-42005-impact-assessment-guide.md)).
- Supplier Register with DPAs from every AI provider.
- AI Incident Response Playbook — [template](./templates/ai-incident-response.md).
- Red Teaming reports.
- Performance & safety disclosures by Intended Use.

**Processes:**

- Annual privacy/security training for everyone handling AI Systems.
- Drift and bias monitoring with log retention ≥ 90 days.
- AIMS requirements cascaded to subcontractors in contracts.
- Management review at minimum annually.

**Certificate:**

- ISO/IEC 42001 from an ANAB/UKAS/RvA-accredited CB. This unlocks the Microsoft carve-out and pre-answers 60–80 % of SIG/CAIQ/HECVAT items.

---

## Need help preparing for Microsoft SSPA or an enterprise tender?

> 📩 **Free 15-minute consultation in Telegram**
> We discuss your situation: where scope hits Sensitive Use, what documents are needed, how to move the AIMS under the carve-out.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [Readiness checklist](./checklist.md)
- [GenAI/LLM-specific controls](./genai-llm-specific-controls.md)
- [Shadow AI Policy template](./shadow-ai-policy-template.md)
- [Vendor Risk Assessment for AI](./vendor-risk-assessment-ai.md)
---

*Sources: Microsoft SSPA homepage; DPR v10 PDF (FY25); SSPA Program Guide v10; SC&H (2024); Schellman (2024); Clark Nuber; AWS Vendor Security Policy; AWS Responsible AI Policy; Google AI Principles (rev. 02/2025); Google Cloud Compliance Center; IBM Supplier Conduct Principles; IBM Trustworthy AI; Salesforce Global Supplier Code of Conduct (06/2025); Salesforce Trusted AI Principles; Oracle Supplier Code of Ethics; ServiceNow Code; Shared Assessments SIG 2025; CSA CAIQ v4.0.2; CSA AICM v1.0 (10 July 2025); CSA STAR for AI 42001 (20 August 2025); EDUCAUSE HECVAT 4.1.5 (10 February 2025); UK ATRS; OMB M-25-21, M-25-22; CCS G-Cloud 15; ISACA AI Governance Benchmark 2025; Pitchbook Q2 2025.*
