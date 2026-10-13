# Шаблон: AI System Card

> 🇬🇧 [Read in English](../templates/ai-system-card.md) · ⬅ [На главную](../ru/README.md)

> **Что это.** Структурированный шаблон карточки AI-системы для реестра ресурсов (контроль ISO/IEC 42001 Annex A.4.2). Заполняется владельцем системы. Хранится в реестре AIMS. Аудитор запрашивает в первую очередь — это самый базовый артефакт.

> **Как использовать.** Скопируйте раздел ниже в Markdown или Google Doc / Notion для каждой AI-системы. Поля в `[квадратных скобках]` заполните своими данными. Поля с ✓ — обязательные для аудита.

---

```markdown
# AI System Card: [Название системы]

**ID карточки:** AIS-[НОМЕР]
**Версия:** 1.0
**Дата создания:** [YYYY-MM-DD]
**Дата последнего обновления:** [YYYY-MM-DD]
**Следующий review:** [YYYY-MM-DD]
**Статус:** [Production / Pilot / Development / Decommissioned]

## 1. Идентификация ✓

- **Название:** [Понятное название для бизнеса]
- **Внутренний идентификатор:** [Код в реестре]
- **Тип системы:** [Classical ML / GenAI on API / GenAI fine-tuned / Hybrid / RPA + AI]
- **Бизнес-функция:** [Маркетинг / Продажи / HR / Finance / R&D / Operations / Customer Support / etc.]
- **Назначение:** [1–2 предложения, для чего система существует]
- **Владелец системы:** [Имя, должность]
- **Технический lead:** [Имя, должность]
- **Executive sponsor:** [Имя, должность]

## 2. Архитектура и компоненты ✓

- **Базовая модель / алгоритм:** [GPT-4-turbo / Claude 3.5 Sonnet / Random Forest / Custom CNN / etc.]
- **Провайдер модели (если внешняя):** [OpenAI / Anthropic / Google / Mistral / Hugging Face / In-house]
- **Endpoint / версия:** [Конкретная версия API, например `gpt-4-turbo-2024-04-09`]
- **Pinning:** [Зафиксирована ли версия или используется `latest`]
- **Архитектурная диаграмма:** [Ссылка на диаграмму в репозитории / Confluence / Miro]
- **Frontend:** [Где пользователь взаимодействует с системой]
- **Backend / orchestration:** [Технологии: Python, FastAPI, LangChain, etc.]
- **Storage / databases:** [Какие данные где хранятся]
- **Embedding store (для RAG):** [Pinecone / Weaviate / pgvector / etc.]

## 3. Данные ✓

- **Training data:** [Источники данных для обучения, если применимо. Иначе — "Не обучаем"]
- **Inference data:** [Что подаётся на вход в production]
- **Output data:** [Что система генерирует]
- **Категории персональных данных:** [Email / имя / телефон / финансы / медицина / биометрия / none]
- **Правовое основание (GDPR):** [Consent / Contract / Legal obligation / Vital interests / Public task / Legitimate interests]
- **Регионы хранения данных:** [EU / US / Multi-region]
- **Retention данных:** [Сколько хранятся данные пользователя]
- **Data lineage:** [Ссылка на data flow diagram]

## 4. Use cases и ограничения ✓

- **Intended use:** [Для чего система предназначена]
- **Out of scope (что НЕ должно делаться):** [Список запрещённых применений]
- **Foreseeable misuse:** [Как система может быть неправомерно использована]
- **Целевая аудитория:** [Кто пользователи системы]
- **Затронутые лица (affected parties):** [Кто получает решения системы]

## 5. Риски и уровень контроля ✓

- **Risk classification:** [High-risk / Medium-risk / Low-risk / Minimal]
- **Обоснование классификации:** [Краткое объяснение]
- **EU AI Act классификация:** [Prohibited / High-risk Annex III / Limited risk / Minimal risk / Not applicable]
- **Уровень человеческого надзора:** [Human-in-the-loop / Human-on-the-loop / Human-in-command]
- **Обоснование уровня:** [Почему этот уровень]
- **Ссылка на AISIA:** [Ссылка на AI System Impact Assessment]
- **Ссылка на risk register:** [Ссылка на запись в реестре рисков]

## 6. Качество и мониторинг

- **Eval-сеты:** [Описание тестовых данных и метрик]
- **Ключевые метрики:** [Accuracy / F1 / Hallucination rate / Latency / etc.]
- **Целевые значения:** [Threshold для каждой метрики]
- **Drift monitoring:** [Инструмент: Fiddler / Arize / Evidently / custom]
- **Частота review:** [Daily / Weekly / Monthly / Quarterly]
- **Triggers для alerting:** [Условия алерта]
- **Bias audit:** [Регулярность + последняя дата]

## 7. Логирование

- **Что логируется:** [Prompts / responses / metadata / errors]
- **Куда:** [Система логирования]
- **Retention:** [Срок хранения логов]
- **Доступ:** [Кто имеет доступ к логам]
- **Immutability:** [Меры защиты от изменения]

## 8. Документация и прозрачность

- **Техническая документация:** [Ссылка]
- **User-facing документация:** [Ссылка]
- **AI disclaimer для пользователя:** [Текст или ссылка на UI-компонент]
- **Канал обратной связи:** [Email / форма для сообщения о проблемах]
- **Apell-процесс:** [Как пользователь может оспорить решение]

## 9. Третьи стороны (для систем на внешних API)

- **Provider:** [OpenAI / Anthropic / Google Cloud]
- **Tier:** [Free / Pay-as-you-go / Enterprise]
- **Training opt-out подтверждён:** [Yes / No, ссылка на контракт]
- **DPA подписан:** [Yes / No, дата]
- **Subprocessors:** [Например, AWS как hosting для Anthropic]
- **Дата последнего vendor review:** [YYYY-MM-DD]

## 10. Жизненный цикл

- **Дата запуска в production:** [YYYY-MM-DD]
- **Запланированный sunset:** [YYYY-MM-DD или "N/A"]
- **Procedure при выводе из эксплуатации:** [Ссылка на процедуру]
- **Дата следующего AISIA review:** [YYYY-MM-DD]
- **Дата следующего bias audit:** [YYYY-MM-DD]

## 11. История изменений

| Дата | Версия | Изменение | Кто внёс |
|------|--------|-----------|----------|
| YYYY-MM-DD | 1.0 | Создание карточки | [Имя] |

## 12. Утверждения

- **Создал:** [Имя, дата]
- **Утвердил (AIMS Lead):** [Имя, дата]
- **Утвердил (Executive sponsor для high-risk):** [Имя, дата]
```

---

## Как заполнять для разных типов систем

### Для classical ML (например, кредитный скоринг)

Заполняются все разделы. Особый фокус на разделах 3 (данные обучения), 6 (eval, drift monitoring), 5 (AISIA для high-risk).

### Для GenAI на API (например, RAG-чатбот на OpenAI)

Раздел 3 «Training data» = «Не обучаем». Раздел 9 (третьи стороны) обязателен и подробный. Раздел 6 фокусируется на hallucination rate и quality metrics, а не на drift в классическом смысле.

### Для fine-tuned LLM

Заполняются все разделы. Раздел 3 включает fine-tuning dataset. Раздел 6 включает eval на оригинальных capabilities (catastrophic forgetting check).

### Для RPA + AI (например, классификация писем)

Облегчённая версия. Если risk classification = Low / Minimal — раздел 5 краткий, AISIA не требуется.

---

## Ссылки

- [Обзор стандарта 42001](../ru/overview.md)
- [ISO 42005 Impact Assessment guide](../ru/iso-42005-impact-assessment-guide.md)
- [GenAI/LLM-specific controls](../ru/genai-llm-specific-controls.md)

---

*Шаблон соответствует требованиям ISO/IEC 42001:2023 Annex A.4.2, A.4.3, A.4.4, A.4.5, A.4.6.*
