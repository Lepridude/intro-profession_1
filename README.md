# Практическая работа №1 — Репозитории и интеграции

**Студент:** Архангельский Данила Андреевич  
**Группа:** ИСТ-05

## О проекте

Небольшой Python-проект для получения информации о фильмах через OMDb API. В нём показаны HTTP-запросы, обработка JSON и работа с переменными окружения.

## Клонирование

```bash
git clone https://github.com/Lepridude/intro-profession_1.git
cd intro-profession_1
python -m venv .venv
```

Активируйте окружение и установите зависимости:

```bash
# macOS / Linux
source .venv/bin/activate
# Windows PowerShell
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Структура проекта

- `rest_api_demo.ipynb` — ноутбук с запросом к OMDb API.
- `reflection1.md` — рефлексия по занятию.
- `INSTRUCTION.md` — описание этапов работы с Git и GitHub.
- `requirements.txt` — зависимости Python.
- `.env.example` — пример файла для API-ключа.

## Ветки

- `master` — основная версия и результат слияния Pull Request.
- `movie-output-feature` — вывод актёров и краткой итоговой строки.
- `env-feature` — загрузка ключа из `.env` и обработка ошибок API.

Для работы с `env-feature` скопируйте `.env.example` в `.env` и укажите свой ключ OMDb:

```env
OMDB_API_KEY=ваш_ключ_OMDb
```

Файл `.env` уже добавлен в `.gitignore`. Не публикуйте его и не сохраняйте ключ в выводах Jupyter.
