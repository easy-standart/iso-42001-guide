# ISO/IEC 42001 for GenAI and LLM Projects

> 🇷🇺 [Читать на русском](./ru/genai-llm-specific-controls.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **TL;DR.** Projects built on GenAI and LLM APIs (OpenAI, Anthropic, Google, Mistral) do not fit the classical "train a model, monitor drift" logic. Their specifics are prompt injection, hallucination, data leakage via the provider, copyright, and jailbreak. Out of 38 Annex A controls, we consider **14 the most relevant** for them (our assessment, not an ISO classification). This guide shows how to apply them to LLM projects.

---

## Contents

- [1. How GenAI/LLM differs from a 42001 perspective](#1-how-genaillm-differs-from-a-42001-perspective)
- [2. 14 critical controls in focus](#2-14-critical-controls-in-focus)
- [3. A.4 Inventory: documenting API-hosted models](#3-a4-inventory-documenting-api-hosted-models)
- [4. A.5 Impact Assessment: LLM specifics](#4-a5-impact-assessment-llm-specifics)
- [5. A.6 Lifecycle: prompt engineering, RAG, fine-tuning](#5-a6-lifecycle-prompt-engineering-rag-fine-tuning)
- [6. A.7 Data: RAG, embeddings, corporate documents](#6-a7-data-rag-embeddings-corporate-documents)
- [7. A.8 Information for users](#7-a8-information-for-users)
- [8. A.10 Suppliers: what to require from OpenAI, Anthropic, Google](#8-a10-suppliers-what-to-require-from-openai-anthropic-google)
- [9. GenAI readiness checklist](#9-genai-readiness-checklist)

---

## 1. How GenAI/LLM differs from a 42001 perspective

Classical ML systems (e.g., credit scoring) fit 42001 "as is": you train a model on labelled data, validate, deploy, monitor drift.

LLM projects break this logic at several points:

| Aspect | Classical ML | LLM via API |
|--------|---------------|-------------|
| "Training" | You train on your data | You do not train the base model |
| Control over the model | Full | Minimal — provider can change the model |
| Drift | Within your data distribution | External — provider updated the model |
| Data | Under your control | May go to provider (depends on tier) |
| Reproducibility | High | Low — even temperature=0 does not guarantee identity |
| Explainability | Possible (SHAP, LIME) | Practically impossible for the base model |
| Attacks | Adversarial examples | Prompt injection, jailbreak |

These differences require rethinking Annex A controls for GenAI projects.

---

## 2. 14 critical controls in focus

Of the 38 Annex A controls, these are especially important for LLM projects:

| Control | Why critical for LLM |
|---------|----------------------|
| **A.2.2** AI Policy | Must include rules for using external LLMs |
| **A.4.2** Resource register | API-hosted models often missing |
| **A.4.3** Data | RAG datasets and embedding stores are a distinct topic |
| **A.5.2** Impact Assessment | Hallucinations and misuse are LLM-specific |
| **A.5.4** Impact on individuals | Who sees a wrong answer |
| **A.6.2.2** Specification | What is allowed to generate, what is not |
| **A.6.2.4** Verification | LLM eval sets need a specific methodology |
| **A.6.2.6** Monitoring | Not drift — deviation from expected behaviour |
| **A.6.2.7** Documentation | Prompt templates as part of documentation |
| **A.6.2.8** Logging | Full prompts + responses + token usage |
| **A.7.3** Data collection | What enters the context window |
| **A.8.2** User information | Hallucination disclaimers |
| **A.10.3** Suppliers | OpenAI, Anthropic, Google — critical suppliers |
| **A.10.4** Customers | Passing LLM features through to your customers |

---

## 3. A.4 Inventory: documenting API-hosted models

Typical Stage 2 finding: "GPT-4 is in the inventory, but that is not a model — it is an API." Auditors want specifics.

**Minimum fields for an API-hosted model:**

- **Provider:** OpenAI / Anthropic / Google / Mistral / other.
- **Endpoint:** specific API (`gpt-4-turbo-2024-04-09`, `claude-3-5-sonnet-20241022`).
- **Version and pinning:** using "latest" or a pinned version?
- **Use case:** what it is used for (RAG responses, classification, summarisation).
- **Data flow:** what data leaves to the API, what stays with the provider.
- **Tariff/SLA:** free vs. Enterprise tier (important — on free tier data may be used for training).
- **Fallback:** what happens when the API is unavailable.
- **Owner:** who is accountable in the team.
- **Last review date:** typically quarterly.

The inventory is updated on every model change — this is a logged AIMS event.

---

## 4. A.5 Impact Assessment: LLM specifics

An AISIA for an LLM project should explicitly cover:

**Foreseeable misuse:**
- Users perceive the answer as an authoritative source, not a "probabilistic hypothesis".
- Requests for data that should not be in the context window (jailbreak).
- Use of an LLM response in high-risk decisions (medicine, law) without human review.

**Hallucinations:**
- Hallucination rate on your eval sets.
- Which hallucination categories are critical (made-up names, numbers, citations, laws).
- Mitigations: RAG with citations, structured output, human-in-the-loop.

**Bias and fairness:**
- LLM inherits the provider's training data bias — you cannot access it.
- What you can check: bias audit on your use cases with representative samples.

**Privacy:**
- What goes into the prompt (including system prompt).
- What ends up in provider logs.
- GDPR linkage: your prompts may contain customer personal data.

---

## 5. A.6 Lifecycle: prompt engineering, RAG, fine-tuning

42001 was written around classical ML lifecycle. For LLM you need to map:

| 42001 stage (A.6) | What it means for LLM |
|-------------------|------------------------|
| Design objectives (A.6.1.1) | Use case, inputs, outputs, constraints |
| Responsible-development objectives (A.6.1.2) | Hallucination policy, refusal policy, transparency |
| Specification (A.6.2.2) | Prompt templates, structured output schemas, refusal cases |
| Documentation (A.6.2.3) | Versioned prompts, RAG configs, retrieval pipelines |
| V&V (A.6.2.4) | Eval sets (accuracy, hallucination rate, refusal accuracy) |
| Deployment (A.6.2.5) | Canary releases for new prompts, A/B testing |
| Operation and monitoring (A.6.2.6) | Token usage, response quality drift, user complaints |
| Technical documentation (A.6.2.7) | Model card + prompt library + RAG architecture |
| Logs (A.6.2.8) | Full prompt + response + metadata (with privacy in mind) |

**Prompt engineering as part of the AIMS:** every meaningful version of a prompt template should be a commit in a repository, with tests and a changelog. An auditor can ask you to show how prompt changes go through review.

---

## 6. A.7 Data: RAG, embeddings, corporate documents

RAG (Retrieval-Augmented Generation) is a special case. The standard requires data transparency, but in RAG loops data comes from multiple sources.

**What must be in data documentation:**

- **Retrieval sources:** specific repositories, knowledge bases, documents. Legal basis for use.
- **Embedding store:** which embeddings, who generates them, refresh cadence.
- **Chunking strategy:** how documents are split. This affects answer quality.
- **Retrieval pipeline:** retriever (BM25, vector search, hybrid), filters, re-ranking.
- **Context window:** maximum size, what is dropped on overflow.
- **Citation:** does the system return a source link.
- **Access:** who can read, who can modify embeddings.

**Corporate documents:** if RAG uses internal documents, the AIMS must cover the synchronisation process. A document removed from the source system should be removed from the embedding store. Otherwise the LLM keeps "knowing" what it should not.

---

## 7. A.8 Information for users

Control A.8.2 requires users to understand the system's limitations. For LLM that is a **disclaimer** which should:

- Clearly state that GenAI is used.
- Warn about potential hallucinations.
- State that the system does not replace professional advice (for medicine / law / finance).
- Describe what data is collected and where it goes.
- Provide a feedback channel for reporting errors.
- For high-risk use cases — state the right to human review.

**Anti-pattern:** "Powered by AI" in small print at the bottom of the page. An auditor will consider that insufficient.

---

## 8. A.10 Suppliers: what to require from OpenAI, Anthropic, Google

Control A.10.3 is critical for LLM projects. What you must have on file:

| Document | Where to get it |
|----------|-----------------|
| Data Processing Agreement (DPA) | Separate document with Enterprise contract |
| Data handling description (training opt-out) | Provider Privacy Policy, Trust Center |
| Provider compliance certificates (ISO 27001, ISO 42001, SOC 2) | Trust Center |
| Uptime and log-access SLAs | Enterprise contract |
| Subprocessor terms (e.g., AWS as hosting for Anthropic) | DPA addendum |
| Incident notification procedure | Privacy / Security Policy |
| Model deprecation policy (when a model is sunset) | API documentation |

**Free and pay-as-you-go tiers:** data may be used for training. That is a clear nonconformity for Sensitive Use scenarios. For production — only Enterprise tier with training opt-out.

**OpenAI Enterprise, Anthropic Claude Enterprise, Google Cloud Vertex AI** all offer no-training variants. This must be locked in the contract and recorded in the supplier register.

---

## 9. GenAI readiness checklist

Short check for an LLM project:

- [ ] Every LLM API in use is recorded (A.4) with provider, version, use case, tariff.
- [ ] Enterprise tier with a no-training-on-our-data guarantee (or equivalent) is in use.
- [ ] DPA / privacy addendum with provider is signed and retained.
- [ ] Prompt templates are versioned in Git; changes go through review.
- [ ] Eval sets for quality and hallucination rate exist and are run regularly.
- [ ] Prompt + response + token-usage logging is configured; retention ≥ 90 days.
- [ ] AISIA (per 42005) for the LLM system has been completed and approved.
- [ ] Users see an explicit AI disclaimer.
- [ ] A feedback channel for reporting hallucinations is operational.
- [ ] Human-in-the-loop is in place for high-risk use cases.
- [ ] AI-incident response procedure specific to LLM exists.
- [ ] Bias audits on your use cases run on a regular cadence.
- [ ] API fallback (degraded mode) is documented.
- [ ] RAG documentation (if applicable): sources, chunking, retrieval, embedding store.

70 % ✅ — you are ready to present an LLM project to an auditor. Below that — you have a concrete work plan.

---

## Need help with GenAI compliance?

> 📩 **Free 15-minute consultation in Telegram**
> We review your LLM architecture: which controls apply, what to require from the provider, how to assemble a reasonable evidence pack for the audit.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./README.md)
- [ISO 42005 Impact Assessment guide](./iso-42005-impact-assessment-guide.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [Shadow AI Policy template](./shadow-ai-policy-template.md)
---

*Sources: ISO/IEC 42001:2023 Annex A; AWS Security Blog — "AI lifecycle risk management: ISO/IEC 42001:2023 for AI governance"; LayerX Security — "ISO 42001: GenAI Governance & Compliance"; OpenAI Enterprise data handling policy; Anthropic privacy and security documentation; Google Cloud Vertex AI security overview.*
