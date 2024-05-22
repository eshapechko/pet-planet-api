# Документация серверного API

## Конечные точки (Endpoints)

### 1. Получение всех товаров

- **Метод**: GET
- **URL**: `/api/products`
- **Описание**: Запрос возвращает список всех продуктов.

### 2. Получение товаров по категориям

- **Метод**: GET
- **URL**: `/api/products/category/:category`
- **Описание**: Запрос возвращает список товаров по заданной категории.
- **Параметры пути**:
  - `category`: строка - категория товаров.

### 3. Получение списка товаров по ID

- **Метод**: GET
- **URL**: `/api/products/list/:ids`
- **Описание**: Запрос возвращает список товаров по указанным ID.
- **Параметры пути**:
  - `ids`: строка - список ID товаров, разделённых запятыми.

### 4. Получение одного товара по ID

- **Метод**: GET
- **URL**: `/api/products/:id`
- **Описание**: Запрос возвращает один товар по указанному ID.
- **Параметры пути**:
  - `id`: строка - ID товара.

### 5. Оформление заказа

- **Метод**: POST
- **URL**: `/api/orders`
- **Описание**: Запрос создаёт новый заказ с данными, предоставленными в теле запроса.
- **Тело запроса**:
  ```json
  {
    "products": [
      {
        "id": "1",
        "quantity": 2
      },
      {
        "id": "2",
        "quantity": 3
      }
    ],
    "storeId": "1"
  }
  ```
