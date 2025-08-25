+++
title = "Контент: статьи и «О компании»"
+++

## Добавление статьи
1. Файл в `content/posts/`, например `my-post.md`.
2. Пример фронтматтера:
```toml
+++
title = "Заголовок"
date = "2025-02-01"
draft = false
image = "/img/cover.png" # опционально
author = "Имя"          # опционально
+++
```
3. Картинки — в `static/img/`, ссылки вида `/img/<file>`.

## Списки и одиночные
- Списки рендерит `layouts/_default/list.html` (перебирает `.Pages`).
- Одиночные — `layouts/_default/single.html`.

## Редактирование «О компании»
- Файл: `content/about.md`.
- Использует шаблон `layouts/about.html` (за счёт `layout = "about"`).
- Частые поля:
```toml
+++
title = "О компании"
description = "Информация"
layout = "about"
image = "/img/<опционально>"
+++
```
- Тело — Markdown: миссия, ценности, контакты и т. п.

## Страница секции
- Необязательно: `content/posts/_index.md` для заголовка/описания списка.
