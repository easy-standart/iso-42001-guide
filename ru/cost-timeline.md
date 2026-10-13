# Сколько стоит ISO/IEC 42001: финансовая модель CEO

> 🇬🇧 [Read in English](../cost-timeline.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** Сертификация ISO/IEC 42001 — инвестиция $55–340 тыс. за первые 3 года для типового SaaS с уже работающим ISO 27001. Без ISO 27001 — $200–325 тыс. и 12–18 месяцев. Реальные диапазоны зависят от scope, размера компании, выбора CB и стартовой compliance-зрелости. Цифры агрегированы из публичных материалов Schellman, Coalfire, A-LIGN, BSI, Vanta, Drata, PECB, Elevate, CertBetter, Reconn, Glocert, Cycore. Все котировки колеблются ±30 %.

---

## Содержание

- [1. 3-летняя TCO по сегментам](#1-3-летняя-tco-по-сегментам)
- [2. Декомпозиция по статьям](#2-декомпозиция-по-статьям)
- [3. Длительность проекта](#3-длительность-проекта)
- [4. Маржинальная стоимость bolt-on к ISO 27001](#4-маржинальная-стоимость-bolt-on-к-iso-27001)
- [5. Зарплаты команды AIMS](#5-зарплаты-команды-aims)
- [6. ROI: триггеры окупаемости](#6-roi-триггеры-окупаемости)

---

## 1. 3-летняя TCO по сегментам

| Профиль | TCO низ | TCO середина | TCO верх |
|---------|---------|---------------|----------|
| Малый SaaS, 50 FTE, ISO 27001 уже есть | $55 тыс. | $95 тыс. | $160 тыс. |
| Малый SaaS, 50 FTE, с нуля (без ISMS) | $80 тыс. | $130 тыс. | $210 тыс. |
| Mid-market, 200 FTE, ISO 27001 есть | $120 тыс. | $210 тыс. | $340 тыс. |
| Mid-market, 200 FTE, с нуля | $180 тыс. | $290 тыс. | $450 тыс. |
| Enterprise, 1000 FTE, зрелый ISMS | $280 тыс. | $480 тыс. | $750 тыс. |
| Enterprise, сложный AI-портфель, multi-region | $400 тыс. | $700 тыс. | $1,2 млн+ |

**Правило больших чисел:** ISO 42001 стоит **60–80 %** от ISO 27001-эквивалента, если ISO 27001 уже работает, и **120–150 %** при старте с нуля. Премия объясняется тем, что AISIA по ISO 42005 не имеет аналога в ISO 27001, аудиторов мало (около 50–60 аккредитованных по миру в начале 2026), а контроли Annex A требуют документации, которой в SaaS «по умолчанию» нет.

---

## 2. Декомпозиция по статьям

### Gap-анализ (внешний readiness assessment)

| CB | Малый | Средний | Enterprise |
|----|--------|---------|-------------|
| Schellman / risk3sixty | $15–25 тыс. | $25–45 тыс. | $50–90 тыс. |
| Coalfire (workshop-формат) | -30–40 % к Schellman | -30–40 % | -30–40 % |
| Vanta-партнёры (Workstreet, Reconn) | $3–8 тыс. («лёгкий» gap) | — | — |

Публичный кейс: fintech в Мельбурне заплатил AUD 12 000 (~$8 тыс.) за 4-дневный gap при действующем ISO 27001.

### Консалтинг и сопровождение внедрения

- Дневная ставка специалиста по AI governance: $1 500–3 500/день (US/EU). Big Four — в 2–3 раза выше.
- **Малый SaaS:** $40–90 тыс. (Schellman/risk3sixty mid-market). Или fractional advisor $10–15 тыс./мес × 4–6 месяцев.
- **Mid-market:** $80–250 тыс. (Mastermind, Modulos, Holistic AI).
- **Enterprise transformation:** $250 тыс. – $1 млн+ (Deloitte/EY/KPMG/PwC).
- Пакеты «полное внедрение за $15 тыс.» — это только шаблоны, не реальная имплементация.

### Внутренние FTE

При нагруженной компенсации $80–150 тыс./год:

| Профиль | Часы | Стоимость |
|---------|-------|-----------|
| ISMS-зрелый малый SaaS | 200–400 ч | $15–32 тыс. |
| Mid-market | 500–900 ч | $40–75 тыс. |
| Enterprise | 1000–1800 ч | $80–150 тыс. |
| При старте с нуля | × 2 | × 2 |

После сертификации — поддержка 0,25–0,5 FTE.

### GRC-инструменты (годовая подписка)

| Инструмент | Базовый тир | Mid-market | Enterprise |
|------------|--------------|-------------|-------------|
| Vanta | $10–20 тыс. (с 42001 add-on) | $25–45 тыс. | $50–80 тыс. |
| Drata | $7,5–12 тыс. (Foundation) | $18–25 тыс. (Advanced) | до $100 тыс. |
| Secureframe | — | $14–70 тыс. | $14–70 тыс. |
| Sprinto | от $4 тыс. | — | — |
| OneTrust AI Governance / Credo AI | без публичного прайса | $30–250 тыс./год | $30–250 тыс./год |

Add-on за каждый дополнительный фреймворк: Drata $1,5–7,5 тыс.; Vanta $5–15 тыс. **Industry rule:** модули ISO 42001 в Vanta/Drata/Sprinto добавляют $7,5–10 тыс./год к базовой подписке.

### Аудит сертификации (год 1)

| CB | Малый | Средний | Enterprise |
|----|--------|---------|-------------|
| Schellman (первый ANAB-аккредитованный) | $20–25 тыс. | $25–35 тыс. | $35–60 тыс. |
| A-LIGN | $20–25 тыс. | $25–35 тыс. | $35–60 тыс. |
| Coalfire (аккредитован июнь 2025) | -10–20 % | -10–20 % | -10–20 % |
| BSI / DNV (премиум) | $25–40 тыс. | $40–60 тыс. | $60–90 тыс. |
| TÜV SÜD / Rheinland / Bureau Veritas | BSI -20 % | BSI -20 % | BSI -20 % |
| Vanta-сетевые мелкие CB | $7–35 тыс. | — | — |

**Драйвер цены — audit-days (IAF MD 5):** Stage 1 = 1–2 дня, Stage 2 = 2–5 дней (малый) до 30 дней (enterprise) при ставке $2,5–4 тыс./день.

### Surveillance audits (годы 2 и 3)

Жёсткий стандарт индустрии — **~1/3 от первоначального аудита**:
- Малый SaaS — $5–9 тыс./год.
- Mid-market — $9–18 тыс./год.
- Enterprise — $18–35 тыс./год.

### Re-certification (год 4)

60–70 % от первоначального:
- Малый — $10–18 тыс.
- Средний — $18–32 тыс.
- Enterprise — $30–55 тыс.

### Обучение

- **PECB:** Foundation $500 + $200 cert; Lead Implementer $1 000 + $500 cert; Lead Auditor $1 000 + $500 cert; ежегодный maintenance $100.
- Партнёрские курсы: Foundation $799–1 798; Lead Implementer $799–3 000; Lead Auditor $799–3 500.
- BSI Lead Auditor $2 800–4 000.
- Awareness для всей компании — $18–30/чел./год.
- Бюджет: $2–5 тыс. малый, $8–18 тыс. mid, $25–60 тыс. enterprise.

---

## 3. Длительность проекта

- При зрелом ISO 27001 и одной AI-системе: **3–6 месяцев**.
- При нескольких AI-системах: **4–9 месяцев**.
- Старт с нуля для малой организации: **6–12 месяцев**.
- Enterprise: **12–18 месяцев**, иногда 24.

---

## 4. Маржинальная стоимость bolt-on к ISO 27001

| Статья | Cold (без 27001) | Bolt-on (есть 27001) |
|--------|-------------------|----------------------|
| Внутреннее усилие | 1,5–2 FTE × 6–12 мес | 0,5–1 FTE × 4–6 мес |
| Консалтинг | $20–40 тыс. | $10–20 тыс. |
| Initial audit | $10–25 тыс. | $5–15 тыс. (combined audit) |
| Annual surveillance | $4–10 тыс. | $2–5 тыс. incremental |
| Tooling | $20–60 тыс./год | $5–20 тыс./год add-on |
| **Year 1 all-in** | **$60–150 тыс.** | **$25–60 тыс.** |

40–60 % работы менеджмент-системы переносится. Integrated Management System (IMS) даёт 30 %+ снижение нагрузки compliance-команды (DQS, ISMS.online).

---

## 5. Зарплаты команды AIMS

| Роль | США база | США TC | EU/UK |
|------|-----------|---------|-------|
| AI Governance Analyst (entry) | $80–120K | $90–140K | €60–90K |
| AI Governance Manager / AIMS Lead | $125–200K | $150–250K + bonus + equity | €90–150K |
| AI Compliance / Risk Manager | $125–200K | $150–230K | €90–140K |
| Director / Head of AI Governance | $190–250K | $250–400K + equity | €150–220K |
| VP AI Governance / Chief AI Ethics Officer | $190–280K | $300–500K+ | €180–280K |
| Chief AI Officer | $200–350K | $351K avg, top $643K | €200–350K |

**Источники:** IAPP Salary and Jobs Report 2025–26 (медиана $123K общий digital governance, $151,8K + IT mgmt, $169,7K + infosec; глобальный TC ~$200K); Tech Jacks Solutions (декабрь 2025); Index.dev; Rise AI Talent Report 2026; ZipRecruiter.

**Двойной домен (privacy + AI gov):** ~25 % премия к зарплате; в 25 % случаев перешагивает $200K (IAPP Salary Report 2025–26).

**Forrester (декабрь 2025):** 60 % Fortune 100 назначат head of AI governance к концу 2026.

---

## 6. ROI: триггеры окупаемости

### Microsoft SSPA Sensitive Use
ISO 42001 — единственный путь для Sensitive Use. Без сертификата поставщик дисквалифицирован для самых стратегических workloads Microsoft (десятки миллиардов закупочного объёма в год).

### Каскадный эффект
Сертификат верхнего поставщика капитализируется в продажах его клиентов. Tim Tutt (Snowflake): «Знание, что у AWS есть ISO 42001-сертифицированные сервисы, даёт нам уверенность... и строит доверие наших клиентов».

### Revenue из консалтинга
Cognizant (декабрь 2024) развернул на 300 000+ сотрудников и запустил консалтинг для клиентов по их сертификации — прямой revenue stream. KPMG International (декабрь 2025) — Steve Chase: «Scaling AI and governance go hand in hand».

### Augment Code (количественно)
Закрыли 7-figure deal за 93 дня после сертификации. CAC -64,9 %. Security-calls 6→2/неделю. Источник: YSecurity case study.

### Colorado AI Act + EU AI Act safe harbor
Снижение юридических резервов и ускорение due diligence.

### Procurement-волна 2026–2027
- A-LIGN benchmark (n=1 000+): **76 %** организаций будут требовать сертификации от поставщиков в течение 24 месяцев.
- Vanta State of Trust 2025 (n=2 500+): **80 %** stakeholders требуют верифицированного proof of safe AI; 79 % используют/планируют agentic AI; 62 % увеличивают AI-security бюджет.
- **Gartner (февраль 2026):** к 2030 AI compliance spend достигнет $1 млрд; организации с AI governance platforms в 3,4 раза эффективнее.

### Точка окупаемости для 50-FTE SaaS
Базовая инвестиция $80–160 тыс. за 3 года при ISO 27001 оправдывается одним enterprise-контрактом стоимостью $200K+ ARR.

---

## Что сделать в ближайшие 90 дней

1. Проверьте триггеры: явный спрос enterprise-клиента в RFP / целевой контракт с Microsoft в Sensitive Use / готовность к EU AI Act август 2026.
2. Оцените готовность по [чеклисту](./checklist.md) — оцените долю ✅.
3. Если ISO 27001 нет — параллельно с 42001, бюджет $200–325 тыс.
4. Если есть — выбирайте узкий scope (один продукт), $80–160 тыс. за 3 года.
5. Назначьте CISO/DPO как AIMS-лида + fractional AI governance advisor $10K/мес × 4–6 мес.
6. Запросите котировки у 2–3 CB (Schellman, A-LIGN, Coalfire или BSI).

---

## Нужен персональный расчёт для вашей компании?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Соберём бюджет под ваш конкретный сценарий: размер, scope, наличие 27001, целевой рынок, выбор CB.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Обзор стандарта 42001](./overview.md)
- [Чеклист готовности](./checklist.md)
- [Аккредитованные органы сертификации](./anab-accredited-cbs.md)
- [Публичные кейсы](./case-studies.md)
- [FAQ для руководителя](./faq.md)

---

*Источники: Schellman/risk3sixty; Coalfire; A-LIGN; BSI; DNV; TÜV SÜD/Rheinland/Bureau Veritas; Vanta; Drata; Secureframe; Sprinto; OneTrust AI Governance; Credo AI; Modulos; Holistic AI; PECB; Elevate Consult; CertBetter; Reconn; Glocert; Cycore; Mastermind; IAPP Salary and Jobs Report 2025–26; Tech Jacks Solutions; Index.dev; Rise AI Talent Report 2026; ZipRecruiter; A-LIGN benchmark 2025; Vanta State of Trust 2025; Gartner Newsroom (февраль 2026); Forrester (декабрь 2025); YSecurity (Augment Code case study).*
