# Публичные кейсы сертификации ISO/IEC 42001

> 🇬🇧 [Read in English](../case-studies.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **Что это.** Детальный разбор 10+ публично подтверждённых сертификаций ISO/IEC 42001 с источниками: пресс-релизы, Trust Centers, статьи аудиторов. Что сертифицировано, scope, сроки, орган сертификации, команда, что было «из коробки» и что наращивали под стандарт. Для краткого списка см. [реестр сертифицированных компаний](./certified-companies.md).

---

## Содержание

- [1. Anthropic (Schellman, январь 2025)](#1-anthropic-schellman-январь-2025)
- [2. AWS (Schellman, ноябрь 2024)](#2-aws-schellman-ноябрь-2024)
- [3. Google Cloud (декабрь 2024)](#3-google-cloud-декабрь-2024)
- [4. Microsoft 365 Copilot, Azure AI, GitHub Copilot (Mastermind/IAS, 2025)](#4-microsoft-365-copilot-azure-ai-github-copilot-mastermindias-2025)
- [5. Workday (Schellman, 2025)](#5-workday-schellman-2025)
- [6. Synthesia (A-LIGN, сентябрь 2024)](#6-synthesia-a-lign-сентябрь-2024)
- [7. IBM Granite (Schellman, сентябрь 2025)](#7-ibm-granite-schellman-сентябрь-2025)
- [8. Cognizant (DNV, декабрь 2024)](#8-cognizant-dnv-декабрь-2024)
- [9. KPMG International (Schellman, декабрь 2025)](#9-kpmg-international-schellman-декабрь-2025)
- [10. Augment Code (количественный кейс)](#10-augment-code-количественный-кейс)
- [11. Общие паттерны успеха](#11-общие-паттерны-успеха)
- [12. Кейс-инцидент: реестр населения Дании и код, написанный ИИ (2026)](#12-кейс-инцидент-реестр-населения-дании-и-код-написанный-ии-2026)

---

## 1. Anthropic (Schellman, январь 2025)

**Сертификат выдан** 6 января 2025, действителен до 5 января 2028. Issuer: Schellman Compliance, LLC (ANAB-accredited). Подписал: Danny Manimbo, Principal, Schellman.

**Scope** (цитата из сертификата):
> «AIMS supporting the AI Research & Development and AI Services for AIMS in the roles as an AI producer as an AI developer and an AI product and service provider, in accordance with statement of applicability, version 1.3, dated November 7, 2024.»

**Покрываемые продукты:** Claude.ai Team Plan, Claude.ai Enterprise Plan, Claude API, Claude Mobile Apps, AI R&D включая модели для партнёров (Bedrock, Vertex AI).

**Важно для FAQ:** Anthropic явно указал, что сертификат относится **только к коммерческим продуктам** (Claude for Work, API). Потребительские планы (Claude Free, Pro, Max) покрыты отдельно — это пример выборочного scope.

**Команда:** Jared Kaplan как Responsible Scaling Officer. Около 8 % сотрудников в security-adjacent областях, но «чистый» AI governance меньше.

---

## 2. AWS (Schellman, ноябрь 2024)

**Сертификат:** 11 ноября 2024. Issuer: Schellman. Surveillance audit ноябрь 2025 — **no findings**.

**Scope:** Amazon Bedrock, Q Business, Textract, Transcribe. Только эти 4 сервиса, не весь AWS.

**Каскадный эффект:** Tim Tutt (Snowflake): «Знание, что у AWS есть ISO 42001-сертифицированные сервисы, даёт нам уверенность... и строит доверие наших клиентов к нашим продуктам».

**Технический фундамент:** AWS Responsible AI Framework на 8 измерениях (fairness, explainability, privacy & security, safety, controllability, veracity & robustness, governance, transparency). AWS публично называет ISO 42001 «foundational standard».

---

## 3. Google Cloud (декабрь 2024)

**Scope:** GCP, Workspace, Gemini app (НЕ весь Alphabet). По индустриальным трекерам — 10 продуктов, включая Vertex AI и Document AI APIs.

**Прямая цитата Google:** «No other generative AI offering has met this level of recognition». Последующая FedRAMP High авторизация — первая для generative AI productivity в US public sector.

**Сертификаты опубликованы:** Cloud Compliance Center.

---

## 4. Microsoft 365 Copilot, Azure AI, GitHub Copilot (Mastermind/IAS, 2025)

Microsoft уникально использует **множество параллельных сертификатов**, каждый со своим SoA:

| Продукт | CB | Дата |
|---------|-----|------|
| Microsoft 365 Copilot | Mastermind (IAS) | март 2025 (до марта 2028), сертификат №MMIND-25032001 |
| Azure AI Foundry + Security Copilot | Mastermind | 2025 |
| Copilot Studio | Mastermind (IAS) | 2025 |
| Dragon Copilot, Foundry, GitHub Copilot | разные | 2025 |

**Scope для M365 Copilot:** «Management system supporting M365 Copilot and M365 Copilot Chat offerings; M365 Trusted Platform, Responsible AI, Security, Privacy teams; роли AI Developer и AI Provider; SoA v2.0».

**Дополнительно:** Microsoft первым получил CSA STAR for AI 42001 Level 2 — industry-first.

**Команда:** Natasha Crampton, Chief Responsible AI Officer. Около 350 человек на Responsible AI работах (129 full-time по данным 2023, сейчас больше). Hub-and-spoke: Office of RAI + AETHER (research) + Responsible AI Council во главе с Brad Smith и Kevin Scott.

---

## 5. Workday (Schellman, 2025)

**Сертификат №1355199-2**, выдан в 2025 (срок действия 3 года).

**Scope** (цитата): «AIMS supporting following product lines: HCM, Financial Management, Student, Spend Management, Adaptive Planning, Peakon, Payroll, Workforce Management, Talent Management, Analytics & Reporting, HiredScore, Platform & Product Extensions; роли AI Producer и AI Provider; SoA v2025.02 от 1 июля 2025; sites: Pleasanton, Boulder, Atlanta, Beaverton, Vancouver BC, Dublin, London, Tel Aviv».

**12 продуктовых линий** в одном сертификате. Workday обслуживает >60 % Fortune 500 — сертификат становится gating-credential для закупок Fortune 500.

**Команда:** Kelly Trindel, выделенная RAI-команда с 2022 г., supplemented сетью «RAI champions» по BU. Oversight от RAI Advisory Board под CLO Rich Sauer.

---

## 6. Synthesia (A-LIGN, сентябрь 2024)

**Сертификат:** 25 сентября 2024, A-LIGN. Изначально без аккредитации, «подняли» после witness audit ANAB в октябре 2024.

**Scope:** AI video platform.

**Контекст:** 65 000 клиентов, 70 % Fortune 100 в клиентской базе.

**Прямая цитата** Martin Tschammer, Head of Security:
> «Certification drew media coverage and significant interest from customers, vendors, and other stakeholders».

**Команда:** Martin Tschammer + Security Manager Nicolás Barberis. Отдельной AI-governance команды публично не упомянуто — security-команда плюс Wiz, Vanta, A-LIGN.

**Audit prep:** 1 FTE × 4 недели при готовом ISMS (модель Modulos/Xayn).

---

## 7. IBM Granite (Schellman, сентябрь 2025)

**Сертификат:** середина сентября 2025, для Granite open-source LLM (лицензия Apache 2.0). Анонс совпал с выпуском Granite 4.0 в октябре 2025.

**Scope:** Только модели семейства Granite (language models) как AI Producer (AI developer). Не вся платформа watsonx.ai.

**Заявление «3 месяца» — критическая интерпретация:**
> «The process was completed in under three months and resulted in zero non-conformities» (IBM пресс-релиз).

«3 месяца» = от **kickoff аудита до certification decision**, не «от нуля до сертификата». IBM уже имел зрелую систему governance, ISO 27001/27017/27018/27701, программу Responsible AI, watsonx.governance, прочные SDLC-практики.

**Реалистичные сроки:**
- Зрелая компания с ISMS/PIMS: 3–6 месяцев.
- С нуля: 6–12 месяцев.
- Стартап с неформализованными процессами: 9–18 месяцев.

**Цитаты:**
- David Cox, VP AI Models, IBM Research: «We're honored to earn ISO 42001 certification for our flagship Granite models. Granite is now the first open model family to meet that bar».
- Avani Desai, CEO Schellman: «IBM has now set an important precedent for how transparency, accountability, and innovation can coexist».

**Сопутствующие меры:** криптографическая подпись контрольных точек Granite 4.0 на Hugging Face, bug-bounty через HackerOne (до $100 000), неограниченная indemnity за IP-претензии при использовании Granite в watsonx.ai.

---

## 8. Cognizant (DNV, декабрь 2024)

Первая глобальная IT-services компания. Развернула на **300 000+ сотрудников** и запустила консалтинг для клиентов по их собственной сертификации — прямой revenue stream.

**Мотивы (HFS Research):** competitive differentiation, client trust, regulatory anticipation.

---

## 9. KPMG International (Schellman, декабрь 2025)

Первый Big Four на международном уровне.

**Цитата** Steve Chase, Global Head of AI: «Scaling AI and governance go hand in hand».

Прямо позиционируется как «необходимый precursor к оказанию AI-assurance услуг клиентам» — revenue link.

---

## 10. Augment Code (количественный кейс)

Кейс с **цифрами от вендора** (единственный источник: YSecurity case study — воспринимать как ориентир):

- **7-figure deal закрыт за 93 дня** после сертификации.
- **CAC -64,9 %**.
- **Security-calls 6→2/неделю**.
- **Enterprise deal закрыт за 2 дня** после сертификации.

Это наиболее количественно подтверждённый публичный ROI-кейс на 2026.

---

## 11. Общие паттерны успеха

Что объединяет успешные сертификации:

### Узкий, чёткий scope
За исключением Anthropic (формулирует через организационные функции), все крупные сертификации скоупируются по продуктам/сервисам. Microsoft уникален — несколько параллельных сертификатов.

### Зрелый фундамент ISO 27001 или эквивалент
IBM, Workday, Anthropic — все имели зрелую ISMS/security/governance. Это сокращает срок на 40–60 %.

### CISO/Head of Security как AIMS lead
Synthesia (Martin Tschammer), Evisort (CTO Amine Anoun). Полноценный отдельный AI Governance Officer — только в Microsoft и других big tech.

### Fractional advisor или внешний CB-preparation
Все используют либо внешний gap analysis, либо fractional advisor, либо consulting от партнёров. Чисто in-house с нуля — редкость.

### Расширение scope на ресертификации
Integral Ad Science (февраль 2026) — initial cert + scope expansion на ресертификации добавил «Quality Attention» и «Ad Fraud solutions». Microsoft — отдельные сертификаты на каждый новый Copilot-продукт.

### Прозрачность сертификата
Все опубликовали Trust Center или публичный сертификат. Это часть маркетинговой ценности.

---

## 12. Кейс-инцидент: реестр населения Дании и код, написанный ИИ (2026)

Кейсы 1–10 показывают, кто получил сертификат. Этот – инцидент, и честно скажем: ISO/IEC 42001 эту атаку **не остановила бы**, потому что ИИ был на стороне злоумышленника. Мы включили кейс ради другого: что он говорит про ИИ внутри вашей компании. Расследование продолжается, детали могут измениться.

**Что произошло.** С 10 сентября 2026 года через законный доступ небольшой IT-компании (Pays ApS) к центральному реестру населения Дании шла массовая выгрузка. Имена, адреса и персональные номера примерно **8,8 млн человек** оказались у злоумышленника, а запросов было больше **14 млн** примерно за десять дней. Сам реестр никто не взламывал: каждый запрос формально укладывался в права подрядчика, их было слишком много. Заметили 2 октября, и не система безопасности, а необычно большой счёт за запросы.

**Роль ИИ.** По словам хакера (Politiken, пересказ TV 2 Fyn), программу для массовых запросов написал ИИ, и двое экспертов, видевших код, с этим согласились. Хакер уверяет, что справилась бы любая модель за последний год. Власти это не подтверждали. Ошибка в коде тоже была: программа искала людей 1877 года рождения вместо 1977.

**Почему это важно для AIMS.** Если один человек со скриптом, написанным ИИ, может сделать 14 млн запросов, то же возможно и изнутри вашей компании: от сотрудника, подрядчика или ИИ-ассистента, который уже подключён к клиентским данным (чат-бот, ассистент в CRM, автоматизация в поддержке). По сути это подрядчик с ключом: работает быстро и без выходных, и часто никто не знает, кто за него отвечает. Именно для такой ситуации написан ISO/IEC 42001. Приложение A просит:

- назначить ответственного за каждую ИИ-систему и определить, для чего её используют (A.3 внутренняя организация, A.9 использование ИИ-систем);
- вести журнал того, что система делает, и следить за её поведением в эксплуатации, чтобы тысячекратный рост запросов увидели вы, а не бухгалтерия (A.6 жизненный цикл ИИ-системы);
- проверять поставщиков ИИ-сервисов, которым вы передаёте данные (A.10 третьи стороны и клиенты);
- задать правила использования ИИ сотрудниками, в том числе внешних сервисов (A.9).

Подробности по мерам: [контроли Annex A](./annex-a-controls.md). Сторона информационной безопасности в этой же истории (пароли, закрытие доступа при уходе сотрудника, контроль подрядчиков) закрывается ISO/IEC 27001. Структура у двух стандартов общая, поэтому их удобно строить вместе: [интегрированная система менеджмента](./integrated-management-system.md).

Источники:

- [TV 2 Fyn – ИИ использовали при утечке](https://www.tv2fyn.dk/fyn/kunstig-intelligens-blev-brugt-i-omfattende-cpr-laek-e6a7e) (на датском).
- [DR/Ritzau – 1 039 компаниям ужесточили требования к безопасности](https://www.dr.dk/nyheder/politik/1039-virksomheder-har-faaet-indskaerpet-sikkerhed-efter-cpr-laek) (на датском).
- [Copenhagen Post – пароль «123456» в утечке CPR](https://cphpost.dk/2026-10-10/general/123456-password-used-in-massive-danish-cpr-data-breach/) (на английском).
- [CSIS – разбор утечки CPR](https://www.csis.com/csis-tech-blog/the-hub/cpr-breach-denmark) (на английском).

---

## Что НЕ работает (типовые ошибки)

- Исключение high-risk систем для облегчения аудита (red flag для аудиторов).
- Размытый scope, который становится audit-unfalsifiable.
- Игнорирование third-party AI компонентов (OpenAI API, Anthropic, Google) в supplier register.
- Отсутствие AI inventory с автоматизацией.
- «Shelfware AIMS» — формальные документы без работающих процессов.

Подробнее — [топ-15 типичных audit findings](./common-audit-findings.md).

---

## Нужна помощь с подготовкой к сертификации?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу ситуацию по аналогии с релевантным кейсом: scope, команда, фундамент 27001, выбор CB.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Реестр публично сертифицированных компаний](./certified-companies.md)
- [Аккредитованные органы сертификации](./anab-accredited-cbs.md)
- [Топ-15 типичных audit findings](./common-audit-findings.md)
- [Стоимость и сроки](./cost-timeline.md)

---

*Источники: пресс-релизы Anthropic, AWS, Google Cloud, Microsoft, Workday, Synthesia, IBM, Cognizant, KPMG; Schellman, A-LIGN, BSI, Mastermind, DNV; HFS Research; Tibor Blaho (Threads); IBM Think; Anthropic Privacy Center; AWS Trust Center; Google Cloud Compliance Center; Microsoft Trust Center; Workday Trust; Synthesia case studies; YSecurity (Augment Code); Vanta case study (Factory); Modulos/Xayn; Forbes (Альянс в сфере ИИ); ISACA; A-LIGN benchmark 2025.*
