# AI Vendor Risk Assessment: a practical process and questionnaire

> 🇷🇺 [Читать на русском](./ru/vendor-risk-assessment-ai.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** A working process for assessing the AI suppliers *you* rely on — foundation-model APIs, AI features baked into SaaS, fine-tuning vendors, GRC tooling. Six steps plus a ready-to-send questionnaire. This is the mirror image of [supplier-requirements.md](./supplier-requirements.md): that file is how you answer *your* customers; this one is how you vet *your* vendors.
>
> **Where it fits.** ISO/IEC 42001 Annex A control **A.10.3** requires AI suppliers to go through due diligence and monitoring; **A.10.2** requires responsibility to be allocated in supplier contracts. This is the evidence for both.

---

## Contents

- [Why AI vendors need their own assessment](#why-ai-vendors-need-their-own-assessment)
- [Step 1. Inventory your AI vendors](#step-1-inventory-your-ai-vendors)
- [Step 2. Tier them by risk](#step-2-tier-them-by-risk)
- [Step 3. Send the due-diligence questionnaire](#step-3-send-the-due-diligence-questionnaire)
- [Step 4. Score and decide](#step-4-score-and-decide)
- [Step 5. Put it in the contract](#step-5-put-it-in-the-contract)
- [Step 6. Monitor after onboarding](#step-6-monitor-after-onboarding)
- [Red flags](#red-flags)
- [How this maps to Annex A](#how-this-maps-to-annex-a)
- [What to do next](#what-to-do-next)

---

## Why AI vendors need their own assessment

A standard vendor risk assessment asks about uptime, encryption, and SOC 2. Necessary, but blind to what makes AI different. An AI vendor also carries risks a classic questionnaire never surfaces:

- **Training data you cannot see** — provenance, licensing, and whether your inputs get used to train the next model version.
- **Bias and drift** — a model that performs well today can degrade or skew as it is retrained, and you inherit the outcome.
- **Opacity** — you often cannot inspect the model, only its documentation (model cards, system cards).
- **Autonomy** — an agentic tool takes actions, not just returns text. The blast radius is larger.
- **Downstream regulation** — under the EU AI Act, obligations flow along the chain. Your vendor's gaps become your exposure.

The point of this process is to make those risks visible *before* you sign, and to keep them visible after.

---

## Step 1. Inventory your AI vendors

You cannot assess what you have not listed. Count as an AI vendor anything that:

- exposes a model via API (OpenAI, Anthropic, Google, Mistral, open-weight hosts);
- embeds AI features in a SaaS you use (support, analytics, code, HR, marketing);
- fine-tunes, hosts, or evaluates models for you;
- provides AI-governance or GRC tooling that ingests your data.

For each, record: vendor, what the AI does, what data it touches, whether it informs decisions about people, and the internal owner. This inventory feeds control **A.4.3** (data resources) as well as A.10.3.

---

## Step 2. Tier them by risk

Do not send a 60-question form to a vendor whose AI reorders your email. Tier by impact:

| Tier | Trigger | Depth of assessment |
|------|---------|---------------------|
| **High** | Informs decisions about people (hiring, credit, access, moderation), or is autonomous/agentic, or processes sensitive data | Full questionnaire + evidence + contract terms + annual re-assessment |
| **Medium** | Touches customer or business data but does not decide about people | Core questionnaire + certificate check + contract clause |
| **Low** | No sensitive data, no decisions, easily replaceable | Lightweight check: certificate + data-usage terms |

The tier maps directly to how your AI impact assessment (clause 6.1.4 / 8.4) treats systems that depend on that vendor.

---

## Step 3. Send the due-diligence questionnaire

The core of the process. Group the questions so a vendor can route them internally.

### A. Governance and certification
1. Do you hold ISO/IEC 42001, ISO/IEC 27001, or SOC 2? Share the certificate and scope.
2. Who is accountable for AI governance in your organization?
3. Do you follow a recognized AI risk framework (ISO/IEC 23894, NIST AI RMF)?

### B. Training data
4. What data was the model trained on, and under what license or legal basis?
5. Can you demonstrate provenance for training datasets?
6. **Is our data used to train or improve your models? Can we opt out, and is opt-out the default?**

### C. Performance, bias, and testing
7. How do you test for bias and performance across relevant groups?
8. What are the known limitations and failure modes?
9. How often is the model retrained or updated, and how are we told?

### D. Transparency and documentation
10. Do you provide a model card or system card?
11. Can end users tell they are interacting with AI?
12. Can a decision be explained and contested where it affects a person?

### E. Security and operations
13. How is our data encrypted, retained, and deleted?
14. Do you run red-teaming or adversarial testing (prompt injection, jailbreak, data exfiltration)?
15. What is your incident response and notification commitment?

### F. Supply chain
16. Which sub-processors and upstream model providers do you depend on?
17. How do their obligations flow down to us (EU AI Act GPAI, sector rules)?

Adjust depth by tier. High-tier vendors answer all of it with evidence; low-tier vendors answer A and B only.

---

## Step 4. Score and decide

For each answer, mark: **acceptable**, **needs mitigation**, or **unacceptable**. Then land on one of three outcomes:

- **Accept** — risks acceptable, document in the vendor register and the SoA rationale.
- **Accept with mitigation** — proceed, but add contract terms, monitoring, or a compensating control (e.g. no PII to the vendor, human review on outputs).
- **Reject** — the residual risk is too high for the use case. Record why; it is audit evidence too.

Keep the completed questionnaire and your scoring. "Show me the due diligence for vendor X" is a direct A.10.3 audit question.

---

## Step 5. Put it in the contract

Control **A.10.2** wants responsibility allocated in writing. An AI addendum typically covers:

- **Data usage** — your data is not used for training unless you opt in; deletion on termination.
- **Model change notice** — you are notified before material model or behavior changes.
- **Right to audit / evidence** — access to certificates, model cards, and test summaries.
- **Incident notification** — timeline and channel for AI incidents affecting you.
- **Regulatory flow-down** — vendor supports your EU AI Act / sector obligations.
- **Sub-processor control** — notice and objection rights for new sub-processors.

---

## Step 6. Monitor after onboarding

Due diligence is not a one-time gate. For high-tier vendors:

- **Re-assess annually**, or whenever the vendor ships a major model change.
- **Track incidents** the vendor discloses and feed them into your own incident process.
- **Watch the certificate** — expiry or a narrowed scope is a signal.
- **Review the relationship** in your management review (clause 9.3).

---

## Red flags

- "Our data usage is covered in the Terms of Service" — and the ToS lets them train on your inputs by default.
- No model card, no documentation, "the model just works".
- Cannot name their upstream providers or sub-processors.
- No incident notification commitment.
- A certificate whose scope excludes the exact product you are buying.

---

## How this maps to Annex A

| Control | What this process gives the auditor |
|---------|-------------------------------------|
| **A.10.3** Suppliers | Vendor register, completed due-diligence questionnaires, monitoring records |
| **A.10.2** Allocating responsibilities | AI addendum in supplier contracts, supplier RACI |
| **A.4.3** Data resources | Inventory of what data each vendor touches, provenance |
| **6.1.4 / 8.4** Impact assessment | Vendor tier feeding the impact assessment of dependent systems |

---

## What to do next

1. Build the vendor inventory (Step 1) — every model, feature, and tool that touches your data.
2. Tier them (Step 2); most will be low, a few high — spend your effort there.
3. Send the questionnaire to your high-tier vendors this month.
4. Add the AI addendum to your standard procurement contract.
5. Record it all in the vendor register and reference it in your SoA.

---

## Need help vetting your AI stack?

> 📩 **Free 15-minute consultation in Telegram**
> Send us your list of AI vendors. We will tier them by risk and tell you which ones need a full assessment before your next audit.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [AI Supplier Requirements (the other side)](./supplier-requirements.md)
- [Annex A controls explained](./annex-a-controls.md)
- [Shadow AI policy template](./shadow-ai-policy-template.md)
- [AI impact assessment guide (ISO 42005)](./iso-42005-impact-assessment-guide.md)
- [Implementation guide](./implementation-guide.md)

---

*Sources: ISO/IEC 42001:2023 Annex A (A.4.3, A.10.2, A.10.3) and clauses 6.1.4 / 8.4; ISO/IEC 23894 (AI risk management); NIST AI RMF; EU AI Act (GPAI transparency and chain-of-responsibility obligations). Questionnaire structure informed by Shared Assessments SIG and CSA CAIQ practice referenced in supplier-requirements.md.*
