+++
title = "Отзывы"
+++

## Добавление отзыва
1. Файл в `content/reviews/`, например `john.md`.
2. Пример фронтматтера:
```toml
+++
title = "John Doe"
date = "2025-02-01"
role = "Founder"        # опционально
rating = 5               # опционально
image = "/img/john.png" # опционально
+++
Отличный продукт!
```
3. Фото — в `static/img/`.

## Вывод отзывов
- Partial: `layouts/partials/reviews.html`.
- Подключение в шаблоне:
```go-html-template
{{ partial "reviews" . }}
```
- При необходимости отфильтруйте `.Site.RegularPages` по секции `"reviews"` внутри partial.
