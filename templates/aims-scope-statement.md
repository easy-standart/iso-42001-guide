# Template: AIMS Scope Statement

> 🇷🇺 [Читать на русском](../ru-templates/aims-scope-statement.md) · ⬅ [Back to home](../README.md)

> **What this is.** A Scope Statement template for an AI Management System (AIMS) under ISO/IEC 42001:2023 Clause 4.3. It is the first document a certification auditor will ask for at Stage 1. A clear scope is the foundation of a successful certification.

---

## What a Scope Statement must include

Per ISO/IEC 42001 Clause 4.3, the scope statement must consider:

- External and internal factors (Clause 4.1)
- Stakeholder requirements (Clause 4.2)
- Interaction with other organizational systems
- Decisions on the applicability of each Annex A control (recorded in the Statement of Applicability — a separate document)

Length: 1–3 pages. It should be **publicly available** (on request from auditors and regulators).

---

## Template

```markdown
# AI Management System (AIMS) Scope Statement

**Organization:** [Full legal name]
**Document version:** 1.0
**Approval date:** [YYYY-MM-DD]
**Approved by:** [Name, role — typically CEO or AIMS C-level sponsor]
**Next review:** [YYYY-MM-DD — no later than 12 months]
**Confidentiality:** Public

## 1. Organization identification

- **Legal name:** [Full name]
- **HQ address:** [Address]
- **Jurisdiction:** [Country / state of registration]
- **Legal entities in scope:** [List, if multiple]
- **Legal entities out of scope:** [Sister / subsidiary companies excluded]

## 2. Business description

[2–3 paragraphs: what the company does, main products and services, customer segments, markets. Enough context for the auditor.]

## 3. AIMS scope (in scope)

### 3.1. Products and services in scope

| ID | Product / Service | Description |
|----|--------------------|-------------|
| P-001 | [Name] | [1–2 sentences] |
| P-002 | [Name] | [1–2 sentences] |

### 3.2. AI systems in scope

| ID | AI system | Business function | Risk level | System card link |
|----|-----------|--------------------|------------|-------------------|
| AIS-001 | [Name] | [Function] | High / Medium / Low | [Link] |

### 3.3. Physical sites and infrastructure

- **Sites:** [Offices, data centers]
- **Cloud infrastructure:** [AWS / Azure / GCP / OnPrem — with regions]
- **Additional subprocessors:** [Third parties processing in-scope data]

### 3.4. Personnel in scope

- **Headcount in scope:** [Number]
- **Included roles:** [Engineering / Product / Customer Support / etc.]
- **Included departments:** [List]

### 3.5. Roles under ISO/IEC 42001

Tick applicable roles (one or more):

- [ ] AI Producer — we build models for our own use or sale
- [ ] AI Provider — we provide AI systems or platforms to third parties
- [ ] AI Customer — we use AI systems built by others
- [ ] AI User — our employees use AI tools for work

## 4. Out of scope

[Explicit list of what is NOT covered by this AIMS. Important — otherwise the auditor may include it.]

Examples:
- Internal generative-AI experiments for marketing purposes.
- R&D-stage products not available to customers.
- AI features in third-party SaaS not integrated with in-scope products.
- Legal entities not listed in section 1.

**Justification for exclusions:** [Short explanation of why these are out of scope]

## 5. External and internal factors (per Clause 4.1)

### External
- **Regulation:** [EU AI Act / Colorado AI Act / NYC LL 144 / etc.]
- **Customer requirements:** [Microsoft SSPA / Fortune 100 procurement / etc.]
- **Tech trends:** [GenAI / LLM platforms / Agents]
- **Competition:** [Competitors with / without certificate]
- **Ethical and social expectations:** [AI fairness, transparency]

### Internal
- **Strategy:** [Short reference to business strategy]
- **Culture:** [Approach to risk management]
- **Existing management systems:** [ISO 27001 / SOC 2 / etc.]
- **Available resources:** [Team, budget]

## 6. Stakeholders (per Clause 4.2)

| Stakeholder | Type | Requirements / expectations |
|-------------|------|------------------------------|
| Customers | External | [What they require] |
| Regulators | External | [Applicable regulation] |
| Employees | Internal | [Their AIMS-related interests] |
| Investors / shareholders | External | [Their expectations] |
| Partners and suppliers | External | [Their role] |
| Affected parties (for high-risk) | External | [E.g., candidates, customer end-users] |
| Society | External | [Social expectations] |

## 7. Interaction with other management systems

[If you hold ISO 27001, ISO 9001, ISO 13485, SOC 2 — describe how they interact with the AIMS.]

Example: "The AIMS is integrated with the existing ISO/IEC 27001-aligned information security management system. Common processes for document management, risk management, supplier management, and internal audit are reused. The list of controls duplicated across standards is in the Statement of Applicability."

## 8. Related documents

- **Statement of Applicability (SoA):** [Link]
- **AI Policy:** [Link]
- **AI systems register:** [Link]
- **AI risk register:** [Link]
- **AISIA portfolio:** [Link]

## 9. Change log

| Date | Version | Change | Approved by |
|------|---------|--------|-------------|
| YYYY-MM-DD | 1.0 | Initial document | [Name] |

## 10. Approval

Approved by order [NUMBER] dated [DATE].

[Name of CEO / AIMS owner]
[Role]
[Date]
[Signature]
```

---

## Common mistakes

1. **Too broad scope.** "The whole company, all products" — almost always leads to major nonconformity. Start with one product.

2. **Vague AI-system definition.** "All our AI features" without an explicit list — the auditor will include things you did not prepare.

3. **No explicit out-of-scope.** If you did not write what is excluded — the auditor may include it.

4. **Ignoring third parties.** If you use OpenAI API in the product — it is part of scope (as a supplier).

5. **Ignoring stakeholders.** Failing to mention that a high-risk AI affects specific groups — the auditor will note it.

---

## References

- [Standard overview (42001)](../overview.md)
- [Readiness checklist](../checklist.md)
- [Certified companies registry with scope examples](../certified-companies.md)
- [AI System Card template](./ai-system-card.md)

---

*Template aligned with ISO/IEC 42001:2023 Clauses 4.1, 4.2, 4.3, 4.4.*
