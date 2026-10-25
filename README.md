# AutoSystemDesignPresentation

Лаконичная техническая презентация для системных архитекторов: пять слайдов,
один BRD и артефакты одного полного запуска AutoSystemDesign.

## Содержание

1. Граница сценария и подтверждённые входные параметры.
2. Одна команда из Markdown BRD и каталог результата.
3. Связь модели C4 с Sequence для `FR-001`.
4. OpenAPI 3.1 и Swagger UI с трассировкой к FR, Sequence и компонентам.
5. Performance-отчёт, результат NFR-проверок и границы достоверности.

В презентации используются артефакты сценария `online_store_brd`: C4, Sequence,
OpenAPI, Swagger и performance report получены из одного каталога запуска. На
последнем слайде намеренно показано ограничение: бюджет проверен, а p95 не
оценён, потому что валидатора процентиля пока нет.

Файлы `online_store_run_tree.png` и `online_store_powershell.png` показывают
рабочий каталог и консольный вывод. Команда на слайде отражает актуальный
BRD-first entry point; YAML остаётся автоматически созданным промежуточным
представлением.

## Компиляция

Потребуются LuaLaTeX, Beamer и DejaVu Sans / DejaVu Sans Mono.

```bash
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
lualatex -interaction=nonstopmode -halt-on-error presentation.tex
```

GitHub Actions собирает PDF на pull request и push в `main`.
