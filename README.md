# Практическая работа №1 — Репозитории и интеграции

**Студент:** Архангельский Данила Андреевич  
**Группа:** ИСТ-05

## О проекте

Небольшой Python-проект для получения информации о фильмах через OMDb API. Пример показывает работу с HTTP-запросом, JSON-ответом и переменными окружения.

## Файлы

- `rest_api_demo.ipynb` — основной ноутбук с запросом к OMDb API и выводом информации о фильме.
- `reflection1.md` — рефлексия по занятию.
- `INSTRUCTION.md` — описание этапов работы и команд Git.
- `.gitignore` — исключает виртуальное окружение и файл с секретным ключом.

## Запуск

```bash
python -m venv .venv
# macOS / Linux
source .venv/bin/activate
# Windows PowerShell: .venv\\Scripts\\Activate.ps1
python -m pip install requests python-dotenv ipykernel
```

Для версии из ветки `env-feature` создайте `.env` в корне проекта:

```env
OMDB_API_KEY=ваш_ключ_OMDb
```

Не добавляйте `.env` в Git и не сохраняйте API-ключ в выводах Jupyter.
