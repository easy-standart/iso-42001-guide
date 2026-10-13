# ISO/IEC 42001 ↔ NIST AI RMF, Colorado AI Act and US State Laws

> 🇷🇺 [Читать на русском](./ru/comparison-nist-ai-rmf.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** NIST AI RMF 1.0 is the official US framework — voluntary, but de facto required for federal contractors. NIST's site hosts a **community-submitted crosswalk** that maps the AI RMF's 72 subcategories to clauses and Annex B of ISO/IEC 42001 (published by NIST, not authored by it). The Govern / Map / Measure / Manage structure aligns nearly 1:1 with clauses 4–10 and Annex A. Colorado's SB 24-205 referenced ISO/IEC 42001 as grounds for an affirmative defense, but it was repealed and replaced by SB 26-189 (effective 1 January 2027), which does not carry that reference; several other state bills that named ISO/IEC 42001 failed.

---

## Contents

- [1. NIST AI RMF structure](#1-nist-ai-rmf-structure)
- [2. NIST → ISO 42001 crosswalk](#2-nist--iso-42001-crosswalk)
- [3. NIST status under the Trump administration](#3-nist-status-under-the-trump-administration)
- [4. Colorado AI Act (SB 24-205 → SB 26-189)](#4-colorado-ai-act-sb-24-205--sb-26-189)
- [5. Texas TRAIGA, Virginia, Utah, Illinois, NYC, California, Connecticut](#5-texas-traiga-virginia-utah-illinois-nyc-california-connecticut)
- [6. Consolidated approach](#6-consolidated-approach)

---

## 1. NIST AI RMF structure

NIST AI Risk Management Framework 1.0 was published on 26 January 2023. It is **voluntary** but has become a de facto standard for:
- US federal contractors,
- enforcement guidance at the FTC, CFPB, FDA, SEC, EEOC,
- reference in state laws (Colorado, Texas, Virginia).

Four functions:

- **GOVERN** (6 categories) — policies, procedures, roles, lifecycle risk management.
- **MAP** (5 categories) — context, AI use-case classification, stakeholders.
- **MEASURE** (4 categories) — analysis, monitoring, trustworthiness assessments.
- **MANAGE** (4 categories) — prioritization, response, third parties, documentation.

Additionally — **Playbook, Roadmap, Perspectives, Generative AI Profile (NIST AI 600-1)** and **Cyber AI Profile (NIST IR 8596)**.

---

## 2. NIST → ISO 42001 crosswalk

NIST hosts a public page "Crosswalks to the NIST AI RMF" with a **community-submitted crosswalk "NIST AI RMF → ISO/IEC FDIS 42001 AI Management System Crosswalk"** mapping the AI RMF's 72 subcategories to clauses and Annex B controls of ISO 42001. The document is published on the NIST site but was contributed by the community, not authored by NIST.

Excerpt (full document at NIST AIRC):

| NIST AI RMF subcategory | Content | ISO/IEC 42001 clause / control |
|---|---|---|
| GOVERN 1.1 | Legal/regulatory requirements; respective values | Cl. 4.1, 4.2; A.2.2, A.2.3 |
| GOVERN 1.2 | Trustworthy AI characteristics integrated into policies | Cl. 5.2; A.2.2–A.2.4 |
| GOVERN 1.3 | AI risk prioritization processes | Cl. 6.1.2, 6.1.3; A.5.2–A.5.5 |
| GOVERN 1.4 | Risk monitoring processes documented and resourced | Cl. 9.1; A.6.2.6 |
| GOVERN 1.5 | Risk reassessment processes | Cl. 9.1, 10.2 |
| GOVERN 1.6 | AI systems inventory | B.4.2, B.4.3, B.4.4, B.4.5, B.4.6 |
| GOVERN 1.7 | Decommissioning procedures | B.6.2.6 |
| GOVERN 2.1 | Roles and communication lines documented | Cl. 9.1; A.3.2 |
| GOVERN 2.2 | AI literacy and training | Cl. 7.2, 7.3 |
| GOVERN 2.3 | Executive accountability | Cl. 5.1, 5.3 |
| GOVERN 3.1 | Diversity/equity/accessibility in teams | A.3.2, B.3.2 |
| GOVERN 4.x | Culture, safety, testing | Cl. 7.4; A.2.3 |
| GOVERN 5.x | Stakeholder engagement | A.8.2, A.8.3 |
| GOVERN 6.x | Third parties | A.10.2–A.10.4 |
| MAP 1.x | Context, categorization, intent | Cl. 4.1–4.4; A.5.2, A.6.1.2 |
| MAP 2.x | AI tasks and methods | A.6.2.2 |
| MAP 3.x | Benefits and harms | A.5.3, A.5.4, A.5.5 |
| MAP 4.x | Third-party risks | A.10.2, A.10.3 |
| MAP 5.x | Impact on individuals/groups | A.5.2–A.5.5 |
| MEASURE 1.x | Metrics approach | Cl. 9.1, A.6.2.4 |
| MEASURE 2.x | Trustworthy characteristics measured | Cl. 9.1, A.6.2.4 |
| MEASURE 3.x | Tracking identified risks | Cl. 9.1, A.6.2.6 |
| MEASURE 4.x | Feedback | A.3.3 |
| MANAGE 1.x | Prioritization and response | Cl. 6.1.3, 8.2 |
| MANAGE 2.x | Benefit maximization / harm minimization | A.9.2–A.9.4 |
| MANAGE 3.x | Third-party risks | A.10.2–A.10.4 |
| MANAGE 4.x | Documenting and communicating risk treatments | Cl. 7.5, 10.1 |

**Aggregated mapping:**

- **GOVERN** ≈ clauses 4–6 + most of Annex A.
- **MAP** ≈ clauses 6.1.2 + 6.1.4 + A.5.
- **MEASURE** ≈ clause 9 + A.6.2.4.
- **MANAGE** ≈ clauses 8.2 + 10 + A.9.

---

## 3. NIST status under the Trump administration

AI RMF 1.0 is still in force — NIST has not released "AI RMF 2.0".

Key events 2025–2026:

- **20 January 2025** — Trump revoked Biden EO 14110 (Safe, Secure, and Trustworthy AI).
- **23 January 2025** — EO 14179 signed: "Removing Barriers to American Leadership in AI".
- **23 July 2025** — AI Action Plan "Winning the Race" + three EOs. The plan directs NIST to "revise AI RMF removing references to misinformation, DEI and climate change". The framework itself remains voluntary.
- **11 December 2025** — EO "Ensuring a National Policy Framework for AI", aimed at preempting state laws (except child safety, infrastructure, procurement).
- **Generative AI Profile (NIST AI 600-1)** — published 26 July 2024, still current. March 2025 update added provenance, supply chain, third parties.
- **Cyber AI Profile (NIST IR 8596)** — preliminary draft 16 December 2025; initial public draft expected in 2026.
- **7 April 2026** — NIST published a concept note for an AI RMF Profile on Trustworthy AI in Critical Infrastructure.
- **NIST SP 800-53 Release 5.2.0** (August 2025) — updates under EO 14306 complementing AI RMF.

**Practical implication:** NIST AI RMF remains the de facto standard for US federal contractors. The text may be revised to remove DEI language, but the Govern/Map/Measure/Manage architecture will remain.

---

## 4. Colorado AI Act (SB 24-205 → SB 26-189)

- The original act, SB 24-205, was signed by Governor Polis on 17 May 2024, with an effective date of 1 February 2026.
- That date was pushed to 30 June 2026 (SB 25B-004, August 2025), and then **SB 24-205 was repealed and replaced by SB 26-189** (signed May 2026, effective 1 January 2027). The original act never took effect.
- Applies to developers and deployers of high-risk AI systems substantially affecting consequential decisions in employment, education, finance, healthcare, housing, insurance, legal services, government services.

**Direct references to ISO 42001 and NIST AI RMF (historical — from the original SB 24-205, not carried into the replacement SB 26-189, so ISO/IEC 42001 is no longer a codified defense in Colorado):**

> Affirmative defense / rebuttable presumption: deployer/developer receives affirmative defense in Attorney General actions if:
> 1. it discovered and remediated the violation through feedback, adversarial testing / red teaming, or internal review, AND
> 2. is in overall compliance with "the latest version of the NIST AI Risk Management Framework, Standard ISO/IEC 42001, or any other nationally or internationally recognized framework if substantially equivalent or more stringent", or
> 3. any framework the Attorney General may designate.

**Additional requirements (under the original SB 24-205):**
- Impact assessment — annually at minimum and within 90 days of substantial modification, 3-year retention.
- Notify the Attorney General within 90 days of detecting algorithmic discrimination.
- Enforcement — Attorney General only; no private right of action.
- Penalties — up to $20,000 per violation under the Colorado Consumer Protection Act.

---

## 5. Texas TRAIGA, Virginia, Utah, Illinois, NYC, California, Connecticut

### Texas TRAIGA (HB 149)
Signed by Abbott on 22 June 2025, effective 1 January 2026. Intent-based liability (disparate impact insufficient). **Safe harbor: substantial compliance with NIST AI RMF or Generative AI Profile** (no direct ISO 42001 reference). Penalties $10,000–$200,000. 36-month regulatory sandbox.

### Virginia HB 2094 (High-Risk AI Developer and Deployer Act)
Passed the Assembly in February 2025, **vetoed by Governor Youngkin on 24 March 2025**. The bill contained an explicit reference to NIST AI RMF or ISO/IEC 42001 as a basis for a presumption of compliance. Virginia Executive Order No. 30 (2024) remains the baseline regime for state agencies.

### Utah AI Policy Act (SB 149)
In force since 1 May 2024. Amendments effective 7 May 2025 (SB 226, SB 332, HB 452, SB 271). Sunset extended to 1 July 2027. Focus: GenAI transparency, regulated professions, mental health chatbots, deepfake. Safe harbor: GenAI system must self-disclose its non-human nature. No direct NIST/ISO references.

### Illinois HB 3773
An amendment to the Illinois Human Rights Act. Signed 9 August 2024, effective 1 January 2026. Prohibits using AI that produces discrimination against protected classes; bans ZIP codes as proxies; mandatory notices to employees and candidates. The older Illinois AI Video Interview Act (since January 2020) also applies.

### New York City Local Law 144 (AEDT Law)
In force since 5 July 2023. Annual bias audit by an independent auditor; summary publication on the site; candidate notice at least 10 business days in advance. Penalties $500–$1,500 per day. In December 2025 the NY State Comptroller criticised DCWP for poor enforcement (only 2 complaints, 32 audited companies).

### California
- SB 1047 — vetoed September 2024.
- **AB 2013** (GenAI Training Data Transparency Act) — effective 1 January 2026.
- **SB 942** (AI Transparency Act) — application date moved from 1 January 2026 to 2 August 2026 by AB 853 (13 October 2025) — alignment with EU AI Act.
- **SB 53** (Transparency in Frontier AI Act, TFAIA) — effective 1 January 2026.
- AB 489, SB 243, AB 325 — effective 1 January 2026.
- AB 2930 (Automated Decision Tools) — failed to pass.

### Connecticut SB 2
Failed to pass in 2024 and 2025 due to Governor Lamont's opposition. The 2025 version was already weakened. Would have provided affirmative defense via NIST AI RMF / ISO 42001 compliance.

**Broader context:** in 2024 more than 635 AI bills were proposed in states, ~100 passed. By mid 2025 — more than 921. The federal EO of 11 December 2025 aims to preempt state laws, but the patchwork remains.

---

## 6. Consolidated approach

For organizations operating across jurisdictions (EU, US, Asia), the most resilient foundation:

1. **ISO/IEC 42001:2023** as the core — an internationally recognized certificate that, by common consulting estimates, covers roughly 40–50 % of the EU AI Act and 70 %+ of the NIST AI RMF (these figures are estimates, not regulator-published).
2. **NIST AI RMF** as the US reference. Use the existing NIST crosswalk.
3. **EN 18286:2026** (once cited in the OJ) for presumption of conformity under the AI Act.
4. **Targeted overlays** — GPAI Code of Practice, Singapore AI Verify, China labelling measures — as applicable.

The big saving: by common consulting estimates, AIMS documents and processes can be reused on the order of 70–90 % across these regimes. The differences are mainly in reporting form, marking, and registration.

---

## Need help with a consolidated AI governance strategy?

> 📩 **Free 15-minute consultation in Telegram**
> We map your jurisdictions and assemble a minimal but sufficient document set.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [EU AI Act comparison](./comparison-eu-ai-act.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [Standard overview](./README.md)

---

*Sources: NIST AI RMF 1.0; NIST AI RMF → ISO/IEC FDIS 42001 Crosswalk (AIRC PDF); NIST AI 600-1 Generative AI Profile; NIST IR 8596 Cyber AI Profile draft; Colorado SB 24-205 (NAAG Deep Dive; Davis Wright Tremaine; Gibson Dunn; Schellman/RockCyber; FPF); Texas TRAIGA (Baker Botts; K&L Gates; Latham & Watkins); Virginia HB 2094 (Ogletree; ABA Health Law; Saul Ewing); Utah SB 149 (Manatt; Perkins Coie); Illinois HB 3773 (Seyfarth Shaw; Morgan Lewis; Ogletree); NYC Local Law 144 (NYC DCWP; Deloitte; FairNow; NY State Comptroller Dec 2025); California AB 2013, SB 942, SB 53 (TrustArc; Cooley; Troutman Privacy; King & Spalding); Connecticut SB 2 (LegiScan; FPF; CT Mirror); EO 14110, 14179; AI Action Plan 23.07.2025; EO 11.12.2025.*
