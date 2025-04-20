
# 🛒 Backend для интернет-магазина на FastAPI

Полноценный бэкенд интернет-магазина, реализованный с использованием **FastAPI** и структурированный по модулям. Проект включает всё необходимое для работы магазина: пользователи, продукты, корзина, лайки, комментарии, история покупок, промокоды и техподдержка.

## 🚀 Возможности

- 👤 Регистрация и управление пользователями
- 📦 CRUD-продукты и категории
- 🛒 Работа с корзиной и оформлением заказов
- 💬 Комментарии к товарам
- ❤️ Лайки на продукты и комментарии
- 🧾 История покупок
- 🎁 Промокоды и скидки
- 🤖 Ссылка на бота поддержки Telegram

## 📁 Структура проекта

```
api/
│
├── users.py         # Работа с пользователями
├── products.py      # Продукты
├── likes.py         # Лайки
├── comments.py      # Комментарии
├── orderhistory.py  # История заказов
├── promo.py         # Промокоды
├── support.py       # Поддержка
│
└── result_message.py  # Общий ответ API

db/
└── productservice.py  # Функции для работы с базой данных
```

## ⚙️ Установка и запуск

```bash
# Клонировать репозиторий
git clone https://github.com/username/project-name.git
cd project-name

# Установить зависимости
pip install -r requirements.txt

# Запустить приложение
uvicorn main:app --reload
```

После запуска API будет доступен по адресу:  
📍 `http://127.0.0.1:8000`

Swagger UI: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)  
ReDoc: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

## 📌 Примеры API

### 🔐 Регистрация пользователя

`POST /user/register_user`

```json
{
  "username": "johndoe",
  "phone_number": "998901234567",
  "email": "john@example.com",
  "password": "securepass",
  "name": "John",
  "surname": "Doe",
  "age": 25,
  "city": "Tashkent"
}
```

---

### ➕ Добавить продукт

`POST /product/add_product`

```json
{
  "user_id": 1,
  "pr_name": "Ноутбук Lenovo",
  "pr_description": "Игровой ноутбук с RTX 4060",
  "pr_price": 1500.99,
  "pr_quantity": 5,
  "category_id": 2
}
```

---

## 🤝 Связь с поддержкой

[Поддержка в Telegram](https://t.me/PySiteSupportBot)

---

## 📎 Технологии

- **Python 3.10+**
- **FastAPI**
- **Pydantic**
- **Uvicorn**
- **PostgreSQL / SQLite**
- (опционально: SQLAlchemy, Alembic)

---

## 📌 Примечание

Проект создан как часть портфолио. Вы можете использовать его как основу для своего интернет-магазина.
