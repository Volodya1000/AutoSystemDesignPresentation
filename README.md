# AutoSystemDesignPresentation

Техническая презентация для системных архитекторов о том, как AutoSystemDesign
превращает Markdown BRD в связанную архитектурную модель и набор проверяемых
артефактов.

За основу оформления и структуры взята авторская версия
`pre-pr22-main-2026-10-22`. Материал сокращён с 27 до 20 слайдов, но сохранены
объяснения архитектуры, доменной модели, валидаторов и repair loop.

## Содержание

Все примеры относятся к одному документу
`examples/requirements/online_store_brd.md` и одному полному запуску:

1. Назначение инструмента и BRD-first workflow.
2. Извлечение требований и проверка исходных цитат.
3. Каталог из 16 связанных выходных артефактов.
4. Архитектура конвейера, типизированные модели и repair loop.
5. C4-модель, её онтология и программные валидаторы.
6. Sequence для `FR-001` и связь участников с C4.
7. Фактический OpenAPI 3.1 и Swagger UI.
8. Расчёт производительности и PDF с вертикальной схемой критического пути.

Для первого запуска достаточно указать BRD:

```bash
uv run python scripts/generate_from_brd.py \
  --document examples/requirements/online_store_brd.md
```

## Компиляция

Потребуются LuaLaTeX, Beamer и DejaVu Sans / DejaVu Sans Mono.

```bash
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
```

GitHub Actions собирает PDF на pull request и push в `main`.
