# Практическая работа №1 — Репозитории и интеграции

## Назначение

Проект демонстрирует запрос к OMDb API из Python, обработку JSON и работу с ветками Git. Репозиторий размещён на GitHub.

## Подготовка

1. Установить Git и Python.
2. Склонировать репозиторий:

```bash
git clone https://github.com/Lepridude/intro-profession_1.git
cd intro-profession_1
```

3. Создать виртуальное окружение и установить зависимости:

```bash
python -m venv .venv
# macOS / Linux
source .venv/bin/activate
# Windows PowerShell: .venv\\Scripts\\Activate.ps1
python -m pip install requests python-dotenv ipykernel
```

## Основная ветка

В `master` находится основная версия ноутбука. Она запрашивает название фильма, обращается к OMDb API и выводит основные поля ответа.

Перед фиксацией изменений очистить вывод ячеек Jupyter, чтобы не сохранить случайно ключ или лишние данные.

```bash
git add rest_api_demo.ipynb .gitignore README.md
git commit -m "Добавлен базовый пример movie API"
git push origin master
```

## Дополнительный вывод

Изменения с выводом актёров и итоговой строки находятся в `movie-output-feature`. Ветка предназначена для отдельной доработки и слияния с `master` через Pull Request на GitHub.

```bash
git switch movie-output-feature
git push -u origin movie-output-feature
```

На GitHub создать Pull Request из `movie-output-feature` в `master`, проверить изменения и выполнить merge.

## Переменные окружения

Ветка `env-feature` переносит API-ключ в `.env` и загружает его через `python-dotenv`. Файл `.env` должен оставаться локальным.

```bash
git switch env-feature
python -m pip install python-dotenv
```

Создать `.env`:

```env
OMDB_API_KEY=ваш_ключ
```

Проверить, что `.env` не отображается в `git status`, затем отправить ветку:

```bash
git status
git add rest_api_demo.ipynb .gitignore
git commit -m "Ключ API читается из .env через python-dotenv"
git push -u origin env-feature
```

`env-feature` не вливать в `master`, если это отдельно не требуется преподавателем.

## Проверка обработки ошибок

В улучшенной версии предусмотрены тайм-аут запроса, проверка отсутствующего ключа, обработка сетевых ошибок и проверка поля `Response` в ответе OMDb. Проверить три случая:

1. Существующий фильм — выводятся его данные.
2. Несуществующее название — выводится сообщение, что фильм не найден.
3. Неверный ключ — выводится сообщение об ошибке доступа.

## Важно

- Не добавлять `.env`, `.venv/` и секретные ключи в коммиты.
- Перед отправкой ноутбука очищать output ячеек.
- Запуск реального запроса к OMDb требует действующего API-ключа.
- Code review и тестирование через сторонние учебные сервисы отмечать выполненными только после фактического прохождения.
