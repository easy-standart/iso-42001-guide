# Template: AI System Card

> 🇷🇺 [Читать на русском](../ru-templates/ai-system-card.md) · ⬅ [Back to home](../README.md)

> **What this is.** A structured AI system card template for the resource register (ISO/IEC 42001 control Annex A.4.2). Filled in by the system owner. Stored in the AIMS register. Auditors ask for it first — it is the most basic artefact.

> **How to use it.** Copy the section below into Markdown or Google Doc / Notion for each AI system. Replace `[bracketed]` placeholders with your data. Fields marked ✓ are mandatory for audit.

---

```markdown
# AI System Card: [System name]

**Card ID:** AIS-[NUMBER]
**Version:** 1.0
**Created:** [YYYY-MM-DD]
**Last updated:** [YYYY-MM-DD]
**Next review:** [YYYY-MM-DD]
**Status:** [Production / Pilot / Development / Decommissioned]

## 1. Identification ✓

- **Name:** [Business-friendly name]
- **Internal ID:** [Register code]
- **System type:** [Classical ML / GenAI on API / GenAI fine-tuned / Hybrid / RPA + AI]
- **Business function:** [Marketing / Sales / HR / Finance / R&D / Operations / Customer Support / etc.]
- **Purpose:** [1–2 sentences on why the system exists]
- **System owner:** [Name, role]
- **Technical lead:** [Name, role]
- **Executive sponsor:** [Name, role]

## 2. Architecture and components ✓

- **Base model / algorithm:** [GPT-4-turbo / Claude 3.5 Sonnet / Random Forest / Custom CNN / etc.]
- **Model provider (if external):** [OpenAI / Anthropic / Google / Mistral / Hugging Face / In-house]
- **Endpoint / version:** [Specific API version, e.g., `gpt-4-turbo-2024-04-09`]
- **Pinning:** [Pinned version or `latest`]
- **Architecture diagram:** [Link in repo / Confluence / Miro]
- **Frontend:** [Where users interact]
- **Backend / orchestration:** [Stack: Python, FastAPI, LangChain, etc.]
- **Storage / databases:** [What data goes where]
- **Embedding store (for RAG):** [Pinecone / Weaviate / pgvector / etc.]

## 3. Data ✓

- **Training data:** [Sources, if applicable. Otherwise — "Not trained"]
- **Inference data:** [What goes in at production time]
- **Output data:** [What the system produces]
- **Personal data categories:** [Email / name / phone / financial / medical / biometric / none]
- **Legal basis (GDPR):** [Consent / Contract / Legal obligation / Vital interests / Public task / Legitimate interests]
- **Data storage regions:** [EU / US / Multi-region]
- **Data retention:** [User data retention period]
- **Data lineage:** [Link to data flow diagram]

## 4. Use cases and limitations ✓

- **Intended use:** [What the system is for]
- **Out of scope (what it must NOT do):** [List of disallowed uses]
- **Foreseeable misuse:** [How the system might be misused]
- **Target audience:** [Who the users are]
- **Affected parties:** [Who receives system decisions]

## 5. Risks and oversight level ✓

- **Risk classification:** [High-risk / Medium-risk / Low-risk / Minimal]
- **Classification rationale:** [Short explanation]
- **EU AI Act classification:** [Prohibited / High-risk Annex III / Limited risk / Minimal risk / Not applicable]
- **Human oversight level:** [Human-in-the-loop / Human-on-the-loop / Human-in-command]
- **Rationale for the level:** [Why this level]
- **AISIA reference:** [Link to AI System Impact Assessment]
- **Risk register entry:** [Link to risk register record]

## 6. Quality and monitoring

- **Eval sets:** [Description of test data and metrics]
- **Key metrics:** [Accuracy / F1 / Hallucination rate / Latency / etc.]
- **Target thresholds:** [Threshold per metric]
- **Drift monitoring:** [Tool: Fiddler / Arize / Evidently / custom]
- **Review cadence:** [Daily / Weekly / Monthly / Quarterly]
- **Alerting triggers:** [Conditions for alerts]
- **Bias audit:** [Cadence + last run date]

## 7. Logging

- **What is logged:** [Prompts / responses / metadata / errors]
- **Where:** [Logging system]
- **Retention:** [Log retention period]
- **Access:** [Who can read]
- **Immutability:** [Tamper-proofing measures]

## 8. Documentation and transparency

- **Technical documentation:** [Link]
- **User-facing documentation:** [Link]
- **AI disclaimer to user:** [Text or link to UI component]
- **Feedback channel:** [Email / form for reports]
- **Appeal process:** [How a user can contest a decision]

## 9. Third parties (for systems built on external APIs)

- **Provider:** [OpenAI / Anthropic / Google Cloud]
- **Tier:** [Free / Pay-as-you-go / Enterprise]
- **Training opt-out confirmed:** [Yes / No, link to contract]
- **DPA signed:** [Yes / No, date]
- **Subprocessors:** [E.g., AWS as hosting for Anthropic]
- **Last vendor review date:** [YYYY-MM-DD]

## 10. Lifecycle

- **Production launch date:** [YYYY-MM-DD]
- **Planned sunset:** [YYYY-MM-DD or "N/A"]
- **Decommissioning procedure:** [Link]
- **Next AISIA review:** [YYYY-MM-DD]
- **Next bias audit:** [YYYY-MM-DD]

## 11. Change log

| Date | Version | Change | By |
|------|---------|--------|----|
| YYYY-MM-DD | 1.0 | Card created | [Name] |

## 12. Approvals

- **Created by:** [Name, date]
- **Approved by AIMS Lead:** [Name, date]
- **Approved by Executive sponsor (for high-risk):** [Name, date]
```

---

## How to fill in for different system types

### For classical ML (e.g., credit scoring)

All sections apply. Special focus on sections 3 (training data), 6 (eval, drift monitoring), 5 (AISIA for high-risk).

### For GenAI on API (e.g., RAG chatbot on OpenAI)

Section 3 "Training data" = "Not trained". Section 9 (third parties) is mandatory and detailed. Section 6 focuses on hallucination rate and quality metrics rather than classical drift.

### For fine-tuned LLM

All sections. Section 3 covers the fine-tuning dataset. Section 6 includes evaluation against original capabilities (catastrophic forgetting check).

### For RPA + AI (e.g., email classification)

A lightweight version. If risk classification = Low / Minimal — section 5 is brief, AISIA not required.

---

## References

- [Standard overview (42001)](../overview.md)
- [ISO 42005 Impact Assessment guide](../iso-42005-impact-assessment-guide.md)
- [GenAI/LLM-specific controls](../genai-llm-specific-controls.md)

---

*Template aligned with ISO/IEC 42001:2023 Annex A.4.2, A.4.3, A.4.4, A.4.5, A.4.6.*
