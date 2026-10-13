# ISO/IEC 42001 ↔ NIST AI RMF, Colorado AI Act и законы штатов США

> 🇬🇧 [Read in English](../comparison-nist-ai-rmf.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** NIST AI RMF 1.0 — официальный фреймворк США, добровольный, но де-факто обязательный для федеральных подрядчиков. На сайте NIST размещён **кросс-маппинг, поданный сообществом** (опубликован NIST, но написан не им): он сопоставляет 72 подкатегории AI RMF с клаузулами и Annex B ISO/IEC 42001. Структура «Govern / Map / Measure / Manage» ложится почти 1:1 на clauses 4–10 и Annex A. Colorado AI Act (SB 24-205) ссылался на ISO/IEC 42001 как на основание для affirmative defense, но был отменён и заменён на SB 26-189 (в силе с 1 января 2027), где этой ссылки уже нет; ещё несколько законопроектов штатов с упоминанием ISO/IEC 42001 не прошли.

---

## Содержание

- [1. NIST AI RMF — структура](#1-nist-ai-rmf--структура)
- [2. Кросс-маппинг NIST → ISO 42001](#2-кросс-маппинг-nist--iso-42001)
- [3. Статус NIST под администрацией Трампа](#3-статус-nist-под-администрацией-трампа)
- [4. Colorado AI Act (SB 24-205 → SB 26-189)](#4-colorado-ai-act-sb-24-205--sb-26-189)
- [5. Texas TRAIGA, Virginia, Utah, Illinois, NYC, California, Connecticut](#5-texas-traiga-virginia-utah-illinois-nyc-california-connecticut)
- [6. Консолидированный подход](#6-консолидированный-подход)

---

## 1. NIST AI RMF — структура

NIST AI Risk Management Framework 1.0 был опубликован 26 января 2023 года. Это **добровольный** фреймворк, но он де-факто стал стандартом для:
- федеральных подрядчиков США,
- enforcement-guidance FTC, CFPB, FDA, SEC, EEOC,
- референса в законах штатов (Colorado, Texas, Virginia).

Четыре функции:

- **GOVERN** (6 категорий) — политики, процедуры, роли, управление рисками жизненного цикла.
- **MAP** (5 категорий) — контекст, классификация AI use-cases, стейкхолдеры.
- **MEASURE** (4 категории) — анализ, мониторинг, оценки доверенности.
- **MANAGE** (4 категории) — приоритизация, реагирование, третьи стороны, документирование.

В дополнение — **Playbook, Roadmap, Perspectives, Generative AI Profile (NIST AI 600-1)** и **Cyber AI Profile (NIST IR 8596)**.

---

## 2. Кросс-маппинг NIST → ISO 42001

NIST ведёт публичную страницу «Crosswalks to the NIST AI RMF», где размещён **кросс-маппинг, поданный сообществом, «NIST AI RMF → ISO/IEC FDIS 42001 AI Management System Crosswalk»**. Он сопоставляет 72 подкатегории AI RMF с клаузулами и контролями Annex B ISO 42001. Документ опубликован на сайте NIST, но подготовлен сообществом, а не самим NIST.

Выдержка (полный документ на сайте NIST AIRC):

| NIST AI RMF подкатегория | Содержание | ISO/IEC 42001 клаузула / контроль |
|---|---|---|
| GOVERN 1.1 | Юр./регул. требования; соответствующие ценности | Кл. 4.1, 4.2; A.2.2, A.2.3 |
| GOVERN 1.2 | Trustworthy AI характеристики в политиках | Кл. 5.2; A.2.2–A.2.4 |
| GOVERN 1.3 | Процессы приоритизации AI-рисков | Кл. 6.1.2, 6.1.3; A.5.2–A.5.5 |
| GOVERN 1.4 | Процессы мониторинга рисков документированы и ресурсированы | Кл. 9.1; A.6.2.6 |
| GOVERN 1.5 | Процессы переоценки рисков | Кл. 9.1, 10.2 |
| GOVERN 1.6 | Инвентарь AI-систем | B.4.2, B.4.3, B.4.4, B.4.5, B.4.6 |
| GOVERN 1.7 | Процедуры decommissioning | B.6.2.6 |
| GOVERN 2.1 | Роли и линии коммуникации | Кл. 9.1; A.3.2 |
| GOVERN 2.2 | AI literacy и обучение | Кл. 7.2, 7.3 |
| GOVERN 2.3 | Управление исполнительное — подотчётность | Кл. 5.1, 5.3 |
| GOVERN 3.1 | Diversity/equity/accessibility в командах | A.3.2, B.3.2 |
| GOVERN 4.x | Культура, безопасность, тестирование | Кл. 7.4; A.2.3 |
| GOVERN 5.x | Вовлечение стейкхолдеров | A.8.2, A.8.3 |
| GOVERN 6.x | Третьи стороны | A.10.2–A.10.4 |
| MAP 1.x | Контекст, категоризация, намерения | Кл. 4.1–4.4; A.5.2, A.6.1.2 |
| MAP 2.x | Задачи и методы ИИ | A.6.2.2 |
| MAP 3.x | Выгоды и вред | A.5.3, A.5.4, A.5.5 |
| MAP 4.x | Риски третьих сторон | A.10.2, A.10.3 |
| MAP 5.x | Влияние на индивидов/группы | A.5.2–A.5.5 |
| MEASURE 1.x | Подход к метрикам | Кл. 9.1, A.6.2.4 |
| MEASURE 2.x | Trustworthy характеристики измеряются | Кл. 9.1, A.6.2.4 |
| MEASURE 3.x | Отслеживание выявленных рисков | Кл. 9.1, A.6.2.6 |
| MEASURE 4.x | Обратная связь | A.3.3 |
| MANAGE 1.x | Приоритизация и реагирование | Кл. 6.1.3, 8.2 |
| MANAGE 2.x | Максимизация выгоды / минимизация вреда | A.9.2–A.9.4 |
| MANAGE 3.x | Риски от третьих сторон | A.10.2–A.10.4 |
| MANAGE 4.x | Документирование и коммуникация risk treatments | Кл. 7.5, 10.1 |

**Агрегированный вывод:**

- **GOVERN** ≈ clauses 4–6 + большая часть Annex A.
- **MAP** ≈ clauses 6.1.2 + 6.1.4 + A.5.
- **MEASURE** ≈ clause 9 + A.6.2.4.
- **MANAGE** ≈ clauses 8.2 + 10 + A.9.

---

## 3. Статус NIST под администрацией Трампа

AI RMF 1.0 по-прежнему действует — NIST не выпустил «AI RMF 2.0».

Ключевые события 2025–2026:

- **20 января 2025** — Трамп отменил Executive Order 14110 Байдена (Safe, Secure, and Trustworthy AI).
- **23 января 2025** — подписан EO 14179 «Removing Barriers to American Leadership in AI».
- **23 июля 2025** — AI Action Plan «Winning the Race» + три EO. План предписывает NIST «ревизовать AI RMF с удалением ссылок на misinformation, DEI и climate change». Сам NIST AI RMF остаётся добровольным.
- **11 декабря 2025** — EO «Ensuring a National Policy Framework for AI», нацеленный на preemption законов штатов (кроме child safety, инфраструктуры, госзакупок).
- **Generative AI Profile (NIST AI 600-1)** — опубликован 26 июля 2024, остаётся актуальным. Мартовское обновление 2025 — provenance, supply-chain, третьи стороны.
- **Cyber AI Profile (NIST IR 8596)** — preliminary draft 16 декабря 2025; initial public draft в 2026.
- **7 апреля 2026** — NIST опубликовал concept note для AI RMF Profile on Trustworthy AI in Critical Infrastructure.
- **NIST SP 800-53 Release 5.2.0** (август 2025) — обновления под EO 14306, дополняющие AI RMF.

**Практическое следствие:** NIST AI RMF остаётся де-факто стандартом для федеральных подрядчиков США. Текст может быть пересмотрен для удаления DEI-формулировок, но фреймворк-структура Govern/Map/Measure/Manage сохранится.

---

## 4. Colorado AI Act (SB 24-205 → SB 26-189)

- Исходный закон, SB 24-205, подписан губернатором Полисом 17 мая 2024, эффективная дата — 1 февраля 2026.
- Эту дату сдвинули на 30 июня 2026 (SB 25B-004, август 2025), а затем **SB 24-205 отменили и заменили на SB 26-189** (подписан в мае 2026, в силе с 1 января 2027). Исходный закон так и не вступил в силу.
- Применяется к developers и deployers high-risk AI systems, влияющим на consequential decisions в занятости, образовании, финансах, здравоохранении, жилье, страховании, юр. услугах, госуслугах.

**Прямые ссылки на ISO 42001 и NIST AI RMF (исторически — из исходного SB 24-205; в закон-замену SB 26-189 не перенесены, поэтому ISO/IEC 42001 больше не является кодифицированной защитой в Colorado):**

> Affirmative defense / rebuttable presumption: deployer/developer получает affirmative defense в действиях Генерального прокурора, если:
> 1. обнаружил и устранил нарушение через обратную связь, adversarial testing / red teaming, внутренний ревью, И
> 2. в целом соответствует «latest version of the NIST AI Risk Management Framework, Standard ISO/IEC 42001, или другому национально/международно признанному framework, если тот substantially equivalent или более строгий», или
> 3. любому framework, который Attorney General может обозначить.

**Дополнительные требования (по исходному SB 24-205):**
- Impact assessment — минимум ежегодно и в 90 дней после substantial modification, retention 3 года.
- Уведомление Attorney General в течение 90 дней после обнаружения алгоритмической дискриминации.
- Enforcement — только Attorney General; нет private right of action.
- Штрафы — до $20,000 за нарушение по Colorado Consumer Protection Act.

---

## 5. Texas TRAIGA, Virginia, Utah, Illinois, NYC, California, Connecticut

### Texas TRAIGA (HB 149)
Подписан Abbott 22 июня 2025, эффективная дата 1 января 2026. Intent-based liability (disparate impact не достаточен). **Safe harbor: substantial compliance с NIST AI RMF или Generative AI Profile** (прямой ссылки на ISO 42001 нет). Штрафы $10,000–$200,000. 36-месячный regulatory sandbox.

### Virginia HB 2094 (High-Risk AI Developer and Deployer Act)
Принят Assembly в феврале 2025, **ветирован губернатором Янгкиным 24 марта 2025**. Содержал явную ссылку на NIST AI RMF или ISO/IEC 42001 как основание для презумпции соответствия. Virginia Executive Order No. 30 (2024) остаётся базовым режимом для госагентств.

### Utah AI Policy Act (SB 149)
В силе с 1 мая 2024. 7 мая 2025 — поправки (SB 226, SB 332, HB 452, SB 271). Sunset продлён до 1 июля 2027. Фокус: GenAI-прозрачность, регулируемые профессии, mental health chatbots, deepfake. Safe harbor: GenAI должна сама disclose non-human природу. Прямых ссылок на NIST/ISO нет.

### Illinois HB 3773
Поправка к Illinois Human Rights Act. Подписан 9 августа 2024, в силе с 1 января 2026. Запрещает использовать ИИ для дискриминации защищённых классов; запрещает ZIP-коды как прокси; обязательные уведомления сотрудников и кандидатов. Действует более старый Illinois AI Video Interview Act (с января 2020).

### New York City Local Law 144 (AEDT Law)
В силе с 5 июля 2023. Ежегодный bias audit независимым аудитором; публикация summary на сайте; уведомление кандидатов минимум за 10 рабочих дней. Штрафы $500–$1,500 за день. В декабре 2025 NY State Comptroller раскритиковал DCWP за неэффективность (только 2 жалобы, 32 проверенные компании).

### California
- SB 1047 — ветирован сентябрь 2024.
- **AB 2013** (GenAI Training Data Transparency Act) — с 1 января 2026.
- **SB 942** (AI Transparency Act) — дата применения перенесена с 1 января 2026 на 2 августа 2026 поправками AB 853 (13 октября 2025) — выравнивание с EU AI Act.
- **SB 53** (Transparency in Frontier AI Act, TFAIA) — с 1 января 2026.
- AB 489, SB 243, AB 325 — с 1 января 2026.
- AB 2930 (Automated Decision Tools) — не принят.

### Connecticut SB 2
Не принят в 2024 и 2025 из-за оппозиции губернатора Ламонта. Закон в редакции 2025 уже был ослаблен. Предполагалась аффирмативная защита через соответствие NIST AI RMF / ISO 42001.

**Общий контекст:** в 2024 в штатах предложено >635 ИИ-биллов, принято ~100. К середине 2025 — >921. Федеральный EO от 11 декабря 2025 нацелен на preemption этих законов, но patchwork сохраняется.

---

## 6. Консолидированный подход

Для организаций, работающих в нескольких юрисдикциях (ЕС, США, Азия), наиболее устойчивая фундаментальная модель:

1. **ISO/IEC 42001:2023** как ядро — даёт международно признанный сертификат и, по распространённым оценкам консультантов, закрывает примерно 40–50 % EU AI Act и 70 %+ NIST AI RMF (это оценки, а не цифры регулятора).
2. **NIST AI RMF** как референс для США. Используется существующий кросс-маппинг от NIST.
3. **EN 18286:2026** (когда процитирован в OJ) — для presumption of conformity по AI Act.
4. **Отдельные надстройки** — GPAI Code of Practice, Singapore AI Verify, China labelling measures — по мере применимости.

Главная экономия: по распространённым оценкам консультантов, документы и процессы AIMS могут переиспользоваться примерно на 70–90 % между этими режимами. Главные различия — в форме отчётности, маркировки и регистрации.

---

## Нужна помощь с consolidated AI governance стратегией?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу карту юрисдикций и подберём минимальный, но достаточный комплект документов.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Сравнение с EU AI Act](./comparison-eu-ai-act.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [Обзор стандарта](./overview.md)

---

*Источники: NIST AI RMF 1.0; NIST AI RMF → ISO/IEC FDIS 42001 Crosswalk (AIRC PDF); NIST AI 600-1 Generative AI Profile; NIST IR 8596 Cyber AI Profile draft; Colorado SB 24-205 (NAAG Deep Dive; Davis Wright Tremaine; Gibson Dunn; Schellman/RockCyber; FPF); Texas TRAIGA (Baker Botts; K&L Gates; Latham & Watkins); Virginia HB 2094 (Ogletree; ABA Health Law; Saul Ewing); Utah SB 149 (Manatt; Perkins Coie); Illinois HB 3773 (Seyfarth Shaw; Morgan Lewis; Ogletree); NYC Local Law 144 (NYC DCWP; Deloitte; FairNow; NY State Comptroller Dec 2025); California AB 2013, SB 942, SB 53 (TrustArc; Cooley; Troutman Privacy; King & Spalding); Connecticut SB 2 (LegiScan; FPF; CT Mirror); EO 14110, 14179; AI Action Plan 23.07.2025; EO 11.12.2025.*
