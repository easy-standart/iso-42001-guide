# Integrated Management System: ISO/IEC 42001 + 27001 + 9001 + другие

> 🇬🇧 [Read in English](../integrated-management-system.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** Annex D ISO/IEC 42001 даёт прямой mapping на ISO 9001 (качество), ISO/IEC 27001 (ИБ), ISO 31000 (риски), ISO 37301 (compliance). Это основа для Integrated Management System (IMS) — единого процессного фундамента с раздельными политиками верхнего уровня и SoA. IMS даёт 30–50 % сокращение нагрузки compliance-команды и 30–50 % экономию на combined audits.

---

## Содержание

- [1. Что такое IMS](#1-что-такое-ims)
- [2. Annex D 42001: mapping](#2-annex-d-42001-mapping)
- [3. Архитектура IMS для AI-компании](#3-архитектура-ims-для-ai-компании)
- [4. Что объединять, что разделять](#4-что-объединять-что-разделять)
- [5. Combined audits](#5-combined-audits)
- [6. Кейсы](#6-кейсы)

---

## 1. Что такое IMS

Integrated Management System — это **внутренняя организация процессов**, не отдельный сертификат. Идея: общий процессный фундамент, на котором надстраиваются специфические требования каждого стандарта.

IMS работает потому, что все современные ISO management standards построены на Annex SL High-Level Structure: одинаковые clauses 4–10, одинаковые понятия (риск, контекст, заинтересованные стороны, документированная информация, корректирующие действия).

Стандарты, которые объединяются в IMS чаще всего:
- ISO 9001 — качество
- ISO/IEC 27001 — информационная безопасность
- ISO/IEC 27701 — приватность
- ISO 14001 — экология
- ISO 22301 — непрерывность бизнеса
- ISO 13485 — медицинские изделия
- ISO 37301 — compliance
- ISO/IEC 42001 — ИИ
- ISO 45001 — охрана труда

---

## 2. Annex D 42001: mapping

Annex D (информативное приложение к ISO/IEC 42001:2023) показывает прямые соответствия между 42001 и:

- **ISO 9001:2015** — общая структура clauses 4–10, концепции «контекст», «лидерство», «риск-based мышление».
- **ISO/IEC 27001:2022** — Annex SL, риск-менеджмент, SoA, internal audit, management review. Около 40 % требований пересекаются.
- **ISO 31000:2018** — методология управления рисками. ISO/IEC 23894 (AI risk) построен на 31000.
- **ISO 37301:2021** — управление compliance, отчётность перед регуляторами.

Annex D **не нормативное** — оно даёт рекомендации, не требования.

---

## 3. Архитектура IMS для AI-компании

Типовая архитектура IMS для SaaS, держащего 27001 + 42001 + 27701:

```
                    ┌────────────────────────────────┐
                    │   Management Board / CEO       │
                    │   (общее лидерство Clause 5)   │
                    └──────────────┬─────────────────┘
                                   │
        ┌──────────────────────────┼──────────────────────────┐
        │                          │                          │
┌───────▼────────┐        ┌────────▼────────┐        ┌───────▼────────┐
│  CISO / AIMS   │        │     CPO/DPO     │        │  Head of QMS   │
│     Lead       │        │                 │        │                │
└───────┬────────┘        └────────┬────────┘        └───────┬────────┘
        │                          │                          │
   27001 SoA                  27701 SoA                 9001 controls
   42001 SoA                  GDPR DPIA                  
                                                              
        ┌─────────────────────────────────────────────────────┐
        │       Общие процессы (на одной HLS):                │
        │  • Контекст и заинтересованные стороны (Cl. 4)      │
        │  • Document control (Cl. 7.5)                       │
        │  • Internal audit (Cl. 9.2)                         │
        │  • Management review (Cl. 9.3)                      │
        │  • Nonconformity & corrective action (Cl. 10.1)     │
        │  • Risk management methodology                      │
        │  • Supplier management                              │
        │  • Awareness & training                             │
        │  • Communication                                    │
        │  • Change management                                │
        └─────────────────────────────────────────────────────┘
```

---

## 4. Что объединять, что разделять

### Объединить (один процесс на все стандарты)

- **Document control** — общая политика, общий шаблон, единое версионирование.
- **Internal audit program** — одна программа, одна команда, разные критерии в чек-листах.
- **Management review** — одно заседание, повестка с блоками по каждому стандарту.
- **Nonconformity и corrective action** — общий процесс, единый tracker.
- **Risk management methodology** — общие шкалы, общий формат регистра. Объекты риска и категории — разные.
- **Supplier management** — общий процесс due diligence. Чек-листы для AI-вендоров (A.10.3) специфичны.
- **Training & awareness** — общий LMS, разные курсы.
- **Communication** — общие каналы.

### Разделить (отдельно для каждого стандарта)

- **Политики верхнего уровня** — Information Security Policy, AI Policy, Privacy Policy, Quality Policy.
- **Statement of Applicability** — отдельный SoA для каждого стандарта (можно в одном файле с тэгами).
- **Объекты учёта** — информационные активы, AI-системы, обработки персональных данных.
- **Метрики и KPI** — специфика каждого стандарта.

### Гибрид

- **Risk register** — общий файл с категориями: information / AI / privacy / quality. Каждая запись помечена применимыми стандартами.

---

## 5. Combined audits

CB могут проводить combined audit для нескольких стандартов одновременно. Условия:

- Один CB, аккредитованный по всем стандартам в scope.
- Один scope statement.
- Combined SoA с тэгами.
- Один risk register.

**Экономия:**
- 27001 + 42001 combined: 30–50 % vs два отдельных аудита.
- 27001 + 27701 + 42001 combined: 40–60 %.
- 9001 + 27001 + 42001 combined: 40–55 %.

**CBs, активные в combined:**
- **BSI** — все ISO standards, в т.ч. 27001 + 42001 + 27701 одним audit-engagement.
- **Schellman** — 27001 + 42001, SOC 2 + 27001, SOC 2 + 42001.
- **A-LIGN** — аналогично.
- **DNV** — особенно силён в 9001 + 14001 + 45001 IMS-аудитах.
- **TÜV Nord/Rheinland** — IMS для производственных компаний.

---

## 6. Кейсы

**Microsoft 365 Copilot** — combined 27001 + 27701 + 42001 SoA в одном engagement (Mastermind / IAS, март 2025).

**Workday** — 27001 + 27701 + 42001 в одной IMS-структуре. 12 продуктовых линий в одном scope, выдан один сертификат 42001 в дополнение к существующим (Schellman, 2025).

**Anthropic** — 27001 + 27701 + 27017 + 27018 + SOC 2 + ISO 42001. Combined audit cycle, Schellman (январь 2025).

**IBM** — 27001 + 27017 + 27018 + 27701 + 42001. «Зрелый IMS» был причиной, по которой 42001-аудит занял 3 месяца (kickoff → certification).

---

## Преимущества IMS в цифрах

По данным DQS и ISMS.online:

- **30–50 % сокращение** нагрузки compliance-команды.
- **30–50 % экономия** на CB-fees при combined audit.
- **40–60 % быстрее** time-to-certification для второго и последующих стандартов.
- **20–40 % меньше документов** благодаря объединённой документации.

---

## Нужна помощь с построением IMS?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу compliance-карту и предложим архитектуру IMS, минимизирующую дублирование.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Структура ISO/IEC 42001](./structure.md)
- [Сравнение с ISO 27001](./comparison-iso-27001.md)
- [Семейство стандартов ISO/IEC AI](./family-of-standards.md)
- [Стоимость и сроки](./cost-timeline.md)

---

*Источники: ISO/IEC 42001:2023 Annex D; Annex SL ISO/IEC Directives Part 1; ISO 9001:2015; ISO/IEC 27001:2022; ISO/IEC 27701:2019; ISO 31000:2018; ISO 37301:2021; ISO 22301; ISO 13485; ISO 14001; ISO 45001; DQS Integrated Management System Practice; ISMS.online; BSI Combined Audit Guide; Schellman; A-LIGN; DNV; TÜV; Microsoft Trust Center; Anthropic Privacy Center; Workday Trust; IBM Think.*
