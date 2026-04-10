# Kittygram

Учебный проект, выполненный в рамках курса Яндекс Практикум.  
Проект представляет собой веб-приложение для публикации информации о питомцах (котах): пользователи могут добавлять карточки питомцев, указывать их характеристики и достижения, а также загружать изображения.

## Функциональность

- регистрация и авторизация пользователей  
- создание, редактирование и удаление записей о питомцах  
- загрузка изображений  
- работа через REST API  
- административная панель Django  

## Стек технологий

Backend:
- Python
- Django
- Django REST Framework
- Gunicorn

Frontend:
- React
- JavaScript

Инфраструктура:
- Docker
- Docker Compose
- PostgreSQL
- Nginx

## Запуск проекта

### 1. Клонирование репозитория

```bash
git clone https://github.com/slavmi1/kittygram_final.git
cd kittygram_final
```

### 2. Создание файла .env

Создать файл .env в корне проекта:
```env
SECRET_KEY=your_secret_key
ALLOWED_HOSTS=localhost,127.0.0.1

POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password

DB_HOST=db
DB_PORT=5432
```

### 3. Запуск контейнеров

```bash
docker compose up -d --build
```

### 4. Миграции и статика

```bash
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic
```

### 5. Создание суперпользователя (опционально)

```bash
docker compose exec backend python manage.py createsuperuser
```

## Доступ

Приложение доступно по адресу:
```http://localhost:9000/```

## Примечание

Проект является учебным и не разрабатывался как полноценный production-сервис.
