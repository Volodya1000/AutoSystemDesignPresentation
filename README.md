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

GitHub Actions автоматически компилирует `presentation.tex` в PDF при каждом push в `main`, для каждого pull request и вручную через вкладку Actions.

После успешной сборки при push в `main` файл `presentation.pdf` автоматически коммитится в корень репозитория, если его содержимое изменилось. Для pull request CI проверяет, что презентация компилируется, но не коммитит PDF в чужую ветку.
