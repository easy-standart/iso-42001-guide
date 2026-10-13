# Executive FAQ — ISO/IEC 42001

> 🇷🇺 [Читать на русском](./ru/faq.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md) · ✅ [Readiness checklist](./checklist.md)

> **What this is.** Direct answers to 30 questions CEOs, investors, and boards ask when ISO/IEC 42001 first lands on the agenda. No filler. With numbers where they exist.

---

## Contents

- [Business case](#business-case)
- [Cost and timeline](#cost-and-timeline)
- [Team and roles](#team-and-roles)
- [Certification scope](#certification-scope)
- [Technical questions](#technical-questions)
- [Certification and audit](#certification-and-audit)
- [Regulation](#regulation)

---

## Business case

### 1. Who actually needs this certificate?

Companies selling to enterprise customers or hyperscalers with AI features in the product. First in line: Microsoft suppliers (especially if the AI service falls under Sensitive Use), companies selling SaaS in the EU, FinTech and HR-tech with automated decisioning, HealthTech with AI diagnostics. Also any company that wants to compress procurement qualification with large customers — the certificate answers 60–80 % of standard AI-security questionnaires by default.

### 2. Is it already mandatory or not yet?

Legally, in most jurisdictions, **not mandatory**. Commercially, **yes**, for certain segments: Microsoft suppliers in Sensitive Use without the certificate get no Purchase Order; Colorado AI Act references it; EU AI Act compliance is, by common consulting estimates, roughly 40–50 % covered by the certificate. In 12–18 months it will be a standard tender requirement at Fortune 500. In 24–36 months it will be the de-facto standard, the way ISO/IEC 27001 is today.

### 3. What do I lose if I don't certify?

Concretely: contracts that already require it (Microsoft SSPA Sensitive Use). Indirectly: every enterprise deal becomes 4–8 weeks of governance negotiation because you do not have the green tick on the questionnaire. Strategically: a place among the early adopters of a market that has grown from a few dozen certificates in early 2025 to several hundred by 2026 — still early.

### 4. We have no AI in the product, just internal ChatGPT use. Do we need it?

Probably not — but it depends on usage. If employees use AI for drafting, translation, coding — no certification needed. If AI participates in decisions about people (recruiting, evaluation, credit, access) — yes, you need at minimum a formal AI Policy and an impact assessment. If you plan to ship AI features in the product within 12 months, starting earlier is wise so you do not have to catch up.

### 5. Should I start now or wait a year?

Now. The case for waiting: the standard is young (December 2023), interpretations may sharpen. The case for now: being an early adopter is a one-time marketing position — the pool grew from a few dozen certificates in early 2025 to several hundred by 2026; an implementation cycle of 6–12 months means starting a year late risks missing the moment when the certificate becomes mandatory; auditor capacity is forming now and lead times will only grow.

### 6. How does 42001 help in sales?

Three ways. First: you answer security and AI questionnaires (SIG, CAIQ, HECVAT) with prebuilt evidence rather than negotiations. Second: you can answer "ISO/IEC 42001 or equivalent required" RFP clauses without disqualification. Third: a marketing argument — on the website, in the pitch deck, in LinkedIn — particularly strong now, while the certified pool is still in the hundreds rather than the tens of thousands that hold ISO/IEC 27001.

---

## Cost and timeline

### 7. How much does the first certificate cost?

For a typical 50-person SaaS:
- **With existing ISO/IEC 27001:** $80–160 K over the first 3 years (everything: gap, consulting, audit, surveillance, internal time).
- **Without ISO/IEC 27001:** $200–325 K, since the foundational management system is built in parallel.
- **Large corporations (1000+ employees)** with broad scope: $300 K — $1 M+.

These figures are total cost of ownership, not just the auditor's invoice.

### 8. How long does it take?

From project kickoff to certificate:
- Minimum — **3 months** (IBM Granite — narrow scope, mature ISO 27001).
- Typical — **6–9 months** for a SaaS with baseline compliance maturity.
- 12–18 months for large corporations with broad scope.

The certification audit itself is Stage 1 (1–2 days) + Stage 2 (from ~2–5 days for a small company up to several weeks for large enterprises, counted in audit-days) + 4–8 weeks for the report and the CB's decision.

### 9. What does the cost include?

Eight main lines:
1. Gap analysis (external or internal) — $5–25 K.
2. Implementation consulting — $30–120 K.
3. Internal team time (hours × loaded rates) — typically 30–50 % of budget.
4. Tooling (GRC platform, drift monitoring, impact assessment) — $5–40 K/year.
5. Team training (PECB Lead Implementer or equivalent) — $3–10 K.
6. Stage 1 + Stage 2 audit at the CB — $20–80 K.
7. Surveillance audits in Y2 and Y3 — $10–40 K/year.
8. Remediation reserve for audit findings — 10–15 % of budget.

### 10. What drives the price?

Main factors: scope size (one product vs whole company — 3–5× difference), presence of ISO/IEC 27001 (40–60 % savings), documentation maturity, choice of certification body (BSI/DNV more expensive than Coalfire or smaller CBs), region (US/EU CBs typically more expensive than Asian), need for international recognition (IAF accreditation).

### 11. How much do surveillance audits cost?

Each year in Y2 and Y3 — about 30–50 % of the initial audit cost. For a 50-person SaaS: $5–25 K/year. After year 3 — recertification (similar to first audit but typically 20–30 % cheaper).

### 12. Can it be done cheaper or faster?

Yes. Levers: (a) narrow scope — one product or one team; (b) open-source tools (CISO Assistant, VerifyWise) instead of commercial GRC; (c) less expensive IAF-accredited CB; (d) internal AIMS lead instead of external consulting. Realistic minimum: $50–80 K over 4–6 months for a small SaaS with mature ISO 27001.

---

## Team and roles

### 13. Do we need a dedicated AI Governance Lead?

For a company under 100 people — no. A blended role works: CISO + AIMS lead, or Head of Compliance + AIMS lead. Dominant pattern: **0.3–0.5 FTE** blended at start, **0.2–0.3 FTE** in steady state. For 100–250 employees or AI-as-core-product companies, a dedicated lead becomes worth hiring (compensation: $130–220 K/year in EU/US).

### 14. Who should own the AIMS?

C-level or a direct report to the CEO. Most often — CISO (if ISO 27001 is mature), CTO, CPO, or Chief Risk Officer. The standard's hard requirement (Clause 5) is real top-management involvement: not delegation "to IT somewhere", but personal accountability.

### 15. How many FTE for implementation?

Typical breakdown for a 50-person SaaS with operating ISO 27001:
- AIMS lead / project manager: 50–100 % during implementation (3–6 mo), 20–40 % steady state.
- Technical SME (ML lead): 15–25 % during implementation, 5–10 % later.
- Internal auditor (independent): 5–10 % / 2–5 %.
- Executive sponsor (CEO/CTO): 5–10 % / 2–5 %.
- Legal / Privacy / DPO: 10–20 % / 5–10 %.

Total blended: ~1.0–1.6 FTE during implementation, ~0.4–0.7 FTE steady state.

### 16. Can our existing CISO be the AIMS lead?

Yes, and this is the most common working pattern for sub-500 companies. ISO 27001 and 42001 share Annex SL structure; 40–60 % of management system work transfers. Condition: the CISO is willing to absorb AI-specific topics (drift, bias, impact assessment) — usually via a PECB Lead Implementer course (5 days, $1.5–2.5 K) or equivalent.

---

## Certification scope

### 17. Should I certify the whole company or one product?

**One product or one BU.** This is the pattern everyone follows, including Microsoft (separate certificates for M365 Copilot, Azure AI Foundry, Copilot Studio, GitHub Copilot, Dragon Copilot), Anthropic (only Claude API + Enterprise), AWS (Bedrock + Q + Textract). Narrow scope = faster (3–6 months vs 9–18 months), cheaper ($50–150 K vs $300+ K), lower audit failure risk.

### 18. What does "scope" mean in practice?

A 1–3 page document recording: which AI systems / products / services / legal entities / physical sites are in certification, which are not, and why. Example: "Certified AIMS covering development and operation of module X within SaaS product Y, in legal entity Z, on cloud infrastructure W. Out of scope: internal experiments with generative AI for marketing." The auditor verifies exactly what is in scope.

### 19. Can scope be expanded later?

Yes, this is the normal path. At recertification (year 3) or even at a surveillance audit you can add new products. Integral Ad Science did this: initial certificate on a narrow scope, recertification added "Quality Attention" and "Ad Fraud solutions".

---

## Technical questions

### 20. Do we need to redesign our models?

No. The standard does not impose technical requirements on models. It requires **management** processes around them: how you build, test, monitor, and document them. At the model level, you may need to add: an explainability layer (for high-risk systems), drift and bias monitoring, logging, fail-safe mechanisms. This is not "rewriting models" but adding operational controls.

### 21. What is model drift and why must we track it?

Drift is the gradual degradation of a model in production because the distribution of real data diverges from training data. Example: a credit scoring model trained on 2022 data; by 2026 macroeconomic conditions changed and the model starts mis-classifying. The standard (control A.6.2.6) requires continuous monitoring so you catch drift before it triggers an incident. Tools: Fiddler, Arize, Evidently, IBM watsonx.governance, Credo AI.

### 22. What tools will we need?

Minimum:
- **GRC platform** for documentation, registers, SoA: CISO Assistant (open-source, free), VerifyWise (open-source/BSL), Vanta, Drata, Secureframe, OneTrust ($15–80 K/year).
- **Drift and bias monitoring**: Fiddler, Arize, Evidently, or in-house solutions on top of MLflow.
- **Model documentation**: Model Cards, Datasheets — Confluence/Notion will do.
- **AI system register**: an Excel or Airtable sheet works at the start.

You do not need to buy everything up front — Excel + Confluence/Notion + Git is enough to get going.

---

## Certification and audit

### 23. Which certification body should I pick?

It depends on the target market:
- **Globally ANAB/UKAS-accredited:** BSI, DNV, Schellman, A-LIGN, TÜV Rheinland, TÜV Nord, Coalfire, LRQA — for selling in the US and EU.

Pricing: BSI/DNV — premium tier; Schellman/A-LIGN — large US audits; Coalfire — flexible for SaaS; PECB partners — usually cheaper.

### 24. How long does the certificate stay valid?

3 years, like other ISO certificates. Surveillance audits in years 2 and 3 (1–3 days for narrow scope). After year 3 — recertification (full audit, typically 20–30 % cheaper than the first).

### 25. What happens at surveillance?

The auditor visits (or connects remotely) for 1–5 days and verifies: is the system operating, what changed, what incidents occurred, did you respond to them, is documentation current, did you complete the improvement plan from the previous audit. The goal is to confirm the AIMS did not "die" after certification.

### 26. What if we fail the audit?

It depends on the type of finding. **Major nonconformity** — critical deviation, no certificate issued; you must remediate (typically 30–90 days) and retest part of the audit. **Minor nonconformity** — small deviation, certificate is issued, but you must close it before the next surveillance. **Observation** — recommendation, no obligation. Per major auditor data (Schellman, A-LIGN), most first audits land 1–3 minor nonconformities — that is normal.

---

## Regulation

### 27. If I have a 42001 certificate, am I automatically compliant with EU AI Act?

No, but close. By common consulting estimates the certificate covers roughly **40–50 %** of EU AI Act requirements — the organizational layer (risk management, documentation, monitoring, impact assessment). It does not cover: specific data requirements for high-risk systems, mandatory registration with the EU AI Office, sector-specific post-market monitoring obligations. The certificate is an excellent base on which to add the rest at 30–50 % incremental cost.

### 28. What about US requirements?

There is no single federal AI law yet. But: **Colorado AI Act** (SB 205) references ISO/IEC 42001 as the benchmark control set. NYC (Local Law 144 for HR-tech), California (CCPA/CPRA), Utah, Illinois, Texas have AI-specific requirements. **NIST AI RMF 1.0** is voluntary, but federal contractors are expected to apply it. ISO/IEC 42001 is compatible with NIST AI RMF (mapping in `comparison-nist-ai-rmf.md`).

### 29. Should we wait for some new standard?

No. The landscape has stabilized: ISO/IEC 42001 is the foundation; complementary standards (42005 for Impact Assessment, 22989 for terminology, 23894 for risk management) are already published. EU AI Act is law, not a standard, and runs in parallel. Any new standards will be compatible with 42001 because they are produced by the same ISO/IEC JTC 1/SC 42 committee.

---

## Question not answered here?

> 📩 **Free 15-minute consultation in Telegram**
> Describe your situation — I will respond to your specific case. If the question is common, I will add it to this FAQ.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

You can also [open an Issue](https://github.com/easy-standart/iso-42001-guide/issues/new) with your question — it becomes public and helps others.

---

## Read next

- [Standard overview](./README.md)
- [Readiness checklist](./checklist.md)
- [Implementation guide](./implementation-guide.md)
- [Cost and timeline in detail](./cost-timeline.md)
- [ISO 27001 comparison](./comparison-iso-27001.md)
---

*Sources for figures: PECB Lead Implementer course curriculum, public press releases of AWS, Google, Microsoft, Anthropic, IBM, KPMG; certification body pricing data (BSI, DNV, Schellman, A-LIGN, Coalfire); compensation benchmarks (LinkedIn).*
