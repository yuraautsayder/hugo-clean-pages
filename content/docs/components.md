+++
title = "Компоненты и шаблоны"
+++

## Partials (включаемые фрагменты)
- `partials/head.html` — метаданные и стили.
- `partials/header.html` — шапка и навигация.
- `partials/footer.html` — подвал.
- `partials/reviews.html` — вывод отзывов.

Подключение partial:
```go-html-template
{{ partial "<name>" . }}
```

## Шаблоны
- Главная: `layouts/index.html`
- Одиночная: `layouts/_default/single.html`
- Список: `layouts/_default/list.html`
- О компании: `layouts/about.html` (при `layout = "about"` в `content/about.md`).

## Меню
Меню можно задать в `hugo.toml` (`[menu.main]`) и итерировать в шаблоне через `site.Menus.main`.

## Стили
Кастомные стили: `static/css/custom.css`. Изображения: `static/img/` → путь `/img/<file>`.
