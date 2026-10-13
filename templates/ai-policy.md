# Template: AI Policy

> 🇷🇺 [Читать на русском](../ru-templates/ai-policy.md) · ⬅ [Back to home](../README.md)

> **What this is.** An AI Policy template under ISO/IEC 42001:2023 Clause 5.2 and Annex A control area A.2. It is the top-level statement of intent that top management signs: what the organization stands for in its use of AI, and the rules everything else in the AIMS hangs off. Usually 1–2 pages.

---

## What an AI Policy must include

Per Clause 5.2, top management establishes an AI policy that:

- Fits the organization's purpose and context.
- Provides a framework for setting AI objectives.
- Commits to meeting applicable requirements (legal, regulatory, customer).
- Commits to continual improvement of the AIMS.

Annex A adds three related controls: **A.2.2** (the AI policy itself), **A.2.3** (alignment with other organizational policies), and **A.2.4** (regular review of the policy). The policy must be documented, communicated inside the organization, and available to interested parties as appropriate.

Keep it short and principled. Detailed rules live in procedures the policy points to (acceptable-use, impact assessment, incident response), not in the policy itself.

---

## Template

```markdown
# AI Policy

**Organization:** [Full legal name]
**Document version:** 1.0
**Approval date:** [YYYY-MM-DD]
**Approved by:** [Name, role — CEO / top management]
**Next review:** [YYYY-MM-DD — at least annually]
**Confidentiality:** Public (available to interested parties on request)

## 1. Purpose

[Why this policy exists: to govern how the organization develops, provides and uses
AI systems responsibly, and to frame the AI Management System under ISO/IEC 42001.]

## 2. Scope

This policy applies to [all / listed] AI systems the organization develops, provides
or uses, and to [employees, contractors, relevant suppliers]. See the AIMS Scope
Statement for the exact boundary.

## 3. Our principles for responsible AI

The organization commits to:

- **Human oversight** — people stay accountable for AI-supported decisions; the level of oversight matches the risk.
- **Transparency** — we can explain, at an appropriate level, what our AI systems do and how they are used.
- **Fairness** — we work to identify and reduce harmful bias and discriminatory outcomes.
- **Safety and robustness** — AI systems are tested and monitored for reliable behaviour.
- **Privacy and security** — personal and sensitive data used by AI is protected (aligned with our information security policy).
- **Accountability** — clear roles own each AI system and its risks.
- **Lawful and ethical use** — we meet applicable regulation (e.g. [EU AI Act / local law]) and our own ethical standards.

## 4. Commitments

The organization commits to:

- Meet applicable legal, regulatory and customer requirements.
- Run risk assessments and AI system impact assessments (AISIA) for AI systems in scope.
- Set and review measurable AI objectives.
- Provide the resources and competence the AIMS needs.
- Continually improve the AIMS.

## 5. Governance and roles

- **Top management** owns this policy and the AIMS.
- **[AIMS lead / AI Governance Lead]** runs the management system day to day.
- **[System owners]** are accountable for individual AI systems and their risks.
- Concerns can be raised through [channel] without fear of reprisal (see A.3.3).

## 6. Related policies and documents

This policy is aligned with, and does not contradict, our:

- Information security policy (ISO/IEC 27001, if held)
- Data protection / privacy policy
- Acceptable-use policy for AI tools (incl. shadow-AI rules)
- Supplier / third-party management policy

Supporting documents: AIMS Scope Statement, Statement of Applicability, AI risk
register, AISIA portfolio, incident response plan.

## 7. Review

This policy is reviewed at least annually and after any significant change
(new regulation, major new AI system, serious incident). Changes are approved by
top management.

## 8. Change log

| Date | Version | Change | Approved by |
|------|---------|--------|-------------|
| YYYY-MM-DD | 1.0 | Initial policy | [Name] |

## Approval

Approved by [Name, role], [Date]. Signature: __________
```

---

## Common mistakes

1. **Generic copy-paste.** A policy that could belong to any company signals a paper AIMS. Tie principles to what your AI systems actually do.

2. **No link to the rest of the AIMS.** The policy should point to the Scope Statement, SoA, risk register and procedures — not float alone.

3. **No owner, no review date.** A.2.4 requires review. A policy with no next-review date is an easy finding.

4. **Contradicting other policies.** A.2.3 requires alignment. If the AI policy says one thing and the security or privacy policy another, the auditor will notice.

5. **All principle, no commitment.** Nice values without concrete commitments (impact assessments, objectives, resources) are not auditable.

6. **Never communicated.** The policy must be communicated internally and available to interested parties. Sitting in a drawer does not count.

---

## References

- [Standard overview (42001)](../overview.md)
- [Annex A — all 38 controls explained](../annex-a-controls.md)
- [Statement of Applicability template](./statement-of-applicability.md)
- [AIMS Scope Statement template](./aims-scope-statement.md)
- [Shadow AI policy template](../shadow-ai-policy-template.md)

---

*Template aligned with ISO/IEC 42001:2023 Clause 5.2 and Annex A.2.*
