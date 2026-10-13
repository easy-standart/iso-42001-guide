# Требования к поставщикам ИИ: Microsoft SSPA DPR v10 и каскад через цепочки закупок

> 🇬🇧 [Read in English](../supplier-requirements.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** С 23 сентября 2024 года Microsoft SSPA DPR v10 ввёл Раздел K — 18 обязательных требований к поставщикам, использующим AI Systems. Сертификат ISO/IEC 42001 явно принимается как замена независимой оценки по Section K. При Sensitive Use он становится обязательным. Гиперскейлеры (AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow) добавляют аналогичные требования через свои Supplier Code, Responsible AI Policy и AI Control Tower. Опросники Shared Assessments SIG 2025/2026, CSA AICM, HECVAT 4 уже маппят разделы прямо на Annex A 42001. Через RFP это всё доходит до подрядчиков второго и третьего уровня.

---

## Содержание

- [1. Microsoft SSPA DPR v10 — что изменилось](#1-microsoft-sspa-dpr-v10--что-изменилось)
- [2. 18 требований Section K — полный перечень](#2-18-требований-section-k--полный-перечень)
- [3. Carve-out для ISO/IEC 42001](#3-carve-out-для-isoiec-42001)
- [4. Sensitive Use — три критерия](#4-sensitive-use--три-критерия)
- [5. Аналоги у AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow](#5-аналоги-у-aws-google-cloud-ibm-salesforce-oracle-servicenow)
- [6. SIG, CAIQ, HECVAT — как ISO 42001 заходит в опросники](#6-sig-caiq-hecvat--как-iso-42001-заходит-в-опросники)
- [7. Тендеры и публичные закупки](#7-тендеры-и-публичные-закупки)
- [8. Практический набор поставщика](#8-практический-набор-поставщика)

---

## 1. Microsoft SSPA DPR v10 — что изменилось

**Supplier Security & Privacy Assurance (SSPA)** — совместная программа Microsoft Procurement, Corporate External and Legal Affairs и Corporate Security. Она доводит до поставщиков документ **Microsoft Supplier Data Protection Requirements (DPR)** и применяется ко всем поставщикам, обрабатывающим Personal Data, Microsoft Confidential Data или использующим **AI Systems** при исполнении контракта.

**Ключевые даты:**

- **23 сентября 2024 года** — DPR v10 вступил в силу. Самое значительное обновление DPR со времён GDPR (2018).
- Самоаттестация обязательна ежегодно. Статус поставщика меняется на «Red» при нарушении 90-дневного окна — новые заказы блокируются до возврата в «Green».
- Поставщикам с годовщиной после 23 сентября 2024 года назначаются новые задачи. Для AI Systems Section K + Independent Assessment должны быть закрыты до открытия Purchase Order и начала любой обработки данных.
- Независимая оценка проводится фирмой из списка Microsoft Preferred Assessors. «Unqualified» Letter of Attestation загружается в портал SSPA.

**Ключевые определения v10:**

- **AI Systems** — «engineered system that applies an optimized model so that the system can, for a given set of human-defined objectives, make predictions, recommendations, or decisions». Определение намеренно охватывает генеративный ИИ.
- **Sensitive Use** — три критерия (см. раздел 4).
- **Red Teaming** — целенаправленное тестирование на ограничения, поверхность рисков и уязвимости.
- **Human Oversight** — три уровня: human-in-the-loop, human-on-the-loop, human-in-command.

---

## 2. 18 требований Section K — полный перечень

Раздел K применяется только к поставщикам, оказывающим услуги с использованием AI Systems. Нумерация по оригинальному DPR v10 (пункты 53–70):

| № | Название | Что должен поставщик |
|---|----------|----------------------|
| 53 | AI Systems contractual terms | В договоре с Microsoft присутствуют специальные положения об ИИ. Изменения Intended Uses раскрываются без задержки, пересмотр не реже раза в год. |
| 54 | Accountability ownership | Назначить конкретное лицо/роль, отвечающую за troubleshooting, операции и контроль на всём жизненном цикле. Документировать мандат. |
| 55 | Annual training | Ежегодное обучение privacy и security для всех, кто работает с данными в AI Systems. Содержание обучения валидируется. |
| 56 | AI System incident response plan | План реакции: уведомление Microsoft, rollback, отключение функций, обновление моделей, коммуникация с клиентами о сбоях и митигациях. |
| 57 | Red Teaming | Red Teaming обязателен, выявленные уязвимости закрываются до деплоя. |
| 58 | Responsible AI program | Документированная программа ответственного ИИ, покрывающая раскрытия и документацию. |
| 59 | Intended Uses Transparency disclosures | Документы о назначении системы, предоставляемые Microsoft по запросу. |
| 60 | Signed Agreement with AI sub-suppliers | При использовании AI-субподрядчиков — договор с разделами по данным, конфиденциальности, IP, ответственности, инцидентам и Sensitive Uses. |
| 61 | Accountability (continuous) | Чёткие линии ответственности за развёртывание и управление рисками. Регулярный мониторинг и аудит моделей. |
| 62 | Risk Assessment | Оценка рисков с учётом bias, уязвимостей, непредвиденных последствий. При Sensitive Uses — дополнительные контроли. Артефакты хранятся. |
| 63 | Transparency and Explainability | Раскрытия по архитектуре модели, обучающим данным, процессу принятия решений. Логирование сбоев, искажений, hallucinations. |
| 64 | Monitoring and Adaptation | Непрерывный мониторинг, адаптация при появлении новых рисков. |
| 65 | Performance & safety disclosures | Допустимые диапазоны ошибок, false positive/negative по каждому Intended Use, документация Sensitive Use, меры против automation bias, ограничения модели, контроли против jailbreaks / data poisoning / prompt extraction, доказательства точности. |
| 66 | Update & notification | Обновление Intended Uses при новых use cases, изменении функциональности, смене стадии релиза, новых данных о безопасности, изменении метрик точности. |
| 67 | System health monitoring / SOP | SOP для каждой системы: воспроизведение сбоев, отслеживаемые события, приоритизация, частота ревью, время устранения, контроль актуальности сторонних компонентов и open source. |
| 68 | Inventory of monitoring methods | Детальная инвентаризация: данные и алерты, механизмы подачи жалоб клиентами, каналы обратной связи от общественности. |
| 69 | Failure of Intended Use procedures | При выявлении непригодности: изъятие из маркетинговых материалов, уведомление клиентов, закрытие разрыва или прекращение эксплуатации, ревизия документации. |
| 70 | Demographic disparity disclosure | Идентификация и раскрытие демографических групп (включая маргинализированные), которые могут получить ухудшенное качество сервиса. Документирование обосновывающих операционных факторов (например, «background noise» для речевых систем). |

Плюс одно требование к Data Subjects (пункт 24) вне Раздела K: поставщик ведёт реестр всех получателей Microsoft Personal Data. Итого 17 новых в Section K + 1 в Section F = **18 новых требований v10**.

---

## 3. Carve-out для ISO/IEC 42001

Microsoft в SSPA Program Guide v10 пишет прямо: «ISO 27701 (privacy), ISO 27001 (security), and ISO 42001 for AI Systems (DPR Section K) are relied on as providing close mapping to the DPR».

Что это значит для поставщика:

- **Валидный сертификат ISO/IEC 42001 принимается вместо независимой оценки по Section K.**
- При **Sensitive Use** сценариях сертификат ISO/IEC 42001 становится **обязательным** и используется как замена Independent Assessment. Сценарий дополнительно проходит ревью Microsoft Office of Responsible AI.
- Scope сертификата и версия DPR должны совпадать. Аттестация под v10 невалидна, если поставщик заполнил DPR v9.

Это первый случай, когда крупный enterprise-заказчик официально приравнял ISO 42001 к собственной программе compliance.

---

## 4. Sensitive Use — три критерия

Точная формулировка из глоссария DPR v10:

> «Sensitive Use» of AI is when the reasonably foreseeable use or misuse of an AI System could affect an individual in the following ways:
> - Consequential impact on legal position or life opportunities.
> - Risk of physical or psychological injury.
> - Threat to human rights.

Эта же триада приведена в Microsoft Responsible AI Standard v2. Sensitive Uses review ведёт **Office of Responsible AI (ORA)** совместно с комитетом **AETHER**.

**Процесс эскалации:**

- В Impact Assessment (подсказки A2.2) команда отвечает на 3 критерия. Если хоть один применим — кейс эскалируется в ORA.
- Sensitive Uses and Emerging Technologies program проводит пре-деплой обзор, часто налагающий требования сверх RAI Standard.
- По Microsoft Responsible AI Transparency Report 2024, **77 %** консультаций касались генеративного ИИ.

**Restricted Uses vs Sensitive Uses:**

- Restricted — запретные сценарии (например, продажа технологии распознавания лиц для нательных камер полиции — публичный отказ Microsoft с 2019 года).
- Sensitive — разрешённые, но требующие дополнительного контроля.

---

## 5. Аналоги у AWS, Google Cloud, IBM, Salesforce, Oracle, ServiceNow

Никто из других гиперскейлеров пока не выпустил публичный документ уровня SSPA DPR v10. Но контракты и политики каскадируют те же требования через другие механизмы.

### AWS

- **Amazon Vendor Security Policy (AVSP)** на базе ISO/IEC 27001/27002 и NIST CSF. Жёсткое ограничение: «Supplier will not develop, train, or improve any AI/ML models using Amazon Information, even if Anonymized».
- **AWS Responsible AI Policy** определяет «consequential decisions» (здоровье, судебные процессы, жильё, занятость, кредиты, медицинские/юридические советы) и требует human oversight и safeguards.
- **AWS Responsible AI Framework** строится на 8 измерениях: fairness, explainability, privacy & security, safety, controllability, veracity & robustness, governance, transparency.
- AWS публично называет ISO 42001 foundational standard. Сам сертифицирован к апрелю 2025 года как major cloud provider.

### Google Cloud

- **Supplier Code of Conduct** задаёт общие ожидания, без AI-специфики.
- **Google AI Principles** (июнь 2018, пересмотр 4 февраля 2025) — пересмотр снял прежние запреты на военные применения.
- **Google Cloud Responsible AI** ведёт двойное ревью: Responsible Innovation team + deal-level review.
- ISO/IEC 42001 для Google Cloud Platform, Google Workspace и Gemini (App) — сертификаты опубликованы в Cloud Compliance Center.

### IBM

- **Supplier Conduct Principles** на базе Responsible Business Alliance Code of Conduct. Социально-экологический management system обязателен для всех first-tier поставщиков с 2010 года.
- **5 Pillars of Trustworthy AI**: fairness, robustness, privacy, explainability, transparency.
- **AI Ethics Board / Responsible Technology Board** ревьюют use cases.
- IBM поставил цель обучить 1000 поставщиков этике ИИ к 2025. К концу 2023 обучено более 600.
- **watsonx.governance** предлагается клиентам как инструмент автоматизации.

### Salesforce

- **Global Supplier Code of Conduct** (июнь 2025).
- **Trusted AI Principles**: Responsibility, Accountability, Transparency, Empowerment, Inclusivity.
- **AI Acceptable Use Policy** требует UI-обозначения автоматизированных взаимодействий.
- **Einstein Trust Layer**: dynamic grounding, zero data retention с LLM-провайдерами, data masking, toxicity detection, audit trail.

### Oracle

- **Supplier Code of Ethics and Business Conduct** — классический compliance-документ, без AI-специфики.
- **CAIQ v4.0** для Oracle Cloud Infrastructure описывает CCM-контроли, опирается на ISO/IEC 27002, SOC 1/2/3, HIPAA, PCI.
- AI-требования к поставщикам формализованы слабо, идут через privacy/security кодекса и ad hoc DPA.

### ServiceNow

- **Code of Business Conduct and Ethics**.
- **Now Assist Guardian / AI Control Tower** — внутренняя платформа для AI stewardship, approval workflows, AI asset inventory. Ссылки на EU AI Act и NIST AI RMF.
- ServiceNow заявил о полном соответствии EU AI Act в течение 24-месячного grace-периода.
- Требует от поставщиков ISO 27001 / SOC 2.

### Сводная таблица

| Вендор | Документ | AI-специфика | ISO 42001 как эквивалент |
|--------|----------|---------------|---------------------------|
| Microsoft | SSPA DPR v10 Section K | 18 обязательных, Sensitive Use ⇒ обязателен | Да, явно (carve-out) |
| AWS | AVSP + Responsible AI Policy | Запрет обучения на данных Amazon, human oversight | Не явно (AWS сам сертифицирован) |
| Google Cloud | Supplier Code + AI Principles | Соблюдение AI Principles + SAIF | Не явно (Google сам сертифицирован) |
| IBM | Supplier Conduct Principles + Trustworthy AI | Обучение 1000 поставщиков; своего DPR нет | Не явно |
| Salesforce | Global Supplier Code + Trusted AI Principles + AI AUP | Раскрытие, Einstein Trust Layer | Не явно (ISO 27001/27701) |
| Oracle | Supplier Code + CAIQ v4 | Без отдельного AI-DPR | Не указано |
| ServiceNow | Code + AI Control Tower / Now Assist Guardian | EU AI Act, NIST AI RMF | Ожидается через VRM |

---

## 6. SIG, CAIQ, HECVAT — как ISO 42001 заходит в опросники

### Shared Assessments SIG

- Владелец Shared Assessments (с 2005, в 2021 приобретён OneTrust).
- **SIG 2025** покрывает 21 risk control domain, ссылается на DORA, NIS2, NIST 2.0.
- **SIG Lite 2025** — 128 вопросов, **SIG Core** — около 850 вопросов.
- **SIG Workbook 2026** (релиз 19 сентября 2025) явно добавляет ISO/IEC 42001 как newly relevant and rapidly maturing framework.

### Cloud Security Alliance — CAIQ v4 и AICM

- **CAIQ v4.0.2** — 261 вопрос по 17 доменам CCM v4. **CAIQ-Lite** — 124 вопроса.
- **AI Controls Matrix (AICM) v1.0** выпущен 10 июля 2025: 243 control objectives в 18 доменах. Модель Shared Security Responsibility (CSP, Model Provider, Orchestrated Service Provider, Application Provider, AI Customer).
- **AI-CAIQ** — опросник для self-assessment под AICM.
- **Маппинг AICM ↔ ISO/IEC 42001** опубликован 20 августа 2025 вместе с **STAR for AI 42001**. Сертифицированная компания загружает сертификат в STAR Registry и, добавив Valid-AI-ted AI CAIQ, получает provisional STAR for AI 42001 Level 2.

### HECVAT 4

- Владелец EDUCAUSE + Internet2 + REN-ISAC.
- **HECVAT 4.1.5** вышел 10 февраля 2025: Full / Lite / On-Prem объединены в один workbook, добавлены AI-specific tab и Privacy tab.
- **AI-tab** оценивает AI risk management, ответственное обучение, AI governance, отключаемость AI-функций, защиту данных от обучения LLM.
- 321 вопрос, согласованы с NIST 800-53, HIPAA, PCI DSS. ISO/IEC 42001 не назван явно, но AI-tab покрывает Annex A.

### Маппинг опросников на Annex A 42001

| Секция опросника | Annex A 42001 | Типичный вопрос |
|-------------------|----------------|-----------------|
| SIG «AI Governance» (2025/2026) | A.2, A.3, A.4 | Есть ли AI Policy, утверждённая board? Кто AI management representative? |
| SIG «Risk Management» | A.5, A.6.1 | Проводится ли AI impact assessment? Документируются ли результаты? |
| SIG «Third-Party Management» | A.10 | Какие контракты обязывают суб-поставщиков к AIMS? |
| CAIQ v4 «GRC» | A.2, A.3, A.9 | Есть ли документированный compliance-план? |
| CAIQ v4 «HRS» | A.4.3 | Обучение персонала работе с ИИ? |
| CAIQ v4 «Data Security and Privacy» | A.7 | Политика training data provenance |
| AICM «Model Security» | A.6, A.8 | Red teaming, защита от jailbreak |
| AICM «Data Security and Privacy» | A.7 | Lineage моделей и наборов обучения |
| AICM «GRC» | A.2, A.3, A.9 | Метрики AI, внутренний аудит |
| HECVAT 4 AI-tab | A.2, A.4, A.5, A.6, A.7, A.9 | Отключаемость AI, training data, governance |

---

## 7. Тендеры и публичные закупки

### Хронология появления 42001 в тендерах

- **Декабрь 2023** — публикация ISO/IEC 42001:2023.
- **2024 (Q2–Q4)** — первые сертификации (Anthropic январь 2025, Snowflake 2024, KPMG, Cognizant, Integral Ad Science, Synthesia, Microsoft Copilot, AWS, Google). Тендеры — «бонусный» характер.
- **Q1 2025** — ISO/IEC 42001 как scoring factor, ещё не блокирующий.
- **Q2–Q4 2025** — в крупных RFP (банки, фарма, страхование, госсектор UK, EU и US федералы) появляются прямые формулировки «требуется ISO 42001 или эквивалент». ISACA 2025 — 76 % организаций планируют использовать ISO 42001 как опорный.
- **Q1 2026** — Pitchbook зафиксировал более 250 корпоративных RFP в ЕС, США и Великобритании с прямыми требованиями ISO 42001.

### Юрисдикции

- **ЕС: TED (Tenders Electronic Daily)** — массовый канал, где 42001 фигурирует в IT-закупках госорганов и национальных компаний.
- **Великобритания** — **UK ATRS** (Algorithmic Transparency Reporting Standard) обязателен для центральных департаментов с 6 февраля 2024. **CCS G-Cloud 15** открывается сентябрь 2026 с бюджетом £14 млрд.
- **США** — **OMB M-25-21** и **M-25-22** (апрель 2025) пересобрали федеральные правила закупок ИИ. ISO 42001 косвенно встроен через crosswalk с NIST AI RMF.
- **Азия** — Сингапур (IMDA AI Verify), Япония, Корея — точечные tenders с упоминаниями.

### Конкурентное преимущество

Из публичных кейсов 2025–2026:

- Time-to-contract сокращается в среднем на 4–8 недель при наличии сертификата.
- Win rate в enterprise сделках с AI-функциями растёт на 15–30 % при равной цене.
- Снимается до 60–80 % вопросов в стандартных security/AI-опросниках.

---

## 8. Практический набор поставщика

Минимальный комплект, который нужен, чтобы войти в цепочки поставок гиперскейлеров и заполнять SIG/CAIQ/HECVAT без переговоров.

**Документы:**

- AIMS Scope Statement (Clause 4.3) — [шаблон](../ru-templates/aims-scope-statement.md).
- AI Policy, утверждённая C-level.
- Реестр AI-систем — [шаблон](../ru-templates/ai-system-card.md).
- Statement of Applicability по 38 контролям Annex A.
- AI Risk Register (по ISO/IEC 23894).
- AISIA на каждую high-risk систему (по [ISO/IEC 42005:2025](./iso-42005-impact-assessment-guide.md)).
- Supplier Register с DPA от каждого AI-провайдера.
- AI Incident Response Playbook — [шаблон](../ru-templates/ai-incident-response.md).
- Red Teaming reports.
- Performance & safety disclosures под Intended Use.

**Процессы:**

- Ежегодное обучение privacy/security для всех, кто работает с AI Systems.
- Drift и bias monitoring с retention логов ≥ 90 дней.
- Каскадирование AIMS-требований субподрядчикам в контрактах.
- Management review минимум раз в год.

**Сертификат:**

- ISO/IEC 42001 от ANAB/UKAS/RvA-аккредитованного CB. Это даёт carve-out у Microsoft и закрывает 60–80 % вопросов в SIG/CAIQ/HECVAT.

---

## Нужна помощь с подготовкой к Microsoft SSPA или enterprise-тендеру?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу ситуацию: где scope попадает в Sensitive Use, какие документы нужны, как перевести AIMS под carve-out.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Обзор стандарта 42001](./overview.md)
- [Чеклист готовности](./checklist.md)
- [GenAI/LLM-specific controls](./genai-llm-specific-controls.md)
- [Shadow AI Policy шаблон](./shadow-ai-policy-template.md)
- [Vendor Risk Assessment для AI](./vendor-risk-assessment-ai.md)
---

*Источники: Microsoft SSPA homepage; DPR v10 PDF (FY25); SSPA Program Guide v10; SC&H (2024); Schellman (2024); Clark Nuber; AWS Vendor Security Policy; AWS Responsible AI Policy; Google AI Principles (ред. 02/2025); Google Cloud Compliance Center; IBM Supplier Conduct Principles; IBM Trustworthy AI; Salesforce Global Supplier Code of Conduct (06/2025); Salesforce Trusted AI Principles; Oracle Supplier Code of Ethics; ServiceNow Code; Shared Assessments SIG 2025; CSA CAIQ v4.0.2; CSA AICM v1.0 (10 июля 2025); CSA STAR for AI 42001 (20 августа 2025); EDUCAUSE HECVAT 4.1.5 (10 февраля 2025); UK ATRS; OMB M-25-21, M-25-22; CCS G-Cloud 15; ISACA AI Governance Benchmark 2025; Pitchbook Q2 2025.*
