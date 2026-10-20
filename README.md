# AutoSystemDesignPresentation

Исходный код презентации AutoSystemDesign на LaTeX Beamer.

## Компиляция

Для локальной сборки нужен LuaLaTeX, пакет Beamer и шрифты DejaVu Sans / DejaVu Sans Mono (или совместимые).

```bash
lualatex presentation.tex
lualatex presentation.tex
```

Повторный запуск помогает обновить нумерацию и внутренние ссылки.

## CI и PDF

GitHub Actions автоматически компилирует `presentation.tex` в PDF при каждом push в `main`, для каждого pull request и вручную через вкладку Actions. Готовый `presentation.pdf` загружается как артефакт workflow с именем `AutoSystemDesignPresentation-pdf` и хранится 30 дней.

PDF не коммитится в репозиторий: его можно скачать со страницы соответствующего запуска Actions в разделе Artifacts.
