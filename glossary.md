# ISO/IEC 42001 Glossary

> 🇷🇺 [Читать на русском](./ru/glossary.md) · ⬅ [Back to home](./README.md) · 📖 [Standard overview](./README.md)

> **What this is.** A single source of truth for ISO/IEC 42001 terminology. All definitions come from official ISO/IEC standards (22989:2022 normative, 23053, 23894, 5338, 42005, 38507, 12792, 24028, 24029, TR 24027). Where ISO terms differ from regulation (EU AI Act, NIST AI RMF), it is noted.

---

## Contents

- [1. Core AI concepts](#1-core-ai-concepts)
- [2. Data and training](#2-data-and-training)
- [3. Models and learning](#3-models-and-learning)
- [4. AI system properties (trustworthiness)](#4-ai-system-properties-trustworthiness)
- [5. Stakeholder roles](#5-stakeholder-roles)
- [6. AI system lifecycle](#6-ai-system-lifecycle)
- [7. Risk and impact management](#7-risk-and-impact-management)
- [8. Management and governance](#8-management-and-governance)
- [9. Security and attacks](#9-security-and-attacks)
- [10. Cross-framework harmonisation](#10-cross-framework-harmonisation)

---

## 1. Core AI concepts

| Term | Definition | Source |
|------|-------------|--------|
| **AI / artificial intelligence** | Field of research and development of engineered systems generating content, forecasts, recommendations, decisions for human-defined objectives | 22989 |
| **AI system** | Engineered system generating outputs for a given set of human-defined objectives | 22989 §3.1.4 |
| **AI agent** | Automated entity that senses and responds to its environment to achieve goals | 22989 §3.1.7 |
| **Autonomy** | Ability of a system to change its area of use or goal without external intervention | 22989 §3.1.5 |
| **Heteronomy** | System characteristic of operating under constraints due to external control | 22989 §3.1.16 |
| **AGI** | Type of AI system covering a broad spectrum of tasks at satisfactory performance | 22989 |

---

## 2. Data and training

| Term | Definition | Source |
|------|-------------|--------|
| **Data** | Representation of information, knowledge or instructions in formalised form | 22989 |
| **Training data** | Dataset used to train an AI model | 22989 |
| **Validation data** | Subset for hyperparameter tuning and preliminary evaluation during training | 22989 |
| **Test data** | Data not used in training, for final performance evaluation | 22989 |
| **Dataset** | Organised data collection for training, validation, testing, operation | 22989 |
| **Data quality** | Degree of fit to organisational data requirements in a specific context | 5259-1 |
| **Ground truth** | Verified labels or values predictions are compared to | 22989 |
| **Label** | Target value paired with a data instance under supervised ML | 22989 |
| **Feature** | Attribute or characteristic of a data instance used by the model | 22989 |

---

## 3. Models and learning

| Term | Definition | Source |
|------|-------------|--------|
| **Model** | Physical, mathematical, or other logical representation | 22989 |
| **Machine learning (ML)** | Branch of AI using computational methods to learn from data or experience | 23053 |
| **Supervised learning** | ML on labelled data | 23053 |
| **Unsupervised learning** | ML to find structure in unlabelled data | 23053 |
| **Semi-supervised** | Combination of labelled and unlabelled | 23053 |
| **Reinforcement learning** | ML maximising reward via actions in an environment | 23053 |
| **Transfer learning** | Reuse of a model trained on one task for a related one | 23053 |
| **Deep learning** | ML based on multi-layer neural networks | 23053 |
| **Neural network** | Model inspired by biological neural networks | TR 24029-1 |
| **Foundation model** | Large pre-trained model, basis for a broad range of downstream tasks | 22989/Amd 1 |
| **LLM (large language model)** | Foundation model variant for natural language | 22989/Amd 1 |
| **Generative AI** | AI systems generating new content (text, images, audio, video, code) | 22989/Amd 1, 23053/Amd 1 |
| **Inference** | Applying a trained system to generate outputs on new inputs | 22989 |
| **Training** | Process of building an ML model | 22989 |
| **Continuous learning** | Model continues learning after initial deployment | 22989 |

---

## 4. AI system properties (trustworthiness)

| Term | Definition | Source |
|------|-------------|--------|
| **Trustworthiness** | Ability to meet stakeholder expectations in a verifiable way | TR 24028 |
| **Transparency** | Information about the system is available to relevant stakeholders (properties, limits, data, design choices) | 12792 |
| **Explainability** | Degree to which the system's mechanics can be presented in human-understandable terms | 22989 |
| **Interpretability** | Degree to which a human can understand the reason for a model decision | 22989 |
| **Controllability** | Ability of a human or other external agent to intervene in operation | 22989 |
| **Robustness** | Ability to maintain performance under changing (including adverse) conditions | TR 24029-1 |
| **Reliability** | Ability to perform required functions under stated conditions for a stated period | 22989 |
| **Resilience** | Ability to recover required performance after disturbances | 22989 |
| **Accuracy** | Closeness of results to reference | TS 4213 |
| **Safety** | Absence of unacceptable risk to life, health, environment | 22989 |
| **Security** | Protection from intentional attacks on CIA | 22989 |
| **Privacy** | Protection of personal data and private life | 22989 |
| **Bias** | Systematic error producing unfair outcomes; split into desired and undesired | TR 24027 |
| **Fairness** | System property of not producing unfair discrimination across groups | 22989 |
| **Accountability** | Ability to identify and hold accountable a party for consequences | 22989 |
| **Data drift** | Change in the input data distribution over time | 5338 |
| **Concept drift** | Change in the input-output relationship over time | 5338 |
| **Hallucination** | Generation of factually wrong or unverifiable content by a generative model | 22989/Amd 1 |

---

## 5. Stakeholder roles

Per ISO/IEC 22989 §5.19:

| Role | Who |
|------|-----|
| **AI stakeholder** | Person or org that can affect, be affected by, or perceive themselves as affected by an AI system decision/activity |
| **AI provider** | Organisation providing AI products or services (AI platform provider, AI product or service provider) |
| **AI producer** | Organisation designing, developing, testing, deploying AI products or services |
| **AI customer** | Organisation or person using an AI product or service (AI user and AI deployer) |
| **AI partner** | Organisation supplying system components (API, data, libraries), integrators, consultants |
| **AI subject** | Person or legal entity affected by system operation |
| **AI relevant authority** | Policymaker, regulator, other government bodies |

### Human oversight modes

Widely used industry terms — **not** defined in ISO/IEC 22989 §5.19. The overarching "human oversight" concept aligns with ISO/IEC DIS 42105.

| Term | Meaning |
|------|---------|
| **Human-in-the-loop (HITL)** | Mode where a human is mandatorily part of every decision |
| **Human-on-the-loop (HOTL)** | Human supervises and may intervene but is not required to per decision |
| **Human-in-command (HIC)** | Human sets overall rules and goals with authority to halt the system |
| **Human oversight** | Comprehensive concept extending controllability; see ISO/IEC DIS 42105 |

---

## 6. AI system lifecycle

Per ISO/IEC 22989 §6, detailed in ISO/IEC 5338:2023:

| Phase | What happens |
|-------|---------------|
| **Inception** | Goals, requirements, assumptions, business case |
| **Design and development** | Architecture, model selection, feature engineering, training |
| **Verification and validation** | Conformance to requirements and fitness for purpose |
| **Deployment** | Putting into operation |
| **Operation and monitoring** | Performance, drift detection |
| **Continuous validation** | Re-evaluation on change |
| **Re-evaluation** | Full reassessment on significant context/data change |
| **Retirement** | End of use respecting data and decision-history requirements |

---

## 7. Risk and impact management

| Term | Definition | Source |
|------|-------------|--------|
| **Risk** | Effect of uncertainty on objectives | ISO Guide 73 |
| **Risk source** | Element with potential to give rise to risk | 23894 Annex B |
| **Risk assessment** | Process of risk identification, analysis, evaluation | 31000 |
| **Risk treatment** | Selection and implementation of measures to modify risk | 31000 |
| **AI System Impact Assessment (AISIA)** | Structured process to identify, evaluate, document impacts of AI on individuals, groups, society | 42005 |
| **FRIA** | Fundamental Rights Impact Assessment — EU AI Act Art. 27 duty for high-risk deployers | EU AI Act |
| **AIA** | Algorithmic Impact Assessment — Canadian methodology (Directive on Automated Decision-Making) | Canada AIA |

---

## 8. Management and governance

| Term | Definition | Source |
|------|-------------|--------|
| **AIMS / AI management system** | Interrelated elements of an organization for setting AI policy and objectives | 42001 |
| **AI governance** | Processes and structures through which an organization directs and controls AI use | 38507:2022 |
| **Statement of Applicability (SoA)** | Document justifying inclusion/exclusion of each Annex A control | 42001 |
| **AI Policy** | Formalised set of principles and rules for AI use | 42001 A.2.2 |
| **Responsible AI** | Umbrella concept of responsible AI development and use | TR 24028 |

---

## 9. Security and attacks

| Term | Definition | Source |
|------|-------------|--------|
| **Red teaming** | Structured adversarial testing of security and robustness | AWI TS 42119-7 |
| **Adversarial attack** | Intentional input perturbation to distort model behaviour | FDIS 27090 |
| **Data poisoning** | Insertion of malicious data into the training set | TR 24028 |
| **Model theft / extraction attack** | Unauthorised reproduction of a model through its interface | TR 24028 |
| **Prompt injection** | Attack on an LLM via crafted user input | (formalisation pending) |
| **Jailbreak** | Bypass of LLM safety mechanisms | (formalisation pending) |
| **Knowledge engineering (KE)** | Process of knowledge acquisition and formalisation for AI systems | 5392:2024 |
| **Formal methods** | Mathematical techniques for rigorous specification and verification | 24029-2 |

---

## 10. Cross-framework harmonisation

### EU AI Act ↔ ISO 22989

| EU AI Act | ISO/IEC 22989 |
|-----------|----------------|
| Provider | AI provider |
| Deployer | AI customer (user/deployer) |
| Importer, distributor | Intermediate |

### NIST AI RMF ↔ ISO/IEC 42001

| NIST AI RMF | ISO/IEC 42001 |
|--------------|-----------------|
| GOVERN | Clauses 4–5 |
| MAP | Clause 6 + ISO/IEC 42005 |
| MEASURE | ISO/IEC 24029, TS 4213, TR 24027 |
| MANAGE | Clauses 8, 10 + ISO/IEC 23894 |

### High-risk AI system

EU AI Act term (Annex III). Requires FRIA (Art. 27); in practice may be implemented via ISO/IEC 42005.

---

## Read next

- [ISO/IEC 42001 structure](./structure.md)
- [Family of standards](./family-of-standards.md)
- [ISO 42005 Impact Assessment guide](./iso-42005-impact-assessment-guide.md)
- [NIST AI RMF comparison](./comparison-nist-ai-rmf.md)

---

*Sources: ISO/IEC 22989:2022; ISO/IEC 23053:2022; ISO/IEC 23894:2023; ISO/IEC 5338:2023; ISO/IEC 38507:2022; ISO/IEC 5259-1; ISO/IEC 12792; ISO/IEC TS 4213; ISO/IEC TR 24027; ISO/IEC TR 24028:2020; ISO/IEC TR 24029-1:2021; ISO/IEC 24029-2:2023; ISO/IEC 42001:2023; ISO/IEC 42005:2025; ISO/IEC DIS 42105; ISO/IEC AWI TS 42119-7; ISO/IEC FDIS 27090; ISO/IEC 5392:2024; ISO Guide 73:2009; EU AI Act 2024/1689; NIST AI RMF 1.0; Canada Directive on Automated Decision-Making; arc42; verifywise.ai; holisticai; digital.nemko; Schellman.*
