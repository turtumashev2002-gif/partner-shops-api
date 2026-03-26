# API: Партнерские магазины

## Endpoint

GET /api/v1/partner-shops

---

## Пример запроса

GET /api/v1/partner-shops?limit=10&offset=0

---

## Пример ответа

```json
{
  "status": "success",
  "data": {
    "shops": [
      {
        "id": "shop_101",
        "name": "Green Market",
        "description": "Свежие фермерские продукты",
        "image_url": "https://cdn.petrushka.ru/shops/green-market.png",
        "rating": 4.7,
        "reviews_count": 124,
        "delivery_time": "30-45 мин",
        "is_open": true,
        "external_url": "https://greenmarket.ru"
      }
    ]
  }
}
```

---

## Переход по клику

Используется поле:
external_url

---

## Допущения

* Переход на сайт магазина осуществляется через поле `external_url`
* Список магазинов может быть расширен (используется пагинация)
* Данные о рейтинге и времени доставки приходят с backend

---

## Возможные улучшения

* Добавить фильтрацию (по рейтингу, открыт/закрыт)
* Добавить сортировку
* Кэширование данных на клиенте

