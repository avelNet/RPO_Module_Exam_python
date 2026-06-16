# Отчет об устранении инцидентов (NexusMonitor)

---

### Инцидент №1: Отсутствие базовых зависимостей
**СИМПТОМ:**
`ModuleNotFoundError: No module named 'pydantic_settings'` при попытке запуска бэкенда.
**ПРИЧИНА:**
Разработчик использовал библиотеку `pydantic-settings` для управления конфигурацией, но не включил её в файл зависимостей `requirements.txt`.
**РЕШЕНИЕ:**
Пакет `pydantic-settings` добавлен в `backend/requirements.txt`.
**КОММИТ:**
`98d081b`

---

### Инцидент №2: Отсутствие драйвера PostgreSQL
**СИМПТОМ:**
`ModuleNotFoundError: No module named 'psycopg2'` при попытке запуска приложения.
**ПРИЧИНА:**
Для работы SQLAlchemy с базой данных PostgreSQL требуется драйвер-адаптер, который не был указан в зависимостях.
**РЕШЕНИЕ:**
Пакет `psycopg2-binary` добавлен в `backend/requirements.txt`.
**КОММИТ:**
[будет обновлено после пуша]
