# Семейство стандартов ISO/IEC по ИИ

> 🇬🇧 [Read in English](../family-of-standards.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** ISO/IEC 42001 — не одинокий стандарт, а ядро экосистемы из 35+ опубликованных стандартов от технического комитета **ISO/IEC JTC 1/SC 42**. Шесть из них прямо дополняют 42001: 22989 (терминология, нормативная ссылка), 23053 (ML framework), 23894 (risk management), 42005 (impact assessment), 42006 (требования к CBs), 5338 (lifecycle processes). Знание семейства экономит время на внедрении и помогает корректно строить SoA.

---

## Содержание

- [1. ISO/IEC JTC 1/SC 42](#1-isoiec-jtc-1sc-42)
- [2. Шесть ключевых стандартов](#2-шесть-ключевых-стандартов)
- [3. Прочие связанные стандарты](#3-прочие-связанные-стандарты)
- [4. Нормативный статус ссылок в 42001](#4-нормативный-статус-ссылок-в-42001)
- [5. Что появилось в 2025](#5-что-появилось-в-2025)

---

## 1. ISO/IEC JTC 1/SC 42

Технический подкомитет **SC 42 «Artificial intelligence»** создан в 2017 году как первый горизонтальный SC в ISO/IEC JTC 1 («Information technology»). К началу 2026 SC 42 имеет в портфеле >35 опубликованных стандартов и десятки в разработке.

Рабочие группы (Working Groups):
- **WG 1** — Foundational standards.
- **WG 2** — Data.
- **WG 3** — Trustworthiness.
- **WG 4** — Use cases and applications.
- **WG 5** — Computational approaches and characteristics.

Параллельные SC с пересечениями: SC 27 (security), SC 38 (cloud), SC 41 (IoT).

---

## 2. Шесть ключевых стандартов

### ISO/IEC 22989:2022 — Концепции и терминология

- 60 страниц. Опубликован в июле 2022.
- **Единственная нормативная ссылка в ISO/IEC 42001.**
- Разделы: концепции ИИ (5), жизненный цикл AI-системы (6, 8 фаз), экосистема ИИ (7), области применения (8).
- **Свойства trustworthiness (§5.15):** transparency, explainability, controllability, robustness, reliability, resilience, accuracy, safety, security, privacy.
- **Роли (§5.19):** AI provider, AI producer, AI customer, AI partner, AI subject, AI relevant authority.
- Поправка **DAmd 1 «Generative AI»** на стадии Close of voting (документ 88145) — терминология GenAI будет добавлена отдельной поправкой.

### ISO/IEC 23053:2022 — Framework for AI Systems Using ML

- 36 страниц. Опубликован в июне 2022.
- ML pipeline: определение задачи → получение данных → обработка → обучение → V&V → развёртывание → эксплуатация.
- Типы ML: supervised, unsupervised, semi-supervised, reinforcement, transfer learning.
- Нейронные сети и их виды.
- Поправка **DAmd 1 «Generative AI»** на стадии Close of voting.

### ISO/IEC 23894:2023 — Guidance on risk management

- Опубликован февраль 2023. Адаптирован в Европе как **EN ISO/IEC 23894:2024**.
- Зеркалит структуру ISO 31000:2018.
- **Annex A** — objectives относительные для ИИ (value, ethics, performance, trustworthiness).
- **Annex B** — каталог AI-specific risk sources (~19 категорий): сложность среды работы, непрозрачность моделей, дрейф данных, адверсариальные воздействия, проблемы аппаратного обеспечения, отказ системы, воспроизводимость.
- **Annex C** — соотнесение процессов risk management со стадиями жизненного цикла.
- В 42001 рекомендуется для clause 6.1 и 8.2.

### ISO/IEC 42005:2025 — AI System Impact Assessment

- 39 страниц. Опубликован ISO/IEC в 2025 (источники называют апрель–май 2025).
- **Первый международный стандарт, посвящённый AISIA.**
- 10-шаговый процесс: определение scope → роли и ответственность → пороги → выполнение → анализ → документирование → надзор → мониторинг → интеграция в AIMS → обновление.
- **Annex A** — сопоставление с ISO/IEC 42001 (Clause 6.1.4, 8.4, Annex A.5, Annex B.5).
- **Annex B** — связь с ISO/IEC 23894.
- **Annex C** — таксономия потенциальных вреда и пользы, шаблоны.
- Гармонизируется с Canada AIA и функциями NIST AI RMF.
- Может использоваться как «due diligence evidence» для **EU AI Act Article 27 (FRIA)**.

Подробный гайд по 42005 — в [`iso-42005-impact-assessment-guide.md`](./iso-42005-impact-assessment-guide.md).

### ISO/IEC 42006:2025 — Требования к CBs для AIMS

- Опубликован ISO/IEC **7 июля 2025** (издание BS ISO/IEC 42006:2025, ISBN 978 0 539 26262 9, датировано 31 июля 2025).
- Аналог ISO/IEC 27006 (для CBs по 27001), но для AIMS.
- Дополняет ISO/IEC 17021-1 требованиями: компетенции аудиторов, покрытие всех контролей Annex A, критерии решения о сертификации, поддержание сертификации.
- **До выхода 42006 рынок 42001-сертификации работал без единого аккредитационного стандарта.** Microsoft, Synthesia и др. прошли сертификацию в 2024 без 42006.
- 42006 устраняет разрыв, повышая доверие к сертификатам.

### ISO/IEC 5338:2023 — AI system life cycle processes

- Опубликован декабрь 2023.
- Описывает 30+ процессов жизненного цикла AI-системы (требования, разработка, V&V, операции, retirement).
- Соответствует ISO/IEC/IEEE 15288 (system life cycle).
- В 42001 — информативная ссылка (bibliography).

---

## 3. Прочие связанные стандарты

| Стандарт | Назначение | Статус | Год |
|----------|-------------|---------|------|
| **ISO/IEC TR 24028:2020** | Overview of trustworthiness in AI | Published (TR) | 2020 |
| **ISO/IEC TR 24029-1:2021** | Robustness of neural networks — Part 1: Overview | Published (TR) | 2021 |
| **ISO/IEC 24029-2:2023** | Part 2: Formal methods | Published | 2023 |
| **ISO/IEC 5339:2024** | Guidance for AI applications | Published | 2024 |
| **ISO/IEC 5259-1...5:2024–2025** | Data quality for analytics and ML | Various | 2024–2025 |
| **ISO/IEC 12792** | Transparency taxonomy | Published | 2025 |
| **ISO/IEC TS 6254** | Methods of explainability | Published (TS) | 2025 |
| **ISO/IEC TR 20226** | Environmental sustainability | Published (TR) | 2025 |
| **ISO/IEC 42007** | Conformity assessment schemes | In development | 2026 ожидается |

### Стандарты Trustworthiness (через WG 3)

ISO/IEC TR 24028:2020 определяет **trustworthiness** как «способность удовлетворять ожидания заинтересованных сторон проверяемым образом» и перечисляет свойства: reliability, robustness, safety, security, privacy, transparency, fairness, accountability.

ISO/IEC TR 24029-1/2 — методы оценки робастности нейронных сетей: статистические, формальные и эмпирические.

---

## 4. Нормативный статус ссылок в 42001

| Стандарт | Статус в 42001 |
|----------|----------------|
| ISO/IEC 22989:2022 | Нормативная ссылка (раздел 2) |
| ISO/IEC 23053:2022 | Bibliography (информативная) |
| ISO/IEC 23894:2023 | Bibliography (информативная) |
| ISO/IEC TR 24028:2020 | Bibliography (информативная) |
| ISO/IEC TR 24029-1:2021 | Bibliography (информативная) |
| ISO/IEC 24029-2:2023 | Bibliography (информативная) |
| ISO/IEC 5338:2023 | Bibliography (информативная) |
| ISO/IEC 5339:2024 | Bibliography (информативная) |
| ISO/IEC 42005:2025 | Не в bibliography (вышел после 42001), но 42005 сам ссылается на 42001 |
| ISO/IEC 42006:2025 | Не в bibliography; 42006 ссылается на 42001 |

**Только 22989 обязателен.** Все остальные — рекомендуются, но не обязательны для сертификации. На практике аудиторы ожидают, что вы используете 23894 (риски) и 42005 (impact assessment) как методологическую базу.

---

## 5. Что появилось в 2025

2025 стал инфлекционной точкой для семейства:

- **ISO/IEC 42005:2025** — AI System Impact Assessment (май/июнь).
- **ISO/IEC 42006:2025** — Требования к CBs (31 июля).
- **ISO/IEC 12792** — Transparency taxonomy.
- **ISO/IEC TS 6254** — Methods of explainability.
- **ISO/IEC TR 20226** — Environmental sustainability.
- **ISO/IEC 42007** (в разработке) — Conformity assessment schemes.

Все они дополняют ISO/IEC 42001, не заменяют его. Через 12–18 месяцев ожидается, что часть из них будет включена в обновлённую bibliography 42001 при следующей системной ревизии (по плану — 2028).

---

## Дальше читать

- [Структура ISO/IEC 42001](./structure.md)
- [Глоссарий](./glossary.md)
- [ISO 42005 Impact Assessment guide](./iso-42005-impact-assessment-guide.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)

---

*Источники: ISO/IEC JTC 1/SC 42 каталог стандартов; ISO/IEC 22989:2022 (документ 74296); ISO/IEC 23053:2022 (74438); ISO/IEC 23894:2023 (77304); ISO/IEC 42005:2025; ISO/IEC 42006:2025 / BS ISO/IEC 42006:2025; ISO/IEC TR 24028:2020; ISO/IEC TR 24029-1:2021; ISO/IEC 24029-2:2023; ISO/IEC 5338:2023; ISO/IEC 5339:2024; ISO/IEC 12792; ISO/IEC TS 6254; ISO/IEC TR 20226; BSI Knowledge; digital.nemko; ITEH; ISMS.online; risk3sixty; KPMG; Oxebridge; CMS Law-Now; Scrut; Prompt Security; libertify; INCITS; AI Standards Hub; verifywise.ai; SAP Community; ANAB.*
