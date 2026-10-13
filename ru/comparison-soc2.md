# ISO/IEC 42001 vs SOC 2: для US-рынка

> 🇬🇧 [Read in English](../comparison-soc2.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** SOC 2 — главный compliance-фреймворк для US enterprise-клиентов. ISO/IEC 42001 покрывает AI-специфику, которую SOC 2 не адресует. Большинство аудиторов (Schellman, A-LIGN, Coalfire) предлагают combined audit SOC 2 + ISO 42001 со скидкой 30–50 %. Лучший паттерн для US SaaS: SOC 2 Type II как базис, ISO 42001 как AI-надстройка.

---

## Содержание

- [1. Главные различия](#1-главные-различия)
- [2. Trust Services Criteria и Annex A 42001](#2-trust-services-criteria-и-annex-a-42001)
- [3. Combined audit SOC 2 + ISO 42001](#3-combined-audit-soc-2--iso-42001)
- [4. Что выбрать для разных сценариев](#4-что-выбрать-для-разных-сценариев)

---

## 1. Главные различия

| Параметр | SOC 2 | ISO/IEC 42001 |
|----------|-------|----------------|
| Тип | Аттестация (AICPA SSAE 18) | Сертификация (ISO/IEC) |
| Юрисдикция | США (исторически), глобально как фактический стандарт | Международный |
| Аудитор | CPA-firm | ANAB/UKAS-аккредитованный CB |
| Объект | Trust Services Criteria (Security, Availability, Confidentiality, Processing Integrity, Privacy) | AI management system |
| Срок действия | Type I — point-in-time; Type II — период (обычно 6–12 мес) | 3 года |
| Управленческая система | Не требуется как формальная конструкция | Обязательна (Annex SL) |
| Annex A controls | TSC criteria (~64–195 в зависимости от scope) | 38 контролей |
| Public/private | Отчёт SOC 2 — конфиденциальный, передаётся под NDA | Сертификат публичный |
| Подходит для | US enterprise B2B, особенно finance, healthcare, SaaS | AI-провайдеры, Microsoft SSPA, EU AI Act |

---

## 2. Trust Services Criteria и Annex A 42001

SOC 2 покрывает 5 категорий **Trust Services Criteria (TSC)**:

- **Security (Common Criteria)** — обязательная.
- **Availability** — опциональная.
- **Confidentiality** — опциональная.
- **Processing Integrity** — опциональная.
- **Privacy** — опциональная.

| TSC | Annex A 42001 | Перекрытие |
|-----|----------------|-------------|
| CC1 Control Environment | A.2.2 AI Policy, A.3.2 Roles | Высокое |
| CC2 Communication | Clause 7.4 | Высокое |
| CC3 Risk Assessment | Clause 6.1, A.5 AISIA | Среднее (SOC 2 покрывает classic risks, 42001 добавляет AI) |
| CC4 Monitoring | Clause 9.1, A.6.2.6 | Высокое |
| CC5 Control Activities | Annex A controls | Среднее |
| CC6 Logical/Physical Access | A.4 Resources | Высокое (для security) |
| CC7 System Operations | A.6 Lifecycle | Среднее (42001 более глубоко по AI lifecycle) |
| CC8 Change Management | Clause 6.3, A.6.2.5 | Высокое |
| CC9 Risk Mitigation | A.5 + A.6 | Среднее |
| Availability | A.6.2.6 Operation | Среднее |
| Processing Integrity | A.6.2.4 V&V | Высокое (42001 даёт AI-специфику) |

**Чего нет в SOC 2 (но есть в 42001):**
- AI System Impact Assessment (A.5).
- Уровни human oversight (A.6.1.2).
- Annex A.7 Data for AI (lineage, provenance).
- Annex A.8 Information for stakeholders (AI-specific disclosures).

**Чего нет в 42001 (но есть в SOC 2):**
- Privacy detailed criteria (если применима P-категория).
- Detailed physical security controls.
- Vendor management deeper formalism.

---

## 3. Combined audit SOC 2 + ISO 42001

CBs, активные в combined SOC 2 + ISO 42001:
- **Schellman** — лидер рынка, первый ANAB-аккредитованный CB по 42001.
- **A-LIGN**.
- **Coalfire**.
- **BDO**, **EY CertifyPoint**.

**Экономия:** 30–50 % vs два отдельных аудита. Это работает потому, что:
- Один scope statement для обоих.
- Один risk register (с AI-секцией).
- Одна программа internal audit.
- Одно management review с AI-блоком.
- Combined SoA с тэгами SOC 2 / ISO 42001.

**Сроки:** combined audit для SaaS 50–200 FTE — 6–12 месяцев от kickoff до отчётов SOC 2 и сертификата 42001.

**Бюджет combined:** $80–250 тыс. в год 1 в зависимости от размера и зрелости.

---

## 4. Что выбрать для разных сценариев

### Только US-рынок, SaaS B2B

**Старт:** SOC 2 Type II. Cybersecurity-первый покупатель ждёт SOC 2.
**Через 6–12 мес:** добавить ISO 42001 при наличии AI-функций в продукте.

### EU-рынок и/или Microsoft SSPA

**Старт:** ISO 27001 + ISO 42001. SOC 2 не покрывает AI-специфику Microsoft SSPA Section K и не даёт presumption of conformity по EU AI Act.

### И US, и EU enterprise

**Старт:** combined SOC 2 + ISO 27001 + ISO 42001. Это максимальное покрытие.

### Healthcare с PHI

**Старт:** SOC 2 + HIPAA. ISO 42001 — при AI-функциях, влияющих на medical decisions.

### FinTech, банки

**Старт:** SOC 1 (financial reporting) + SOC 2 + ISO 27001. ISO 42001 — при AI-моделях для скоринга/AML/KYC.

---

## Нужна помощь с выбором SOC 2 vs ISO 42001?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Соберём карту юрисдикций и compliance-требований ваших клиентов, предложим минимальный достаточный набор.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Сравнение с ISO 27001](./comparison-iso-27001.md)
- [Сравнение с EU AI Act](./comparison-eu-ai-act.md)
- [Microsoft SSPA — supplier requirements](./supplier-requirements.md)
- [Стоимость и сроки](./cost-timeline.md)

---

*Источники: AICPA SSAE 18; SOC 2 Trust Services Criteria 2017 (updated 2022); ISO/IEC 42001:2023 Annex A; Schellman SOC 2 + ISO 42001 guides; A-LIGN; Coalfire; BDO; EY CertifyPoint; Vanta SOC 2 vs ISO 42001 comparison; Drata; Sprinto.*
