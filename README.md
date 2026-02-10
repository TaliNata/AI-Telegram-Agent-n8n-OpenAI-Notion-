# Описание

AI-агент для Telegram, реализованный в n8n, с поддержкой пользовательских и плановых сценариев, интеграцией OpenAI и Notion, централизованной обработкой ошибок и логированием.

---

# Возможности

Обработка пользовательских команд из Telegram
Автоматические сценарии по расписанию (Cron)
Генерация контента и аналитики через LLM
Работа с данными из Notion
Логирование результатов обработки
Централизованная обработка ошибок и уведомления

---

# Архитектура

Telegram Trigger — входная точка
Валидация команд и контекста
Fetch / Aggregate Notion data
Dynamic Prompt Builder
OpenAI Chat Model (LLM Chain)
Telegram Response Formatter
Logging в Notion
Error Trigger + Telegram Alerts

Архитектура построена модульно и масштабируется добавлением новых сценариев без изменения базового workflow.

---

# Поддерживаемые сценарии

1. дайджест 

2. резюмирование данных (insight, news, tasks, ideas)

3. автоматические отчёты

# Стек

n8n
Telegram Bot API
OpenAI API
Notion API
JavaScript
Cron

# Доступ к реализации

Полный workflow, credentials и production-конфигурация не публикуются.
Демо и архитектурный разбор доступны по запросу.
