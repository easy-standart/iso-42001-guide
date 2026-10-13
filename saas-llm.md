# SaaS built on LLM APIs (OpenAI, Anthropic, Google) + ISO/IEC 42001

> 🇷🇺 [Читать на русском](./ru/saas-llm.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./overview.md)

> **TL;DR.** Most modern SaaS startups build AI on top of foundation models via API: OpenAI, Anthropic, Google, Mistral. Under ISO/IEC 22989 §5.19 such SaaS simultaneously plays the **AI Customer** role (consuming an LLM) and **AI Producer/Provider** (building its own product). ISO 42001 certification for wrappers is possible — see Anthropic, Evisort, UiPath, Snowflake, FloQast. Key specifics: scope to the application layer (not the foundation model), correct use of Annex A.10 (third parties), Shared Responsibility Model per CSA AICM v1.0.

---

## Contents

- [1. Role mapping per 22989](#1-role-mapping-per-22989)
- [2. Scoping strategies](#2-scoping-strategies)
- [3. Annex A.10 and upstream flow-down](#3-annex-a10-and-upstream-flow-down)
- [4. Upstream provider terms](#4-upstream-provider-terms)
- [5. Certified LLM-SaaS cases](#5-certified-llm-saas-cases)
- [6. CSA AICM v1.0 and Shared Responsibility Model](#6-csa-aicm-v10-and-shared-responsibility-model)
- [7. Reference SoA template for LLM-SaaS](#7-reference-soa-template-for-llm-saas)

---

## 1. Role mapping per 22989

| Stack layer | Example | ISO/IEC 22989 role |
|-------------|---------|---------------------|
| Foundation model provider | OpenAI, Anthropic, Google, Mistral, Cohere, Meta | AI Producer (and partially AI Provider via API) |
| Cloud hyperscaler reselling the LLM | AWS Bedrock, Azure OpenAI Service, Google Vertex AI | AI Platform Provider |
| SaaS built on LLM (RAG, fine-tuning, prompt engineering, guardrails) | Evisort, FloQast, Eightfold, Noxtua | **AI Customer + AI Producer/Provider** |
| Corporate SaaS buyer | Bank, clinic, retailer | AI Customer |
| End user | Bank employee / clinician / shopper | AI User |
| Person affected by a decision | Loan applicant / patient / candidate | AI Subject |

**Anthropic certified as "AI producer, AI developer, AI product and service provider"** — the template for SaaS doing meaningful engineering.

---

## 2. Scoping strategies

| Strategy | What's in | Pros | Cons |
|----------|-----------|------|------|
| **Full-stack** | Foundation model + RAG + application | Maximum "covered surface" | The organization does not control the foundation model ⇒ certification risk |
| **Application layer (recommended)** | Own fine-tuning, RAG ingestion, prompt engineering, guardrails, monitoring, content filtering, incident management | Realistic, auditable scope | Requires a clean SoA with A.10 exceptions |
| **Deployer-only** | Company does not modify the model, only uses it | Minimal obligations | Limited certification value |

Schellman and other CBs **recognize the "AI Producer + Provider" role even for wrappers** when the organization performs substantive engineering: fine-tuning, RAG, prompt engineering, safety classifiers. Evisort received ISO 42001 as an AI producer/provider in exactly this model.

---

## 3. Annex A.10 and upstream flow-down

Annex A.10 (resources for AI systems / third-party AI) requires:

- **A.10.2** — supplier processes and practices (due diligence before selecting a foundation-model provider).
- **A.10.3** — allocation of responsibilities (shared-responsibility matrix).
- **A.10.4** — supplier agreements (contractual requirements in ToS).

**Frequent mistake:** "We are certified because our LLM provider is certified."

**This is wrong.** ISO 42001 certifies an organizational management system; it does not propagate transitively. The organization itself must:

1. Run AISIA on its own implementation.
2. Define an SoA where the upstream model is out of direct control but covered via A.10.
3. Confirm the supplier contract reflects requirements (data retention, training opt-out, incident notification).

---

## 4. Upstream provider terms

| Provider | Key provisions |
|----------|----------------|
| **OpenAI Enterprise Terms** | API inputs/outputs not used for training by default; data residency (EU, US, JP, UK, AU, KR, AE etc.); Zero Data Retention (ZDR) available to eligible enterprise projects with approval; Enterprise Key Management (BYOK); HIPAA via BAA for ZDR projects |
| **Anthropic Commercial Terms** | Prompts/outputs not used for training; SOC 2 Type II; ISO 42001 since 6 January 2025; HIPAA BAA |
| **Azure OpenAI Service** | Default 30-day retention for abuse monitoring; ZDR (Modified Abuse Monitoring) gated, requires EA/MCA and approval by Microsoft MAR team; 3 deployment types (Global, DataZone, Regional) with different data residency; HIPAA BAA via Microsoft Online Services DPA |
| **Google Vertex AI** | Inputs not used for foundation-model training; data residency by region |
| **AWS Bedrock** | Inputs not used for training; AWS controls PCI DSS, HIPAA BAA, FedRAMP |

These terms must be in the supplier register and reviewed at minimum annually.

---

## 5. Certified LLM-SaaS cases

- **Anthropic** — 6 January 2025, Schellman. Scope: "AI Research & Development and AI Services, AI producer + AI developer + AI product and service provider".
- **Snowflake** — one of the first cloud data companies. AI stack: Snowflake Cortex AI, routed through Azure OpenAI, Anthropic, Meta, Mistral.
- **UiPath** — ISO/IEC 42001:2023, Schellman. Multi-LLM routing (Azure/AWS/Google/Anthropic) with AI Trust Layer.
- **Evisort** — one of the first AI companies with ISO 42001. Role "AI producer and provider"; built-in LLM for contracts.
- **FloQast** — accounting AI, January 2025, Schellman. Used its own FloQast Compliance Management to collect evidence.
- **Workday, Eightfold** — see HR-tech.
- **StackAware, Noxtua (legal AI), Xayn** — publicly stated movement toward ISO 42001.

Details in [`case-studies.md`](./case-studies.md).

---

## 6. CSA AICM v1.0 and Shared Responsibility Model

**Cloud Security Alliance AI Controls Matrix (AICM)** — the first vendor-agnostic control framework for cloud AI, released 10 July 2025.

- **243 controls across 18 domains.**
- **Shared Security Responsibility Model (SSRM)** distributes responsibility across 5 roles:
  - **CSP** — Cloud Service Provider (AWS, Azure, GCP).
  - **MP** — Model Provider (OpenAI, Anthropic, Google).
  - **OSP** — Orchestrated Service Provider (Bedrock, Azure OpenAI Service).
  - **AP** — Application Provider (your SaaS).
  - **AI Customer** — end client.
- Mapping to ISO 42001, ISO 27001, NIST AI RMF 1.0, BSI AIC4 released August 2025. Mapping to EU AI Act — later.
- Companion **AI-CAIQ** — foundation for the upcoming STAR for AI certification.

For ISO 42001, a SaaS supplier can use AICM as the "operational layer" under Annex A: CSA controls answer "how", Annex A answers "what must be confirmed".

---

## 7. Reference SoA template for LLM-SaaS

| Annex A control | Applicable | Rationale | Owner |
|------------------|------------|-----------|--------|
| A.2.2 AI Policy | Yes | Company publishes a Responsible AI Policy | Application Provider (AP) |
| A.3.2 Roles | Yes | Chief Responsible AI Officer, AI Review Board | AP |
| A.5.2 AISIA | Yes | AISIA template referencing EU AI Act FRIA | AP |
| A.6.2.2 Objectives | Yes | Per AI feature | AP |
| A.6.2.3 Design and development | Partial | Foundation model out of scope; fine-tuning, RAG, prompts in scope | AP (in-scope); Model Provider (upstream) |
| A.6.2.4 V&V | Yes | Red teaming, output safety, hallucination rate | AP |
| A.6.2.5 Deployment | Yes | CI/CD pipeline, canary releases | AP |
| A.6.2.6 Operation / monitoring | Yes | Observability, drift detection | AP |
| A.6.2.7 Updates | Yes | Change management | AP |
| A.6.2.8 Re-evaluation | Yes | Annual review | AP |
| A.7.2 Data for AI | Partial | Own data — full control; foundation-model training data — out of scope, justified via A.10 | AP |
| A.7.3–A.7.6 Data sources, quality, lineage, preparation | Yes (own data) | Own data documented in detail | AP |
| A.8.2–A.8.5 Information for stakeholders | Yes | User-facing disclosures, AI disclaimer, channels for AI subjects | AP |
| A.9.2–A.9.4 Use of AI | Yes | Acceptable Use Policy for customers | AP |
| A.10.2 Supplier processes | Yes | Due diligence on OpenAI/Anthropic/Google | AP |
| A.10.3 Allocation of responsibilities | Yes | Shared responsibility matrix | AP + MP |
| A.10.4 Supplier agreements | Yes | DPA with opt-out, ZDR, HIPAA BAA | AP |

Per-control deep dive — [`annex-a-controls.md`](./annex-a-controls.md).

---

## Need help scoping an LLM-SaaS under 42001?

> 📩 **Free 15-minute consultation in Telegram**
> We work through your architecture, roles, scope statement, and SoA — what to include, what to push into A.10, what upstream contracts you need.
>
> 👉 [Message in Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Read next

- [Standard overview (42001)](./overview.md)
- [GenAI/LLM-specific controls (deep dive)](./genai-llm-specific-controls.md)
- [Shadow AI Policy template](./shadow-ai-policy-template.md)
- [Cases: Anthropic, Evisort, FloQast, UiPath](./case-studies.md)
- [Microsoft SSPA supplier requirements](./supplier-requirements.md)

---

*Sources: ISO/IEC 22989:2022 §5.19; Anthropic Certificate (Schellman, 6 January 2025); Schellman; Sensiba; OpenAI Enterprise Terms; OpenAI Data Controls; Anthropic Commercial Terms; Microsoft Azure OpenAI Service Q&A; Microsoft Modified Access Review; Google Vertex AI; AWS Bedrock; CSA AI Controls Matrix v1.0 (10 July 2025); Tripwire; AIGL blog; PR Newswire (Evisort); GlobeNewswire (FloQast); Snowflake; UiPath; StackAware; Noxtua; Xayn; Oxebridge.*
