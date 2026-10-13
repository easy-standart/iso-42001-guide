# SaaS на базе LLM API (OpenAI, Anthropic, Google) + ISO/IEC 42001

> 🇬🇧 [Read in English](../saas-llm.md) · ⬅ [На главную](./README.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** Большинство современных SaaS-стартапов строят свой AI-функционал на базе foundation моделей через API: OpenAI, Anthropic, Google, Mistral. По ISO/IEC 22989 §5.19 такой SaaS одновременно играет роли **AI Customer** (потребляя LLM) и **AI Producer/Provider** (создавая собственный продукт). Сертификация ISO 42001 для wrappers возможна — пример Anthropic, Evisort, UiPath, Snowflake, FloQast. Главные особенности: scoping на application-layer (не foundation model), правильное использование Annex A.10 (третьи стороны), Shared Responsibility Model по CSA AICM v1.0.

---

## Содержание

- [1. Распределение ролей по 22989](#1-распределение-ролей-по-22989)
- [2. Стратегии scoping](#2-стратегии-scoping)
- [3. Annex A.10 и flow-down upstream-требований](#3-annex-a10-и-flow-down-upstream-требований)
- [4. Юридическая основа upstream-провайдеров](#4-юридическая-основа-upstream-провайдеров)
- [5. Реальные кейсы сертифицированных LLM-SaaS](#5-реальные-кейсы-сертифицированных-llm-saas)
- [6. CSA AICM v1.0 и Shared Responsibility Model](#6-csa-aicm-v10-и-shared-responsibility-model)
- [7. Референтный шаблон SoA для LLM-SaaS](#7-референтный-шаблон-soa-для-llm-saas)

---

## 1. Распределение ролей по 22989

| Слой стека | Пример | ISO/IEC 22989 роль |
|------------|--------|---------------------|
| Foundation model provider | OpenAI, Anthropic, Google, Mistral, Cohere, Meta | AI Producer (и частично AI Provider через API) |
| Cloud-гиперскейлер, перепродающий LLM | AWS Bedrock, Azure OpenAI Service, Google Vertex AI | AI Platform Provider |
| SaaS-компания на LLM (RAG, fine-tuning, prompt engineering, guardrails) | Evisort, FloQast, Eightfold, Noxtua | **AI Customer + AI Producer/Provider** |
| Корпоративный покупатель SaaS | Банк, клиника, ритейлер | AI Customer |
| Конечный пользователь | Сотрудник банка / врач / покупатель | AI User |
| Физлицо, на которое влияет решение | Заявитель на кредит / пациент / кандидат | AI Subject |

**Anthropic сертифицирован как «AI producer, AI developer, AI product and service provider»** — это шаблон для SaaS с серьёзной разработкой.

---

## 2. Стратегии scoping

| Стратегия | Что входит | Плюсы | Минусы |
|-----------|------------|-------|--------|
| **Full-stack** | Foundation model + RAG + приложение | Максимальная «covered surface» | Организация не контролирует foundation model ⇒ риск отказа в сертификации |
| **Application-layer (рекомендуется)** | Собственный fine-tuning, RAG-ингестия, prompt engineering, guardrails, мониторинг, content filtering, инцидент-менеджмент | Реалистичный, auditable scope | Требует чёткого SoA с оговорками по A.10 |
| **Deployer-only** | Компания не модифицирует модель, только использует | Минимальные обязательства | Ограниченная ценность сертификации |

Schellman и другие CB **признают роль «AI Producer + Provider» даже для wrappers**, при условии, что организация выполняет существенные развертывания: fine-tuning, RAG, prompt engineering, safety classifiers. Evisort получила ISO 42001 как AI producer/provider именно в такой модели.

---

## 3. Annex A.10 и flow-down upstream-требований

Annex A.10 (resources for AI systems / third-party AI) требует:

- **A.10.2** — supplier processes and practices (due diligence перед выбором foundation-model-провайдера).
- **A.10.3** — allocation of responsibilities (shared-responsibility-matrix).
- **A.10.4** — supplier agreements (контрактные требования в TOS).

**Частая ошибка:** «Мы сертифицированы, потому что наш LLM-провайдер сертифицирован».

Это **неверно**. ISO 42001 сертифицирует organizational management system, а не переносит её транзитивно. Организация сама обязана:

1. Выполнить AISIA по своей реализации.
2. Определить SoA, где upstream-модель исключена из прямого контроля, но покрыта через A.10.
3. Подтвердить, что supplier-контракт отражает требования (data retention, opt-out из обучения, инцидент-нотификация).

---

## 4. Юридическая основа upstream-провайдеров

| Провайдер | Ключевые положения |
|-----------|---------------------|
| **OpenAI Enterprise Terms** | API-inputs/outputs не используются для обучения по умолчанию; data residency (EU, US, JP, UK, AU, KR, AE и др.); Zero Data Retention (ZDR) доступен для eligible enterprise-проектов при одобрении; Enterprise Key Management (BYOK); HIPAA через BAA для ZDR-проектов |
| **Anthropic Commercial Terms** | Prompts/outputs не используются для обучения; SOC 2 Type II; ISO 42001 с 6 января 2025; HIPAA BAA |
| **Azure OpenAI Service** | По умолчанию 30-дневная retention для abuse-monitoring; ZDR (Modified Abuse Monitoring) — только gated, требует EA/MCA и approval от Microsoft MAR team; 3 deployment types (Global, DataZone, Regional) с разными гарантиями data residency; HIPAA BAA через Microsoft Online Services DPA |
| **Google Vertex AI** | Inputs не используются для обучения foundation models; data residency по регионам |
| **AWS Bedrock** | Inputs не используются для обучения; AWS-контроли PCI DSS, HIPAA BAA, FedRAMP |

Эти положения должны быть зафиксированы в supplier register и регулярно ревьюиться (минимум ежегодно).

---

## 5. Реальные кейсы сертифицированных LLM-SaaS

- **Anthropic** — 6 января 2025, Schellman. Scope: «AI Research & Development and AI Services, AI producer + AI developer + AI product and service provider».
- **Snowflake** — одна из первых cloud data companies. AI-stack: Snowflake Cortex AI, маршрутизируемый через Azure OpenAI, Anthropic, Meta, Mistral.
- **UiPath** — ISO/IEC 42001:2023, Schellman. Multi-LLM-routing (Azure/AWS/Google/Anthropic) с AI Trust Layer.
- **Evisort** — одна из первых AI компаний с ISO 42001. Роль «AI producer and provider»; built-in LLM для контрактов.
- **FloQast** — accounting AI, январь 2025, Schellman. Использовал собственное FloQast Compliance Management для сбора evidence.
- **Workday, Eightfold** — см. HR-tech.
- **StackAware, Noxtua (legal AI), Xayn** — публично заявили о движении к ISO 42001.

Подробнее в [`case-studies.md`](./case-studies.md).

---

## 6. CSA AICM v1.0 и Shared Responsibility Model

**Cloud Security Alliance AI Controls Matrix (AICM)** — первый vendor-agnostic control framework для cloud-AI, выпущен 10 июля 2025.

- **243 контроля в 18 доменах.**
- **Shared Security Responsibility Model (SSRM)** распределяет ответственность между 5 ролями:
  - **CSP** — Cloud Service Provider (AWS, Azure, GCP).
  - **MP** — Model Provider (OpenAI, Anthropic, Google).
  - **OSP** — Orchestrated Service Provider (Bedrock, Azure OpenAI Service).
  - **AP** — Application Provider (ваш SaaS).
  - **AI Customer** — конечный клиент.
- Маппинг к ISO 42001, ISO 27001, NIST AI RMF 1.0, BSI AIC4 выпущен в августе 2025. Маппинг к EU AI Act — позже.
- Сопровождающий **AI-CAIQ** — основа для upcoming STAR for AI certification.

Для ISO 42001 SaaS-поставщик может использовать AICM как «operational layer» под Annex A: CSA-контроли отвечают на «как», а Annex A — на «что требуется подтвердить».

---

## 7. Референтный шаблон SoA для LLM-SaaS

| Контроль Annex A | Applicable | Обоснование | Владелец |
|-------------------|------------|-------------|----------|
| A.2.2 AI Policy | Да | Компания публикует Responsible AI Policy | Application Provider (AP) |
| A.3.2 Roles | Да | Chief Responsible AI Officer, AI Review Board | AP |
| A.5.2 AISIA | Да | AISIA-шаблон с ссылкой на EU AI Act FRIA | AP |
| A.6.2.2 Objectives | Да | Для каждого AI-feature | AP |
| A.6.2.3 Design and development | Частично | Foundation model out-of-scope; fine-tuning, RAG, prompts in-scope | AP (in-scope); Model Provider (upstream) |
| A.6.2.4 V&V | Да | Red-teaming, безопасность вывода, hallucination rate | AP |
| A.6.2.5 Deployment | Да | CI/CD pipeline, canary releases | AP |
| A.6.2.6 Operation / monitoring | Да | Observability, drift detection | AP |
| A.6.2.7 Updates | Да | Change management | AP |
| A.6.2.8 Re-evaluation | Да | Annual review | AP |
| A.7.2 Data for AI | Частично | Собственные данные — полный контроль; foundation model training data — out-of-scope, обоснование через A.10 | AP |
| A.7.3–A.7.6 Data sources, quality, lineage, preparation | Да (для своих) | Свои данные подробно | AP |
| A.8.2–A.8.5 Information for stakeholders | Да | User-facing disclosures, AI disclaimer, channels for AI subjects | AP |
| A.9.2–A.9.4 Use of AI | Да | Acceptable Use Policy для клиентов | AP |
| A.10.2 Supplier processes | Да | Due diligence на OpenAI/Anthropic/Google | AP |
| A.10.3 Allocation of responsibilities | Да | Shared responsibility matrix | AP + MP |
| A.10.4 Supplier agreements | Да | DPA с opt-out, ZDR, HIPAA BAA | AP |

Подробнее по контролям — в [`annex-a-controls.md`](./annex-a-controls.md).

---

## Нужна помощь со scoping LLM-SaaS под 42001?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу архитектуру, роли, scope statement и SoA — что включить, что вынести в A.10, какие upstream-контракты нужны.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Обзор стандарта 42001](./overview.md)
- [GenAI/LLM-specific controls (детально)](./genai-llm-specific-controls.md)
- [Shadow AI Policy шаблон](./shadow-ai-policy-template.md)
- [Кейсы Anthropic, Evisort, FloQast, UiPath](./case-studies.md)
- [Требования поставщикам Microsoft SSPA](./supplier-requirements.md)

---

*Источники: ISO/IEC 22989:2022 §5.19; Anthropic Certificate (Schellman, 6 января 2025); Schellman; Sensiba; OpenAI Enterprise Terms; OpenAI Data Controls; Anthropic Commercial Terms; Microsoft Azure OpenAI Service Q&A; Microsoft Modified Access Review; Google Vertex AI; AWS Bedrock; CSA AI Controls Matrix v1.0 (10 июля 2025); Tripwire; AIGL blog; PR Newswire (Evisort); GlobeNewswire (FloQast); Snowflake; UiPath; StackAware; Noxtua; Xayn; Oxebridge.*
