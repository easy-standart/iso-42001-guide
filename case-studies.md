# Public ISO/IEC 42001 Certification Case Studies

> 🇷🇺 [Читать на русском](./ru/case-studies.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** Detailed walk-through of 10+ publicly confirmed ISO/IEC 42001 certifications with sources: press releases, Trust Centers, auditor articles. What was certified, scope, timelines, certification body, team, what was already in place, and what was built specifically for the standard. For the short list see the [certified companies registry](./certified-companies.md).

---

## Contents

- [1. Anthropic (Schellman, January 2025)](#1-anthropic-schellman-january-2025)
- [2. AWS (Schellman, November 2024)](#2-aws-schellman-november-2024)
- [3. Google Cloud (December 2024)](#3-google-cloud-december-2024)
- [4. Microsoft 365 Copilot, Azure AI, GitHub Copilot (Mastermind/IAS, 2025)](#4-microsoft-365-copilot-azure-ai-github-copilot-mastermindias-2025)
- [5. Workday (Schellman, 2025)](#5-workday-schellman-2025)
- [6. Synthesia (A-LIGN, September 2024)](#6-synthesia-a-lign-september-2024)
- [7. IBM Granite (Schellman, September 2025)](#7-ibm-granite-schellman-september-2025)
- [8. Cognizant (DNV, December 2024)](#8-cognizant-dnv-december-2024)
- [9. KPMG International (Schellman, December 2025)](#9-kpmg-international-schellman-december-2025)
- [10. Augment Code (quantitative case)](#10-augment-code-quantitative-case)
- [11. Common patterns of success](#11-common-patterns-of-success)
- [12. Incident case: Denmark's CPR register and AI-written code (2026)](#12-incident-case-denmarks-cpr-register-and-ai-written-code-2026)

---

## 1. Anthropic (Schellman, January 2025)

**Certificate issued** 6 January 2025, valid through 5 January 2028. Issuer: Schellman Compliance, LLC (ANAB-accredited). Signed by Danny Manimbo, Principal, Schellman.

**Scope** (quote):
> "AIMS supporting the AI Research & Development and AI Services for AIMS in the roles as an AI producer as an AI developer and an AI product and service provider, in accordance with statement of applicability, version 1.3, dated November 7, 2024."

**Products covered:** Claude.ai Team Plan, Claude.ai Enterprise Plan, Claude API, Claude Mobile Apps, AI R&D including partner-delivered models (Bedrock, Vertex AI).

**Important for FAQ:** Anthropic explicitly states the certificate applies **only to commercial products** (Claude for Work, API). Consumer plans (Claude Free, Pro, Max) are covered separately — an example of selective scope.

**Team:** Jared Kaplan as Responsible Scaling Officer. About 8 % of employees in security-adjacent areas; pure AI governance is smaller.

---

## 2. AWS (Schellman, November 2024)

**Certificate:** 11 November 2024. Issuer: Schellman. Surveillance audit November 2025 — **no findings**.

**Scope:** Amazon Bedrock, Q Business, Textract, Transcribe. Only these 4 services, not all of AWS.

**Cascade effect:** Tim Tutt (Snowflake): "Knowing AWS has ISO 42001-certified services gives us confidence... and builds our customers' trust in our products."

**Technical foundation:** AWS Responsible AI Framework across 8 dimensions (fairness, explainability, privacy & security, safety, controllability, veracity & robustness, governance, transparency). AWS publicly calls ISO 42001 a "foundational standard".

---

## 3. Google Cloud (December 2024)

**Scope:** GCP, Workspace, Gemini app (NOT all of Alphabet). Per industry trackers — 10 products including Vertex AI and Document AI APIs.

**Direct quote from Google:** "No other generative AI offering has met this level of recognition." Subsequent FedRAMP High authorization — first for generative AI productivity in US public sector.

**Certificates published** in Cloud Compliance Center.

---

## 4. Microsoft 365 Copilot, Azure AI, GitHub Copilot (Mastermind/IAS, 2025)

Microsoft uniquely uses **multiple parallel certificates**, each with its own SoA:

| Product | CB | Date |
|---------|-----|------|
| Microsoft 365 Copilot | Mastermind (IAS) | March 2025 (through March 2028), certificate №MMIND-25032001 |
| Azure AI Foundry + Security Copilot | Mastermind | 2025 |
| Copilot Studio | Mastermind (IAS) | 2025 |
| Dragon Copilot, Foundry, GitHub Copilot | various | 2025 |

**Scope for M365 Copilot:** "Management system supporting M365 Copilot and M365 Copilot Chat offerings; M365 Trusted Platform, Responsible AI, Security, Privacy teams; AI Developer and AI Provider roles; SoA v2.0".

**Additionally:** Microsoft was the first to obtain CSA STAR for AI 42001 Level 2 — industry-first.

**Team:** Natasha Crampton, Chief Responsible AI Officer. About 350 people on Responsible AI work (129 full-time per 2023 data, now larger). Hub-and-spoke: Office of RAI + AETHER (research) + Responsible AI Council led by Brad Smith and Kevin Scott.

---

## 5. Workday (Schellman, 2025)

**Certificate №1355199-2**, issued 2025 (three-year validity).

**Scope** (quote): "AIMS supporting the following product lines: HCM, Financial Management, Student, Spend Management, Adaptive Planning, Peakon, Payroll, Workforce Management, Talent Management, Analytics & Reporting, HiredScore, Platform & Product Extensions; AI Producer and AI Provider roles; SoA v2025.02 dated 1 July 2025; sites: Pleasanton, Boulder, Atlanta, Beaverton, Vancouver BC, Dublin, London, Tel Aviv".

**12 product lines** in one certificate. Workday serves >60 % of Fortune 500 — the certificate becomes a gating credential for Fortune 500 procurement.

**Team:** Kelly Trindel, dedicated RAI team since 2022, supplemented by a network of "RAI champions" across BUs. Oversight from the RAI Advisory Board under CLO Rich Sauer.

---

## 6. Synthesia (A-LIGN, September 2024)

**Certificate:** 25 September 2024, A-LIGN. Initially without accreditation, "lifted" after a witness audit by ANAB in October 2024.

**Scope:** AI video platform.

**Context:** 65 000 customers, 70 % of Fortune 100 in the customer base.

**Direct quote** from Martin Tschammer, Head of Security:
> "Certification drew media coverage and significant interest from customers, vendors, and other stakeholders."

**Team:** Martin Tschammer + Security Manager Nicolás Barberis. No dedicated AI-governance team publicly mentioned — security team plus Wiz, Vanta, A-LIGN.

**Audit prep:** 1 FTE × 4 weeks on top of mature ISMS (Modulos/Xayn model).

---

## 7. IBM Granite (Schellman, September 2025)

**Certificate:** mid-September 2025, for Granite open-source LLM (Apache 2.0 license). Announced together with the Granite 4.0 release in October 2025.

**Scope:** Only the Granite family of language models as AI Producer (AI developer). Not the entire watsonx.ai platform.

**"3 months" claim — critical interpretation:**
> "The process was completed in under three months and resulted in zero non-conformities" (IBM press release).

"3 months" = from **audit kickoff to certification decision**, not "from zero to certificate". IBM already had a mature governance system, ISO 27001/27017/27018/27701, a Responsible AI program, watsonx.governance, and strong SDLC practices.

**Realistic timelines:**
- Mature company with ISMS/PIMS: 3–6 months.
- From scratch: 6–12 months.
- Startup with informal processes: 9–18 months.

**Quotes:**
- David Cox, VP AI Models, IBM Research: "We're honored to earn ISO 42001 certification for our flagship Granite models. Granite is now the first open model family to meet that bar."
- Avani Desai, CEO Schellman: "IBM has now set an important precedent for how transparency, accountability, and innovation can coexist."

**Surrounding measures:** cryptographic signing of Granite 4.0 checkpoints on Hugging Face, bug bounty via HackerOne (up to $100 000), unlimited indemnity for IP claims when using Granite in watsonx.ai.

---

## 8. Cognizant (DNV, December 2024)

First global IT-services company. Rolled out to **300 000+ employees** and launched a client-certification consulting line — direct revenue stream.

**Motives (HFS Research):** competitive differentiation, client trust, regulatory anticipation.

---

## 9. KPMG International (Schellman, December 2025)

First Big Four at the international level.

**Quote** from Steve Chase, Global Head of AI: "Scaling AI and governance go hand in hand."

Positioned explicitly as a "necessary precursor to delivering AI assurance services to clients" — revenue link.

---

## 10. Augment Code (quantitative case)

A case with **vendor-reported numbers** (single source: YSecurity case study — treat as indicative):

- **7-figure deal closed in 93 days** after certification.
- **CAC -64.9 %**.
- **Security calls 6→2/week**.
- **Enterprise deal closed in 2 days** after certification.

The most quantitatively confirmed public ROI case as of 2026.

---

## 11. Common patterns of success

What successful certifications have in common:

### Narrow, clear scope
With the exception of Anthropic (organizational-functions wording), all large certifications scope by product/service. Microsoft is unique with multiple parallel certificates.

### Mature ISO 27001 baseline or equivalent
IBM, Workday, Anthropic — all had mature ISMS/security/governance. Cuts timeline by 40–60 %.

### CISO/Head of Security as AIMS lead
Synthesia (Martin Tschammer), Evisort (CTO Amine Anoun). A dedicated AI Governance Officer — only in Microsoft and other big tech.

### Fractional advisor or external CB preparation
All used external gap analysis, fractional advisor, or partner consulting. Pure in-house from scratch is rare.

### Scope expansion at recertification
Integral Ad Science (February 2026) — initial cert + scope expansion at recertification adding "Quality Attention" and "Ad Fraud solutions". Microsoft — separate certificates for each new Copilot product.

### Certificate transparency
All published a Trust Center or public certificate. Part of the marketing value.

---

## 12. Incident case: Denmark's CPR register and AI-written code (2026)

Cases 1–10 show who got certified. This one is an incident, and an honest one: ISO/IEC 42001 would **not** have stopped this attack, because the AI was on the attacker's side. We include it for what it says about AI inside your own company. The investigation is still going, and details may change.

**What happened.** From 10 September 2026 a bulk extraction ran through the legitimate access of a small IT contractor (Pays ApS) to Denmark's central population register. Names, addresses and personal ID numbers of about **8.8 million people** were obtained, with more than **14 million** query attempts over roughly ten days. The register itself was not hacked: every request was formally within the contractor's rights, there were just far too many. It was noticed on 2 October, not by a security system but by an unusually large bill for the queries.

**The AI part.** According to the hacker (Politiken, via TV 2 Fyn), the program for the mass queries was written by AI, and two experts who saw the code agreed. The hacker says any model of the last year could have done it. Not confirmed by the authorities. The code had a mistake: it searched for people born in 1877 instead of 1977.

**Why this matters for an AIMS.** If one person with an AI-written script can make 14 million queries, the same is possible from inside your company: an employee, a contractor, or an AI assistant already connected to client data (a chatbot, a CRM assistant, support automation). In practice that is a contractor with a key: fast, round the clock, and nobody asks who is responsible for it. This is the situation ISO/IEC 42001 is built for. Annex A asks you to:

- assign a responsible owner for each AI system and define what it is intended for (A.3 internal organization, A.9 use of AI systems);
- keep logs of what it does and monitor its behaviour in production, so a thousandfold growth in requests is seen by you, not by an invoice (A.6 AI system life cycle);
- check suppliers of AI services that receive your data (A.10 third parties and customers);
- set rules for how employees use AI, including external services (A.9).

Details per control: [Annex A controls](./annex-a-controls.md). The information-security side of the same story (passwords, offboarding, supplier monitoring) is covered by ISO/IEC 27001. The two standards share one structure, so they are easy to build together: [Integrated management system](./integrated-management-system.md).

Sources:

- [TV 2 Fyn – artificial intelligence used in the leak](https://www.tv2fyn.dk/fyn/kunstig-intelligens-blev-brugt-i-omfattende-cpr-laek-e6a7e) (in Danish).
- [DR/Ritzau – 1,039 companies receive stricter security requirements](https://www.dr.dk/nyheder/politik/1039-virksomheder-har-faaet-indskaerpet-sikkerhed-efter-cpr-laek) (in Danish).
- [Copenhagen Post – "123456" password used in the CPR breach](https://cphpost.dk/2026-10-10/general/123456-password-used-in-massive-danish-cpr-data-breach/).
- [CSIS – analysis of the CPR breach](https://www.csis.com/csis-tech-blog/the-hub/cpr-breach-denmark).

---

## What does NOT work (typical mistakes)

- Excluding high-risk systems to ease the audit (auditor red flag).
- Vague scope that becomes audit-unfalsifiable.
- Ignoring third-party AI components (OpenAI API, Anthropic, Google) in the supplier register.
- Lack of AI inventory automation.
- "Shelfware AIMS" — formal documents without operating processes.

More in [top 15 common audit findings](./common-audit-findings.md).

---

## Need help preparing for certification?

> 📩 **Free 15-minute consultation in Telegram**
> We work through your situation against the most relevant case: scope, team, 27001 baseline, CB choice.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Certified companies registry](./certified-companies.md)
- [Accredited certification bodies](./anab-accredited-cbs.md)
- [Top 15 common audit findings](./common-audit-findings.md)
- [Cost and timeline](./cost-timeline.md)

---

*Sources: press releases from Anthropic, AWS, Google Cloud, Microsoft, Workday, Synthesia, IBM, Cognizant, KPMG; Schellman, A-LIGN, BSI, Mastermind, DNV; HFS Research; Tibor Blaho (Threads); IBM Think; Anthropic Privacy Center; AWS Trust Center; Google Cloud Compliance Center; Microsoft Trust Center; Workday Trust; Synthesia case studies; YSecurity (Augment Code); Vanta case study (Factory); Modulos/Xayn; Forbes (AI Alliance); ISACA; A-LIGN benchmark 2025.*
