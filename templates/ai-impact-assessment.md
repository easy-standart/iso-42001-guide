# Template: AI System Impact Assessment (AISIA)

> 🇷🇺 [Читать на русском](../ru-templates/ai-impact-assessment.md) · ⬅ [Back to home](../README.md)

> **What this is.** A fillable AI System Impact Assessment (AISIA) template — the artefact required by ISO/IEC 42001 clause 6.1.4, performed under clause 8.4, and evidenced by Annex A controls A.5.2–A.5.5. It assesses how an AI system affects individuals, groups, and society. This is the requirement with no equivalent in ISO 27001, and the one auditors go to first. Structure follows ISO/IEC 42005:2025.
>
> **How to use it.** Copy the block below into Markdown or a Doc for each AI system, at design and before any material change. Replace `[bracketed]` placeholders. Fields marked ✓ are mandatory for audit. Pair it with the system's [AI System Card](./ai-system-card.md).

---

```markdown
# AI System Impact Assessment: [System name]

**AISIA ID:** AISIA-[NUMBER]
**Linked AI System Card:** AIS-[NUMBER]
**Version:** 1.0
**Assessment date:** [YYYY-MM-DD]
**Next review:** [YYYY-MM-DD]
**Lifecycle stage:** [Design / Pre-deployment / Post-change / Periodic review]
**Trigger for this assessment:** [New system / Material model change / New use case / Scheduled review]
**Assessor:** [Name, role]

## 1. System and scope of assessment ✓

- **System purpose:** [1–2 sentences — what it does and why]
- **What is being assessed:** [The specific system, version, and use case in scope]
- **Why now:** [What triggered the assessment]
- **Deployment context:** [Where and how it operates — sector, geography, at what scale]

## 2. Intended use and foreseeable misuse ✓

- **Intended use:** [The approved purpose]
- **Out of scope:** [Uses that are explicitly disallowed]
- **Foreseeable misuse:** [Realistic ways it could be misused or fail in the real world]
- **Degree of autonomy:** [Advisory / Human-in-the-loop / Human-on-the-loop / Autonomous]

## 3. Affected parties ✓

- **Direct users:** [Who operates the system]
- **Individuals affected by outputs:** [Who receives or is subject to its decisions]
- **Vulnerable groups:** [Minors, patients, applicants, protected groups — anyone at heightened risk]
- **Society / third parties:** [Wider groups affected indirectly]

## 4. Data and sensitivity ✓

- **Input data:** [What the system consumes]
- **Personal / special-category data:** [Categories, or "none"]
- **Data provenance:** [Where training / reference data comes from, licensing]
- **Known data limitations:** [Gaps, imbalance, staleness that could skew outcomes]

## 5. Potential impacts ✓

For each relevant category, describe the impact, who it falls on, and rate it. Delete rows that do not apply, and say why in section 6.

| Impact category | Potential harm | Potential benefit | Affected party | Likelihood (L/M/H) | Severity (L/M/H) |
|-----------------|----------------|-------------------|----------------|--------------------|------------------|
| Fundamental rights & freedoms | [ ] | [ ] | [ ] | [ ] | [ ] |
| Fairness & bias | [ ] | [ ] | [ ] | [ ] | [ ] |
| Safety & security | [ ] | [ ] | [ ] | [ ] | [ ] |
| Privacy & data protection | [ ] | [ ] | [ ] | [ ] | [ ] |
| Transparency & explainability | [ ] | [ ] | [ ] | [ ] | [ ] |
| Economic & societal (jobs, access) | [ ] | [ ] | [ ] | [ ] | [ ] |
| Environmental (compute footprint) | [ ] | [ ] | [ ] | [ ] | [ ] |

## 6. Impact evaluation ✓

- **Most significant impacts:** [The 1–3 that drive the decision]
- **Groups most at risk:** [From section 3]
- **Categories excluded and why:** [Justify any deleted rows]

## 7. Mitigations and residual impact ✓

| Impact | Mitigation | Owner | Residual impact after mitigation |
|--------|------------|-------|----------------------------------|
| [ ] | [ ] | [ ] | [ ] |

## 8. Human oversight

- **Oversight model:** [Human-in-the-loop / on-the-loop / in-command]
- **Who can override or stop the system:** [Role]
- **How a person contests a decision:** [Appeal / redress channel]

## 9. Links to the management system

- **Risk register entries:** [IDs of related risks — clause 6.1.2]
- **Applicable Annex A controls (SoA):** [e.g. A.5.4, A.6.2, A.8.x]
- **AI System Card:** AIS-[NUMBER]

## 10. Conclusion and decision ✓

- **Overall residual impact:** [Low / Medium / High]
- **Decision:** [Proceed / Proceed with conditions / Do not proceed]
- **Conditions (if any):** [What must be true before/while operating]
- **Rationale:** [Why this decision]

## 11. Approvals ✓

- **Prepared by:** [Name, role, date]
- **Reviewed by AIMS Lead:** [Name, date]
- **Approved by (Executive sponsor for High residual):** [Name, date]

## 12. Review and change log

| Date | Version | Change / trigger | By |
|------|---------|------------------|----|
| YYYY-MM-DD | 1.0 | Initial assessment | [Name] |
```

---

## How to fill it in

### At design stage
Sections 1–5 are estimates against the intended design. Impacts are forecast, not measured — that is expected. The point is to surface high-severity impacts early, while the design can still change.

### Before deployment
Revisit sections 5–7 with real test data — bias-testing results, eval metrics, red-team findings. Residual impact in section 7 should now be evidenced, not assumed. This is what control **A.5.3** and **A.5.4** expect.

### After a material change
A new model version, a new use case, or a new market re-triggers the assessment (clause 8.4). Bump the version, log the trigger in section 12, and re-evaluate only what changed.

### Scaling by risk
- **High-risk (decisions about people):** every section in full, executive sign-off, annual review.
- **Low / minimal risk:** sections 1–3 and 10 may be brief; a short justification that impact is minimal is acceptable — but the record must still exist (A.5.3).

---

## References

- [Standard overview (42001)](../overview.md)
- [ISO 42005 Impact Assessment guide](../iso-42005-impact-assessment-guide.md)
- [Annex A controls explained (A.5)](../annex-a-controls.md)
- [Implementation guide](../implementation-guide.md)
- [AI System Card template](./ai-system-card.md)

---

*Template aligned with ISO/IEC 42001:2023 clause 6.1.4 and 8.4, Annex A controls A.5.2–A.5.5; structure follows ISO/IEC 42005:2025 (AI system impact assessment).*
