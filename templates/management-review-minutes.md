# Template: Management Review Minutes

> 🇷🇺 [Читать на русском](../ru-templates/management-review-minutes.md) · ⬅ [Back to home](../README.md)

> **What this is.** A Management Review minutes template under ISO/IEC 42001:2023 Clause 9.3. Without a properly conducted and documented review, the certificate **is not issued**. Minimum — one full review in the 12 months before Stage 2.

> **What the auditor checks:** not only that the review happened, but its quality — agenda matching Clause 9.3 requirements, top-management participation, decisions made, follow-up actions.

---

## Template

```markdown
# AIMS Management Review Minutes

**Date:** [YYYY-MM-DD]
**Time:** [HH:MM — HH:MM]
**Location:** [In person / online / hybrid]
**Document version:** 1.0
**Prepared by:** [Name — typically AIMS Lead]
**Approved by:** [Name of CEO or AIMS sponsor]
**Confidentiality:** Internal

## 1. Attendees

| Name | Role | Function on review |
|------|------|---------------------|
| [Name] | CEO | Chair |
| [Name] | CTO | Member |
| [Name] | CISO / AIMS Lead | Presenter |
| [Name] | CPO / DPO | Member |
| [Name] | Head of Product | Member |
| [Name] | Head of Legal | Member |
| [Name] | Internal auditor | Invitee |

**Quorum:** top management present (at minimum CEO + CTO or equivalent).

## 2. Agenda (per Clause 9.3.2)

ISO/IEC 42001 Clause 9.3.2 requires the review to cover the following items. All must appear on the agenda and be discussed:

1. Status of actions from previous management reviews.
2. Changes in internal and external factors relevant to the AIMS.
3. Information on AIMS performance, including trends in:
   - nonconformities and corrective actions,
   - monitoring and measurement results,
   - audit results,
   - achievement of AIMS objectives.
4. Stakeholder feedback.
5. Results of AI System Impact Assessments.
6. Results of AI risk assessment and status of the treatment plan.
7. Opportunities for continual improvement.

## 3. Items reviewed

### 3.1. Status of actions from previous reviews

| ID | Action | Due | Status | Comment |
|----|--------|-----|--------|---------|
| MR-2025-Q1-001 | [Description] | YYYY-MM-DD | Done / In progress / Overdue | [Comment] |

### 3.2. Context changes

**External:**
- [Regulatory changes in the period]
- [Customer requirements]
- [Technology trends]

**Internal:**
- [Strategy / structure changes]
- [Resource changes]
- [New products / systems]

### 3.3. AIMS performance

#### Nonconformities and corrective actions

| Period | Opened | Closed | Average closure time |
|--------|--------|--------|----------------------|
| Q[N] | [Number] | [Number] | [Days] |

Top 3 finding types: [List]

#### Monitoring results

| AI system | Metric | Target | Actual | Trend |
|-----------|--------|--------|--------|-------|
| AIS-001 | Hallucination rate | <3% | 2.1% | Stable |
| AIS-001 | Drift score | <0.15 | 0.08 | Improving |

#### Audit results

- **Internal audits in period:** [Number + key findings]
- **External audits:** [If any — Stage 1 / Stage 2 / surveillance]

#### AIMS objectives (KPIs)

| KPI | Target | Actual | Status |
|-----|--------|--------|--------|
| [E.g., % of AI systems with current AISIA] | 100% | 95% | Not met |
| [E.g., % of employees trained on AI Policy] | 100% | 100% | Met |

### 3.4. Stakeholder feedback

- **Customers:** [Key signals — security questionnaires, complaints, suggestions]
- **Employees:** [Surveys, AI concerns channel reports]
- **Regulators:** [Any contacts, requests, changes]
- **Affected parties:** [Feedback on high-risk systems]

### 3.5. AISIA results in the period

- **New AISIAs completed:** [Number]
- **Existing AISIAs reviewed:** [Number]
- **Key findings:** [Material ones]

### 3.6. AI risks

- **Register status:** [Active, new, closed risks]
- **Top 5 risks:** [List]
- **Changes in risk appetite:** [If any]

### 3.7. Incidents in the period

| Date | Description | Severity | Status | Lessons learned |
|------|-------------|----------|--------|------------------|
| YYYY-MM-DD | [Short description] | High / Medium / Low | Closed | [What we learned] |

### 3.8. AIMS resources

- **Team:** [Changes, needs]
- **Budget:** [Utilisation, needs]
- **Tooling:** [Changes, needs]

## 4. Decisions taken (output per Clause 9.3.3)

| ID | Decision | Rationale | Owner | Due |
|----|----------|-----------|-------|-----|
| MR-[period]-001 | [Decision] | [Why] | [Name] | YYYY-MM-DD |
| MR-[period]-002 | [Decision] | [Why] | [Name] | YYYY-MM-DD |

ISO/IEC 42001 Clause 9.3.3 requires the output to include:
- Decisions on continual improvement opportunities.
- Decisions on changes needed to the AIMS.
- Decisions on resource needs.

## 5. Policy and document changes

[If the review decides on changes to AI Policy, scope, or other key documents — record here with links to the new versions.]

## 6. Next review date

**Scheduled:** [YYYY-MM-DD]

Minimum cadence for AIMS — annually. Quarterly recommended for high-risk systems or in the first certification year.

## 7. Approvals

Minutes approved by:

**Chair (CEO):** [Name, date, signature]
**AIMS Lead:** [Name, date, signature]

## 8. Distribution

Minutes sent to:
- All review attendees
- Internal auditor
- AIMS archive

Full version — Internal. A summary report without sensitive details may be shared with employees.
```

---

## Common mistakes

1. **Review too short.** "30 minutes at standup" is not enough. A proper review takes 2–4 hours for a serious company.

2. **No top-management participation.** If the CEO did not show up and did not send a deputy — the review does not count.

3. **Decisions without owners or deadlines.** "Agreed to improve training" is not a decision. It must be specific.

4. **No tracking of prior-review decisions.** The auditor will ask at the next review what was done about earlier decisions.

5. **Mandatory Clause 9.3.2 items not covered.** If the agenda misses any of the 7 items — that is a nonconformity.

---

## References

- [Standard overview (42001)](../overview.md)
- [Readiness checklist](../checklist.md)
- [Top 15 common audit findings](../common-audit-findings.md)

---

*Template aligned with ISO/IEC 42001:2023 Clause 9.3.*
