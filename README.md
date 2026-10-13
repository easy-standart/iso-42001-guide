# ISO/IEC 42001 Guide

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Language](https://img.shields.io/badge/lang-en%20%7C%20ru-blue.svg)](#)
[![Topic: AI governance](https://img.shields.io/badge/topic-AI%20governance-purple.svg)](#)

> 🇷🇺 [Читать на русском](./ru/README.md)

**A practical, vendor-neutral guide to implementing and certifying ISO/IEC 42001:2023 — the world's first AI Management System standard.** No theory padding, no copy-paste from the standard text, no academic detours. Only what an executive or process owner needs to go from decision to certificate.

---

## Why this repository exists

Seven out of ten companies that use AI in their products cannot explain to an auditor how their model makes decisions. Until recently, this was not a problem.

That changed in September 2024.

- **Microsoft** released SSPA DPR v10 with 18 new AI management requirements. Suppliers running AI services classified as Sensitive Use no longer receive a Purchase Order without an ISO/IEC 42001 certificate.
- **AWS, Google Cloud, Anthropic, Microsoft, IBM, KPMG International** — all already certified.
- **EU AI Act** phases in through 2027–2028 (high-risk obligations now apply from 2 December 2027 after the Digital Omnibus). ISO/IEC 42001 covers an estimated 40–50 % of its requirements.
- **US state AI laws** increasingly point to ISO/IEC 42001: Colorado's 2024 AI Act named it as a benchmark (that law was later repealed and replaced), and other state bills reference it too.

The story of ISO/IEC 27001 is repeating itself. Five times faster.

**The question is no longer "will this affect my business". The question is "when".**

### Do you need it now?

Probably yes if any of these are true:

- An enterprise customer or an RFP asks for "ISO 42001 or equivalent".
- You ship AI features to the EU, US or UAE, or sell to regulated industries.
- Investors or a due-diligence process are asking how you govern AI.
- A competitor just got certified and you are losing the "trust" comparison.

If none of these apply yet, bookmark this and come back when you move into enterprise or EU deals.

---

## What's inside

**Start here**

| Section | What you get |
|---------|--------------|
| [Standard overview](./overview.md) | What ISO/IEC 42001 is, who needs it, how it's built, where the value is |
| [Readiness checklist](./checklist.md) | 60+ items: assess how close you are to certification |
| [Executive FAQ](./faq.md) | Cost, timeline, headcount, scope, risks — answers to the key questions |

**Understand the standard**

| Section | What you get |
|---------|--------------|
| [Standard structure](./structure.md) | Clauses 4–10, Harmonized Structure (Annex SL), PDCA, Annexes A/B/C/D |
| [Annex A controls](./annex-a-controls.md) | All 38 controls: what each requires, evidence, common mistakes |
| [Family of AI standards](./family-of-standards.md) | How ISO/IEC 22989, 23053, 23894, 42005, 42006 connect |
| [Glossary](./glossary.md) | AIMS, AI system impact assessment, drift, human-in-the-loop |

**Implement and certify**

| Section | What you get |
|---------|--------------|
| [Implementation guide](./implementation-guide.md) | Step-by-step from decision to certificate |
| [Cost and timeline](./cost-timeline.md) | Real numbers by budget line |
| [Common audit findings](./common-audit-findings.md) | What auditors flag at Stage 1 and Stage 2, and how to avoid it |
| [Certification bodies](./anab-accredited-cbs.md) | Accredited CBs: who they are, geography, fit |
| [Integrated management system](./integrated-management-system.md) | Running 42001 alongside ISO 27001 / 9001 as one system |

**AI-specific risk**

| Section | What you get |
|---------|--------------|
| [GenAI & LLM controls](./genai-llm-specific-controls.md) | Which Annex A controls matter most for LLM-based products |
| [AI impact assessment (ISO 42005)](./iso-42005-impact-assessment-guide.md) | How to run an AI system impact assessment |
| [Shadow AI policy](./shadow-ai-policy-template.md) | Template policy for uncontrolled AI use |
| [AI vendor risk assessment](./vendor-risk-assessment-ai.md) | How to assess third-party AI providers |

**How it maps to other frameworks**

| Section | What you get |
|---------|--------------|
| [vs EU AI Act](./comparison-eu-ai-act.md) | Where the standard overlaps with the regulation |
| [vs NIST AI RMF](./comparison-nist-ai-rmf.md) | For the US market |
| [vs ISO 27001](./comparison-iso-27001.md) | What carries over, real savings |
| [vs SOC 2](./comparison-soc2.md) | How the two differ and overlap |
| [vs prEN 18286](./pren-18286-vs-iso-42001.md) | The upcoming EU harmonised AI standard |

**Market context**

| Section | What you get |
|---------|--------------|
| [Certified companies](./certified-companies.md) | Who is actually certified |
| [Public case studies](./case-studies.md) | How major companies approached certification |
| [Supplier requirements](./supplier-requirements.md) | Microsoft SSPA and equivalents, SIG/CAIQ/HECVAT |
| [Industry guide: SaaS on LLM](./saas-llm.md) | Sector-specific angle for LLM-based SaaS |

**Templates**

| Template | Use |
|----------|-----|
| [AIMS scope statement](./templates/aims-scope-statement.md) | Define the boundaries of your AI management system |
| [AI Policy](./templates/ai-policy.md) | Top-level statement of intent (Clause 5.2, Annex A.2) |
| [Statement of Applicability (SoA)](./templates/statement-of-applicability.md) | All 38 controls: applicable or not, justification, evidence |
| [AI impact assessment](./templates/ai-impact-assessment.md) | Document impact per AI system |
| [AI system card](./templates/ai-system-card.md) | Describe an AI system for governance |
| [AI incident response](./templates/ai-incident-response.md) | Plan for AI-specific incidents |
| [Management review minutes](./templates/management-review-minutes.md) | Record management reviews for audit |

---

## Quick start

1. **Not sure if you need the standard** → [Standard overview](./overview.md)
2. **Want to assess your readiness** → [Checklist](./checklist.md)
3. **Need to answer questions from your CEO or investors** → [FAQ](./faq.md)
4. **Already certified to ISO/IEC 27001 or 9001** → see what carries over: [vs ISO 27001](./comparison-iso-27001.md) · [Integrated management system](./integrated-management-system.md)

---

## Who this is for

- Suppliers to Microsoft, AWS, Google Cloud and other hyperscalers shipping AI features
- SaaS companies exporting AI products to the EU
- FinTech, HR-tech, HealthTech, EdTech, LegalTech with AI inside the product
- Series A+ startups selling to enterprise customers
- Companies already certified to ISO/IEC 27001 — your path to 42001 is an estimated 40–60 % shorter
- CEO, CTO, CISO, CPO, Head of Compliance, AI Governance Lead

---

## Need help?

**Start free, on your own.** Most of the "do we need it / what will it cost / how long" questions are answered in the [readiness checklist](./checklist.md) and the [executive FAQ](./faq.md).

**Prefer to talk it through?** A free 15-minute Telegram consult, no obligation:

> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)
>
> We cover whether you need the certificate now, how to scope it, what resources it takes, what carries over from ISO/IEC 27001, and which certification body fits your market.

After that, you either continue on your own using this repository, or we discuss an engagement.

---

## Support the project

- ⭐ **Star this repo** — it improves search visibility and helps others find it
- 🐛 **Found an error or inaccuracy** → [open an Issue](https://github.com/easy-standart/iso-42001-guide/issues/new)
- ✍️ **Want to suggest a topic** → [Discussions](https://github.com/easy-standart/iso-42001-guide/discussions)
- 🌍 **Help translate** to another language → [Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## License and disclaimers

- **Content:** [Creative Commons BY-SA 4.0](./LICENSE) — free to reuse with attribution.
- **Does not reproduce** the text of ISO/IEC 42001:2023. This is independent interpretation. The official text is owned by ISO/IEC and must be purchased at [iso.org](https://www.iso.org/standard/81230.html).
- **Not** legal, regulatory, or formal certification advice. Certification decisions should be made with an accredited certification body.
- Sources are cited in each document. If you spot an inaccuracy, please open an Issue.

---

*Last updated: see commit history.*
