# MyApi

MyApi — это пример простого веб-приложения на ASP.NET Core, которое предоставляет API для управления пользователями и их постами. Приложение использует Entity Framework Core для работы с базой данных SQL Server.

---

## 🚀 Основные функции

- **CRUD-операции для пользователей:**
  - Создание, чтение, обновление и удаление пользователей.
- **CRUD-операции для постов:**
  - Создание, чтение, обновление и удаление постов.
- **Swagger UI:**
  - Интерактивная документация API с возможностью тестирования.

---

## 🛠️ Технологии

- **ASP.NET Core 8.0**
- **Entity Framework Core**
- **SQL Server**
- **Swagger**

---

## 📂 Структура проекта

MyApi/
├── Controllers/ # Контроллеры API
├── Data/ # Контекст базы данных и миграции
├── Models/ # Модели данных (User, Post)
├── Properties/ # Настройки запуска (launchSettings.json)
├── appsettings.json # Настройки приложения
├── Program.cs # Точка входа приложения
├── MyApi.csproj # Файл проекта
└── README.md # Документация проекта
text

---

## 🔧 Настройка и запуск

### 1. Установите .NET SDK

Убедитесь, что у вас установлен .NET SDK. Скачайте его с [официального сайта](https://dotnet.microsoft.com/ru-ru/download).

### 2. Клонируйте репозиторий

git clone https://github.com/your-username/MyApi.git
cd MyApi
text

### 3. Настройте строку подключения

Откройте файл `appsettings.json` и настройте строку подключения к вашей базе данных:

{
"ConnectionStrings": {
"DefaultConnection": "Server=localhost;Database=MyDatabase;Trusted_Connection=True;TrustServerCertificate=True;"
}
}
text

### 4. Выполните миграцию

Создайте базу данных и примените миграции:

dotnet ef database update
text

### 5. Запустите приложение

dotnet run
text

Приложение будет доступно по адресу:

- HTTP: http://localhost:5017
- Swagger UI: http://localhost:5017/swagger

---

## 📝 Примеры API

### Пользователи

- `GET /api/users` — Получить всех пользователей.
- `GET /api/users/{id}` — Получить пользователя по ID.
- `POST /api/users` — Создать нового пользователя.
- `PUT /api/users/{id}` — Обновить пользователя.
- `DELETE /api/users/{id}` — Удалить пользователя.

### Посты

- `GET /api/posts` — Получить все посты.
- `GET /api/posts/{id}` — Получить пост по ID.
- `POST /api/posts` — Создать новый пост.
- `PUT /api/posts/{id}` — Обновить пост.
- `DELETE /api/posts/{id}` — Удалить пост.
