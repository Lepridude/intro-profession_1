# Практическая работа № 2 — вариант 01

**Студент:** Архангельский Данила Андреевич  
**Группа:** ИСТ-05  
**Репозиторий:** https://github.com/Lepridude/intro-profession_1

## Состав
- llm_demo.ipynb — ноутбук с GigaChat, LangChain, базовым промптом, Few-shot, JSON-парсером и Pydantic.
- data/rental_01.csv — 15 исходных заявок варианта 01.
- gold_fields_01.csv — ручная эталонная разметка.

## Запуск
Установить зависимости:
```bash
python -m venv .venv
source .venv/bin/activate
pip install -U jupyter ipykernel langchain-gigachat pandas pydantic python-dotenv
```
Создать рядом с ноутбуком локальный .env:
```dotenv
GIGA_KEY=ВАШ_НОВЫЙ_КЛЮЧ
```
Не добавлять .env в Git и не отправлять ключ в переписку. Запустить Jupyter и выполнить llm_demo.ipynb сверху вниз.

Метрики появятся только после реального обращения к GigaChat. remarks размечено, но не включено в среднюю числовую точность, поскольку это свободный текст.
