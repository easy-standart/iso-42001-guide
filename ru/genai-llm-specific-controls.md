# ISO/IEC 42001 для GenAI и LLM-проектов

> 🇬🇧 [Read in English](../genai-llm-specific-controls.md) · ⬅ [На главную](./overview.md) · 📖 [Обзор стандарта](./overview.md)

> **TL;DR.** Проекты на базе GenAI и LLM API (OpenAI, Anthropic, Google, Mistral) не вписываются в классическую логику «обучили модель — следим за дрифтом». Их специфика — prompt injection, hallucination, утечка данных через провайдера, copyright, jailbreak. Из 38 контролей Annex A мы считаем **наиболее релевантными 14** (наша оценка, не классификация ISO). Этот гайд показывает, как именно их применять к LLM-проектам.

---

## Содержание

- [1. Чем GenAI/LLM отличается с точки зрения 42001](#1-чем-genaillm-отличается-с-точки-зрения-42001)
- [2. 14 критичных контролей: что в фокусе](#2-14-критичных-контролей-что-в-фокусе)
- [3. A.4 Реестр: как описывать API-модели](#3-a4-реестр-как-описывать-api-модели)
- [4. A.5 Impact Assessment: специфика LLM](#4-a5-impact-assessment-специфика-llm)
- [5. A.6 Lifecycle: prompt engineering, RAG, fine-tuning](#5-a6-lifecycle-prompt-engineering-rag-fine-tuning)
- [6. A.7 Данные: RAG, embeddings, корпоративные документы](#6-a7-данные-rag-embeddings-корпоративные-документы)
- [7. A.8 Информирование: что писать пользователям](#7-a8-информирование-что-писать-пользователям)
- [8. A.10 Вендоры: что требовать у OpenAI, Anthropic, Google](#8-a10-вендоры-что-требовать-у-openai-anthropic-google)
- [9. Чеклист GenAI-готовности](#9-чеклист-genai-готовности)

---

## 1. Чем GenAI/LLM отличается с точки зрения 42001

Классические ML-системы (например, кредитный скоринг) хорошо ложатся на 42001 «как есть»: вы обучаете модель на размеченных данных, валидируете, разворачиваете, мониторите drift.

LLM-проекты ломают эту логику в нескольких точках:

| Аспект | Классический ML | LLM на API |
|--------|------------------|------------|
| «Обучение» | Тренировка на ваших данных | Вы не обучаете базовую модель |
| Контроль над моделью | Полный | Минимальный — модель может измениться без вашего ведома |
| Drift | Внутри вашего распределения данных | Внешний — провайдер обновил модель |
| Данные | Под вашим контролем | Может уходить провайдеру (зависит от тарифа) |
| Воспроизводимость | Высокая | Низкая — даже temperature=0 не гарантирует identity |
| Объяснимость | Возможна (SHAP, LIME) | Практически невозможна для базовой модели |
| Атаки | Adversarial examples | Prompt injection, jailbreak |

Эти отличия требуют переосмысления контролей Annex A для GenAI-проектов.

---

## 2. 14 критичных контролей: что в фокусе

Из 38 контролей Annex A особенно важны для LLM:

| Контроль | Почему критичен для LLM |
|----------|-------------------------|
| **A.2.2** AI Policy | Должна включать правила использования внешних LLM |
| **A.4.2** Реестр ресурсов | API-модели часто не учитываются |
| **A.4.3** Данные | RAG-датасеты и embedding stores — отдельная тема |
| **A.5.2** Impact Assessment | Hallucinations и misuse — специфика LLM |
| **A.5.4** Воздействие на людей | Кому покажем неверный ответ |
| **A.6.2.2** Спецификация | Что разрешено генерировать, что нет |
| **A.6.2.4** Верификация | Eval-сеты для LLM — особая методология |
| **A.6.2.6** Мониторинг | Не drift, а deviation от ожидаемого поведения |
| **A.6.2.7** Документация | Prompt templates как часть документации |
| **A.6.2.8** Логирование | Полные prompts + responses + token usage |
| **A.7.3** Сбор данных | Что попадает в context window |
| **A.8.2** Информирование пользователей | Дисклеймеры про hallucinations |
| **A.10.3** Поставщики | OpenAI, Anthropic, Google — это критичный supplier |
| **A.10.4** Клиенты | Передача LLM-функции своим клиентам |

---

## 3. A.4 Реестр: как описывать API-модели

Типичная ошибка Stage 2: «модель GPT-4 в реестре есть, но это не модель, а API». Аудиторы хотят видеть конкретику.

**Минимум полей для API-модели в реестре:**

- **Provider:** OpenAI / Anthropic / Google / Mistral / другой.
- **Endpoint:** конкретное API (`gpt-4-turbo-2024-04-09`, `claude-3-5-sonnet-20241022`).
- **Версия и pinning:** используете latest или зафиксированную версию?
- **Use case:** для чего используется (RAG-ответы, классификация, summarization).
- **Data flow:** какие данные уходят в API, остаются ли у провайдера.
- **Tariff/SLA:** free vs Enterprise tier (важно — на free-тарифе данные могут использоваться для обучения).
- **Fallback:** что происходит при недоступности API.
- **Владелец:** кто отвечает в команде.
- **Дата последнего review:** обычно ежеквартально.

Реестр обновляется при каждой смене модели — это event для AIMS-логирования.

---

## 4. A.5 Impact Assessment: специфика LLM

В AISIA для LLM-проекта должны быть отдельно отражены:

**Foreseeable misuse:**
- Пользователи воспринимают ответ как авторитетный источник, не как «вероятностную гипотезу».
- Запрос данных, которых не должно быть в context window (jailbreak).
- Использование LLM-ответа в высокорисковых решениях (медицина, право) без human review.

**Hallucinations:**
- Какова частота hallucinations на ваших eval-сетах.
- Какие категории hallucinations критичны (выдуманные фамилии, цифры, цитаты, законы).
- Меры снижения: RAG с цитированием, structured output, human-in-the-loop.

**Bias и fairness:**
- LLM наследует bias обучающих данных провайдера — у вас нет доступа.
- Что вы можете проверить: bias-аудит на ваших use cases с representative samples.

**Privacy:**
- Что отправляется в prompt (включая system prompt).
- Что попадает в логи провайдера.
- Связь с GDPR: ваши prompts могут содержать персональные данные клиентов.

---

## 5. A.6 Lifecycle: prompt engineering, RAG, fine-tuning

42001 написан под классический ML-lifecycle. Для LLM нужно мэппить:

| Этап 42001 (A.6) | Что это для LLM |
|------------------|------------------|
| Цели проектирования (A.6.1.1) | Use case, входы, выходы, ограничения |
| Цели «ответственной разработки» (A.6.1.2) | Hallucination policy, refusal policy, transparency |
| Спецификация (A.6.2.2) | Prompt templates, structured output schemas, refusal cases |
| Документирование (A.6.2.3) | Версионирование prompts, RAG-конфигов, retrieval pipelines |
| Верификация и валидация (A.6.2.4) | Eval-сеты (точность, hallucination rate, refusal accuracy) |
| Развёртывание (A.6.2.5) | Canary releases для новых prompts, A/B testing |
| Эксплуатация и мониторинг (A.6.2.6) | Token usage, response quality drift, user complaints |
| Техническая документация (A.6.2.7) | Model card + prompt library + RAG architecture |
| Журналы (A.6.2.8) | Полный prompt + response + metadata (с учётом приватности) |

**Prompt engineering как часть AIMS:** каждая значимая версия prompt template должна быть commit'ом в репозитории, с тестами и changelog. Аудитор может попросить продемонстрировать, как изменения prompts проходят review.

---

## 6. A.7 Данные: RAG, embeddings, корпоративные документы

RAG (Retrieval-Augmented Generation) — особый случай. Стандарт требует прозрачности по данным, но в RAG-контурах данные приходят из разных источников.

**Что должно быть в data documentation:**

- **Источники retrieval:** конкретные репозитории, базы знаний, документы. Правовые основания использования.
- **Embedding store:** какие embeddings, кто их генерирует, как часто обновляется.
- **Chunking strategy:** как документы разрезаются на чанки. Это влияет на качество ответов.
- **Retrieval pipeline:** какой retriever (BM25, vector search, hybrid), какие фильтры, какой re-ranking.
- **Контекстное окно:** какой максимум, что отрезается при overflow.
- **Цитирование:** возвращает ли система ссылку на источник.
- **Доступы:** кто может читать, кто может изменять embeddings.

**Корпоративные документы:** если RAG использует внутренние документы, AIMS должна охватывать процесс синхронизации. Удалённый из основной системы документ должен удаляться из embedding store. Иначе LLM продолжает «знать» то, чего быть не должно.

---

## 7. A.8 Информирование: что писать пользователям

Контроль A.8.2 требует, чтобы пользователи понимали ограничения системы. Для LLM это **disclaimer**, который должен:

- Чётко указывать, что используется GenAI.
- Предупреждать о возможности hallucinations.
- Указывать, что система не заменяет профессиональную консультацию (для медицины/права/финансов).
- Описывать, какие данные собираются и куда уходят.
- Давать канал обратной связи для сообщения об ошибках.
- Для high-risk сценариев — указывать право на human review.

**Антипаттерн:** «Powered by AI» внизу страницы мелким шрифтом. Аудитор это сочтёт недостаточным.

---

## 8. A.10 Вендоры: что требовать у OpenAI, Anthropic, Google

Контроль A.10.3 в случае LLM проектов — критичен. Что должно быть на руках:

| Документ | Где взять |
|----------|-----------|
| Data Processing Agreement (DPA) | Обычно отдельный документ к Enterprise-контракту |
| Описание data handling (training opt-out) | Privacy Policy, Trust Center провайдера |
| Сертификаты compliance провайдера (ISO 27001, ISO 42001, SOC 2) | Trust Center |
| SLA по uptime и доступу к логам | Enterprise contract |
| Условия subprocessors (например, AWS как hosting для Anthropic) | DPA addendum |
| Процедура incident notification | Privacy / Security Policy |
| Условия model deprecation (когда модель будет отключена) | API documentation |

**Free и Pay-as-you-go тарифы:** данные могут использоваться для обучения. Это явный nonconformity для Sensitive Use сценариев. Для production — только Enterprise тариф с opt-out training.

**OpenAI Enterprise, Anthropic Claude Enterprise, Google Cloud Vertex AI** — у всех есть варианты с no-training гарантией. Это должно быть зафиксировано в контракте и упомянуто в supplier record.

---

## 9. Чеклист GenAI-готовности

Короткая проверка для LLM-проекта:

- [ ] Все используемые LLM API внесены в реестр (A.4) с провайдером, версией, use case, тарифом.
- [ ] Используется Enterprise tier с гарантией no-training-on-our-data (или эквивалент).
- [ ] DPA / privacy addendum с провайдером подписан и хранится.
- [ ] Prompt templates версионируются в Git, изменения проходят review.
- [ ] Eval-сеты для оценки качества и hallucination rate существуют и регулярно прогоняются.
- [ ] Логирование prompts + responses + token usage настроено, retention ≥ 90 дней.
- [ ] AISIA (по 42005) для LLM-системы проведена и утверждена.
- [ ] Пользователям отображается явный AI-disclaimer.
- [ ] Канал обратной связи для сообщения о hallucinations работает.
- [ ] Для high-risk use cases внедрён human-in-the-loop.
- [ ] Существует процедура incident response для AI-инцидентов специфичных для LLM.
- [ ] Bias-аудит на ваших use cases проводится регулярно.
- [ ] Описан fallback при недоступности API.
- [ ] Документация по RAG (если есть): источники, chunking, retrieval, embedding store.

70 % ✅ — вы готовы предъявить аудитору LLM-проект. Меньше — есть конкретный план работы.

---

## Нужна помощь с GenAI compliance?

> 📩 **Бесплатная 15-минутная консультация в Telegram**
> Разберём вашу LLM-архитектуру: какие контроли применимы, что требовать у провайдера, как организовать reasonable evidence pack для аудита.
>
> 👉 [Написать в Telegram](https://t.me/m/8NsOXRkMZmQy)

---

## Дальше читать

- [Обзор стандарта 42001](./overview.md)
- [Гайд по ISO 42005 — Impact Assessment](./iso-42005-impact-assessment-guide.md)
- [prEN 18286 vs ISO 42001](./pren-18286-vs-iso-42001.md)
- [Shadow AI Policy шаблон](./shadow-ai-policy-template.md)
---

*Источники: ISO/IEC 42001:2023 Annex A; AWS Security Blog — «AI lifecycle risk management: ISO/IEC 42001:2023 for AI governance»; LayerX Security — «ISO 42001: GenAI Governance & Compliance»; OpenAI Enterprise data handling policy; Anthropic privacy and security documentation; Google Cloud Vertex AI security overview.*
