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

- В pull request из этой же репозитория сгенерированный `presentation.pdf` автоматически коммитится в ветку PR, если его содержимое изменилось, поэтому он виден в **Files changed**.
- При push в `main` обновлённый `presentation.pdf` автоматически коммитится в корень репозитория, если файл изменился.
- Каждый успешный запуск также публикует PDF как артефакт `AutoSystemDesignPresentation-pdf` на 30 дней. Артефакт доступен на странице запуска во вкладке Actions.

## Изображения для слайдов-примеров

Добавьте в каталог `images/` пять файлов:

- `c4_example_1.png` — первый пример C4-диаграммы.
- `c4_example_2.png` — второй пример C4-диаграммы.
- `sequence_example_1.png` — первый пример диаграммы последовательностей.
- `sequence_example_2.png` — второй пример диаграммы последовательностей.
- `swagger_ui.png` — скриншот Swagger UI.

Это только слайды-примеры, которые уже были в презентации до PR. Основные слайды C4 и sequence не менялись.
