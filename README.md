# AutoSystemDesignPresentation

Техническая презентация для системных архитекторов о том, как AutoSystemDesign
превращает Markdown BRD в связанную архитектурную модель и набор проверяемых
артефактов.

За основу оформления и структуры взята авторская версия
`pre-pr22-main-2026-10-22`. Материал сокращён с 27 до 21 слайда, но сохранены
объяснения архитектуры, доменной модели, валидаторов и цикла исправления ответа.

## Содержание

Все примеры относятся к одному документу
`examples/requirements/online_store_brd.md` и одному полному запуску:

1. Назначение инструмента и BRD-first workflow.
2. Извлечение требований и проверка исходных цитат.
3. Минимальная команда и сразу за ней скриншот входного BRD и созданных артефактов.
4. Архитектура конвейера, типизированные модели и цикл исправления ответа.
5. C4-модель, её онтология и программные валидаторы.
6. Sequence для `FR-001` и связь участников с C4.
7. Сгенерированный OpenAPI 3.1 и Swagger UI.
8. Расчёт производительности, критический путь и загрузка компонентов.

Схема критического пути и таблица нагрузки показаны на отдельных слайдах.
Оба фрагмента вставлены непосредственно из исходного отчёта
`images/online_store_brd_performance_report.pdf` с сохранением векторного текста.
В заголовках отмечено, что это фрагменты сгенерированного PDF-отчёта.

Для первого запуска достаточно указать BRD:

```powershell
uv run python scripts/generate_from_brd.py `
  --document examples/requirements/online_store_brd.md
```

## Компиляция

Потребуются LuaLaTeX, Beamer и DejaVu Sans / DejaVu Sans Mono.

```bash
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
```

GitHub Actions собирает PDF на pull request и push в `main`.
