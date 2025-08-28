# Проект Hugo Clean

Этот репозиторий содержит сайт на Hugo с пользовательской темой `ga-hugo-theme`.

## Быстрый старт

1. Установите Hugo (extended): https://gohugo.io/getting-started/installing/
2. Запустите сервер разработки:

```bash
hugo server -D
```

- Откройте `http://localhost:1313`
- Флаг `-D` показывает черновики (`draft = true`)

## Структура проекта

- `content/` — контент сайта в Markdown
  - `posts/` — статьи (посты)
  - `reviews/` — отзывы
  - `about.md` — страница «О компании» (использует кастомный шаблон)
- `themes/ga-hugo-theme/` — шаблоны темы и partials
  - `layouts/`
    - `_default/single.html` — шаблон одиночной страницы
    - `_default/list.html` — шаблон страниц-списков (секции, таксономии)
    - `index.html` — шаблон главной страницы
    - `about.html` — кастомный шаблон страницы «О компании»
    - `partials/` — `head.html`, `header.html`, `footer.html`, `reviews.html`
- `static/`  статические файлы (например, `/img`)
- `assets/` — `/css` и `resources/` — пайплайн-ресурсы Hugo
- `hugo.toml` — конфигурация сайта (меню, тема и т. д.)

## Основы контента

- Фронтматтер используется в формате TOML (`+++`). Частые поля:
  - `title`, `date`, `draft`, `image`, `author`, `description`
- Изображения: кладите файлы в `static/img/` и ссылайтесь как `/img/<file>`

## Обзор шаблонов

- Главная: `themes/ga-hugo-theme/layouts/index.html`
- Одиночные страницы: `themes/ga-hugo-theme/layouts/_default/single.html`
- Списки: `themes/ga-hugo-theme/layouts/_default/list.html`
- Страница «О компании»: укажите `layout = "about"` в `content/about.md`, чтобы использовался `layouts/about.html`
- Партшал с отзывами: `themes/ga-hugo-theme/layouts/partials/reviews.html`
