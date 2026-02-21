# Описание

AI-агент для Telegram, реализованный в n8n, с поддержкой пользовательских и плановых сценариев, интеграцией OpenAI и Notion, централизованной обработкой ошибок и логированием.

---

<img width="1642" height="666" alt="Workflow Screenshot AI-Telegram-Agent-n8n-OpenAI-Notion" src="https://github.com/user-attachments/assets/55b98d57-f315-4499-b457-a3bbf88e5a1b" />


---

## Возможности

- Обработка пользовательских команд из Telegram;
- Автоматические сценарии по расписанию (Cron);
- Генерация контента и аналитики через LLM;
- Работа с данными из Notion;
- Логирование результатов обработки;
- Централизованная обработка ошибок и уведомления.

---

## Архитектура
```
- Telegram Trigger — входная точка
- Валидация команд и контекста
- Fetch / Aggregate Notion data
- Prompt Builder
- OpenAI Chat Model (LLM Chain)
- Telegram Response Formatter
- Logging в Notion
- Error Trigger + Telegram Alerts
```
Архитектура построена модульно и масштабируется добавлением новых сценариев без изменения базового workflow.

---

## Поддерживаемые сценарии

1. /news — дайджест новостей за прошлую неделю (фильтрация записей property_type = news, обзор ключевых событий и трендов);

2. /ideas — дайджест идей за прошлую неделю (фильтрация записей property_type = idea, фокус на практической ценности);

3. /report — аналитический отчёт за прошлую неделю (фильтрация записей property_type = report, результаты и тенденции);

4. /digest (fallback, по умолчанию) — универсальный дайджест.

---

# Стек
```
n8n
Telegram Bot API
OpenAI API
Notion API
JavaScript
Cron
```
