# Template: AI Incident Response Playbook

> 🇷🇺 [Читать на русском](../ru-templates/ai-incident-response.md) · ⬅ [Back to home](../README.md)

> **What this is.** A response playbook template for AI incidents under ISO/IEC 42001:2023 control A.8.4 and Clause 10. Covers classification, escalation, stakeholder notifications, root cause analysis, regulatory timers (GDPR, EU AI Act, NYC LL 144).

> **Why a separate playbook for AI.** Classical IT incident response covers availability, integrity, confidentiality. AI incidents add new categories: discrimination, hallucination in production, jailbreak, data leakage through LLM providers. Each requires specific response.

---

## 1. What counts as an AI incident

**AI incident categories:**

| Category | Examples | Default severity |
|----------|----------|-------------------|
| **Discrimination / bias** | A scoring model started rejecting one demographic group disproportionately | Critical |
| **Hallucination in production** | An LLM gave a customer legal advice that turned out to be fabricated | High |
| **Data leakage via LLM** | Confidential customer data appeared in another user's response | Critical |
| **Jailbreak / prompt injection** | A user accessed the system prompt or disallowed functionality | High |
| **Model degradation** | Model quality dropped sharply (drift, deployment bug) | High |
| **Data poisoning** | Malicious content found in training / RAG data | Critical |
| **Unauthorized AI use** | An employee used an AI tool outside the policy | Medium |
| **AI supply chain incident** | The LLM provider had an incident that affected your system | High |
| **Regulator inquiry** | A regulator asked about AI use | High |
| **Public disclosure** | A complaint in the press, social media, or public forums | Medium-High |

---

## 2. Severity classification

| Severity | Criterion | Time to acknowledge | Time to mitigate | Escalation |
|----------|-----------|----------------------|-------------------|------------|
| **Critical** | Direct harm to affected parties OR regulatory violation OR public resonance | 30 min | 4 hours | CEO + legal + PR |
| **High** | Material service degradation OR potential to become Critical | 1 hour | 24 hours | CISO + AIMS Lead |
| **Medium** | Local issue without broad impact | 4 hours | 5 business days | AIMS Lead |
| **Low** | Isolated glitch | 1 business day | 30 days | AI system owner |

---

## 3. Incident response roles

| Role | Who | Responsibility |
|------|-----|-----------------|
| **Incident Commander** | AIMS Lead / CISO | Runs the response, escalates |
| **Technical Lead** | ML Lead / AI System Owner | Technical analysis and remediation |
| **Communications Lead** | PR / Comms | External communications |
| **Legal Lead** | Head of Legal / DPO | Legal assessment, regulatory notifications |
| **Executive sponsor** | CEO / CTO | Key decisions for Critical |
| **Scribe** | Any member | Records timeline, decisions |

---

## 4. Response process (phases)

### Phase 1: Detect

**Signal sources:**
- Internal monitoring (drift, deviation alerts)
- A.3.3 channel (ai-concerns@company.com)
- Customer or user complaint
- Regulator inquiry
- Media / social media post
- LLM provider notification

**Actions:**
1. Any employee receiving a signal forwards to ai-incidents@company.com or via the ticketing system.
2. AIMS Lead acknowledges within 30 min and assesses severity.

### Phase 2: Triage

**Actions:**
1. AIMS Lead assembles the initial team (depends on severity).
2. Severity, scope, affected systems and parties are clarified.
3. An incident ticket is opened with a unique ID.
4. A Slack channel (or equivalent) is created: `#incident-[ID]`.

### Phase 3: Contain

**Actions:**
1. Containment decision: disable the AI system / switch to fallback / human-only mode / no change.
2. For Critical — default to disable or switch to human-in-the-loop.
3. Apply technical mitigations.
4. Document decision and rationale.

### Phase 4: Notify

**Internal:**
- Executive sponsor — for High and above.
- AIMS team — for all.
- Affected product teams.

**External (if applicable):**

| Party | When | Deadline | Basis |
|-------|------|----------|-------|
| Affected users | Critical / High with direct impact | Without undue delay, typically 72 hours | GDPR Art. 34, etiquette |
| Data protection regulator | Personal data leakage | 72 hours | GDPR Art. 33 |
| AI Act regulator | Serious incident in high-risk system | 15 days | EU AI Act Art. 73 |
| NYC regulator | AEDT bias detected | Per Local Law 144 rules | NYC LL 144 |
| B2B customers | Per contractual obligations | See contracts | Contract law |
| Partners and suppliers | If their data / systems are affected | Per contracts | Contract law |

### Phase 5: Eradicate

**Actions:**
1. Root cause analysis (RCA) — at minimum 5-Whys or a formal RCA method.
2. Corrective action plan.
3. Apply patches, model rollback, data cleanup, policy update.
4. Validate the cause is removed.

### Phase 6: Recover

**Actions:**
1. Gradual return to production (canary → partial → full).
2. Enhanced monitoring for 7–30 days.
3. Validate quality and safety metrics.
4. Lift the enhanced mode.

### Phase 7: Lessons learned (post-mortem)

**Actions:**
1. Within 14 days — post-mortem document.
2. Structure: timeline, root cause, what worked, what did not, action items.
3. Reported to the next management review.
4. Playbook updates based on lessons learned.
5. Added to the AIMS incident register.

---

## 5. Post-mortem template

```markdown
# Post-mortem: [Incident ID] [Short description]

**Incident date:** [YYYY-MM-DD]
**Severity:** [Critical / High / Medium / Low]
**Duration:** [Open → close]
**Affected systems:** [List]
**Affected parties:** [Count / categories]

## Timeline

| Time | Event | Source |
|------|-------|--------|
| HH:MM | [What happened] | [Where it came from] |

## Root cause

[Root cause from RCA. Not "what broke" but "why we did not prevent it".]

## What worked

- [Positives in the response]

## What did not work

- [What needs improvement]

## Action items

| ID | Action | Type | Owner | Due |
|----|--------|------|-------|-----|
| AI-001 | [Action] | Technical / Process / Policy / Training | [Name] | YYYY-MM-DD |

## Lessons learned

[What we learned so it does not recur]
```

---

## 6. Interaction with other processes

- **GDPR breach notification:** AI incidents with personal data leakage trigger the GDPR process (72 hours).
- **EU AI Act incident reporting:** high-risk systems have a dedicated procedure to notify national regulators (15 days).
- **Information security:** AI incidents may overlap with conventional infosec incidents (e.g., prompt injection as a form of social engineering).
- **Public Relations:** Critical incidents often become PR events.

---

## 7. Regular tabletop exercises

ISO 42001 does not explicitly require tabletop exercises, but they are the best way to verify the playbook works. Recommended:

- **Minimum:** one full scenario per year.
- **For high-risk systems:** every six months.
- **After material changes:** new product, new region, new regulator.

Scenario examples:
- "LLM produced a hallucination that ended up in a customer publication"
- "Employee accidentally uploaded source code into ChatGPT Free"
- "Regulator requested AI system documentation with a one-week deadline"
- "Bias detected in a production recruiting model"

---

## References

- [Standard overview (42001)](../overview.md)
- [Shadow AI Policy template](../shadow-ai-policy-template.md)
- [GenAI/LLM-specific controls](../genai-llm-specific-controls.md)
- [Top 15 common audit findings](../common-audit-findings.md)

---

*Template aligned with ISO/IEC 42001:2023 Clause 10, Annex A.8.4; accounts for GDPR Art. 33-34, EU AI Act Art. 73, NYC Local Law 144.*
