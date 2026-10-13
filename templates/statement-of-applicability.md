# Template: Statement of Applicability (SoA)

> 🇷🇺 [Читать на русском](../ru-templates/statement-of-applicability.md) · ⬅ [Back to home](../README.md)

> **What this is.** A Statement of Applicability template for an AI Management System under ISO/IEC 42001:2023 Clause 6.1.3. The SoA is the single most-scrutinized document at audit: for every Annex A control it records whether the control applies, why, and how it is implemented. An empty justification column is the most common Stage 2 finding.

---

## What a Statement of Applicability must include

Per ISO/IEC 42001 Clause 6.1.3, the SoA must contain:

- The controls the organization has determined necessary (from Annex A **and** any additional controls added from your own risk and impact assessment).
- For each control: the **justification for inclusion**, and whether it is **implemented or not**.
- The **justification for excluding** any Annex A control.

The SoA is driven by two inputs: the AI risk assessment (Clause 6.1.2) and the AI system impact assessment / AISIA (Clause 6.1.4). You do not implement all 38 controls "just in case" — you select what your risks and impacts require, and justify the rest as excluded.

Length: as long as it needs to be (38+ rows). Usually **Confidential / Internal** — shared with the auditor, not published.

---

## Template

```markdown
# Statement of Applicability (SoA)

**Organization:** [Full legal name]
**Document version:** 1.0
**Approval date:** [YYYY-MM-DD]
**Approved by:** [Name, role — AIMS owner / C-level sponsor]
**Next review:** [YYYY-MM-DD — no later than 12 months, or after any significant change]
**Confidentiality:** Internal / Confidential
**Related inputs:** AI risk assessment v[__], AISIA portfolio v[__], Scope statement v[__]

## Legend

- **Applicable:** Yes / No
- **Status:** Implemented / Partially implemented / Planned (with target date)
- **Justification:** why the control is included (tie to a risk or impact) or excluded
- **Evidence:** link to the policy, procedure, record or system that implements it

## Annex A controls (38)

> Control wording is summarized. For the full description of each control, see
> [annex-a-controls.md](../annex-a-controls.md).

### A.2 — AI policies

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.2.2 | AI policy | Yes / No | | | | |
| A.2.3 | Alignment with other organizational policies | Yes / No | | | | |
| A.2.4 | Review of the AI policy | Yes / No | | | | |

### A.3 — Internal organization

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.3.2 | AI roles and responsibilities | Yes / No | | | | |
| A.3.3 | Reporting of concerns | Yes / No | | | | |

### A.4 — Resources for AI systems

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.4.2 | Resource documentation | Yes / No | | | | |
| A.4.3 | Data resources | Yes / No | | | | |
| A.4.4 | Tooling resources | Yes / No | | | | |
| A.4.5 | System and computing resources | Yes / No | | | | |
| A.4.6 | Human resources | Yes / No | | | | |

### A.5 — Assessing impacts of AI systems

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.5.2 | AI system impact assessment process | Yes / No | | | | |
| A.5.3 | Documentation of impact assessments | Yes / No | | | | |
| A.5.4 | Assessing impact on individuals and groups | Yes / No | | | | |
| A.5.5 | Assessing societal impact | Yes / No | | | | |

### A.6 — AI system life cycle

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.6.1.2 | Objectives for responsible development | Yes / No | | | | |
| A.6.1.3 | Processes for responsible design and development | Yes / No | | | | |
| A.6.2.2 | AI system requirements and specification | Yes / No | | | | |
| A.6.2.3 | Documentation of design and development | Yes / No | | | | |
| A.6.2.4 | Verification and validation | Yes / No | | | | |
| A.6.2.5 | Deployment | Yes / No | | | | |
| A.6.2.6 | Operation and monitoring | Yes / No | | | | |
| A.6.2.7 | Technical documentation | Yes / No | | | | |
| A.6.2.8 | Recording of event logs | Yes / No | | | | |

### A.7 — Data for AI systems

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.7.2 | Data for development and enhancement | Yes / No | | | | |
| A.7.3 | Acquisition of data | Yes / No | | | | |
| A.7.4 | Quality of data | Yes / No | | | | |
| A.7.5 | Data provenance | Yes / No | | | | |
| A.7.6 | Data preparation | Yes / No | | | | |

### A.8 — Information for interested parties

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.8.2 | System documentation and information for users | Yes / No | | | | |
| A.8.3 | External reporting | Yes / No | | | | |
| A.8.4 | Communication of incidents | Yes / No | | | | |
| A.8.5 | Information for interested parties | Yes / No | | | | |

### A.9 — Use of AI systems

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.9.2 | Processes for responsible use | Yes / No | | | | |
| A.9.3 | Objectives for responsible use | Yes / No | | | | |
| A.9.4 | Intended use of the AI system | Yes / No | | | | |

### A.10 — Third parties and customers

| Control | Topic | Applicable? | Status | Justification | Evidence | Owner |
|---------|-------|-------------|--------|---------------|----------|-------|
| A.10.2 | Allocation of responsibilities | Yes / No | | | | |
| A.10.3 | Suppliers | Yes / No | | | | |
| A.10.4 | Customers | Yes / No | | | | |

## Additional controls (beyond Annex A)

If your risk or impact assessment surfaced a control that Annex A does not cover
(e.g. a sector-specific or regulatory control), record it here.

| Control | Source | Applicable? | Status | Justification | Evidence | Owner |
|---------|--------|-------------|--------|---------------|----------|-------|
| CUST-01 | [EU AI Act Art. __ / internal] | Yes / No | | | | |

## Change log

| Date | Version | Change | Approved by |
|------|---------|--------|-------------|
| YYYY-MM-DD | 1.0 | Initial SoA | [Name] |

## Approval

Approved by [Name, role], [Date]. Signature: __________
```

---

## Common mistakes

1. **Empty justification column.** The single most common Stage 2 finding. Every "applicable" needs a reason and an evidence link; every "not applicable" needs a justification.

2. **Marking all 38 applicable "to be safe".** The SoA must follow from your risk and impact assessment, not the other way round. Over-scoping creates evidence you cannot produce.

3. **Justification not tied to a risk or impact.** "We do this because it is good practice" is weak. Link the control to a specific risk (Clause 6.1.2) or impact (AISIA, Clause 6.1.4).

4. **Evidence column points nowhere.** "Implemented" without a link to the actual policy, record or system is treated as not implemented.

5. **Not updated after change.** New AI system, new supplier, new regulation — the SoA must be revised. A stale SoA undermines the whole AIMS.

6. **Forgetting third-party controls.** If you use an external model API (OpenAI, Anthropic, Google), A.10 controls apply — they are part of your scope as a supplier.

---

## References

- [Annex A — all 38 controls explained](../annex-a-controls.md)
- [Standard overview (42001)](../overview.md)
- [Readiness checklist](../checklist.md)
- [AIMS Scope Statement template](./aims-scope-statement.md)
- [AI Impact Assessment template](./ai-impact-assessment.md)

---

*Template aligned with ISO/IEC 42001:2023 Clauses 6.1.2, 6.1.3, 6.1.4 and Annex A.*
