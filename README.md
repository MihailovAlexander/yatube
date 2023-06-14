# Проект «API для Yatube»

API для Yatub представляет собой проект социальной сети в которой реализованы следующие возможности: 
- публиковать записи
- комментировать записи
- подписываться или отписываться от авторов

## Стек технологий

- Python 3.11
- Django 4.2
- DRF
- JWT + Djoser

## Запуск проекта в dev-режиме

- Клонировать репозиторий
- Установить и активируйте виртуальное окружение

```bash
python -m venv venv
```

```bash
source venv/Scripts/activate
```

```bash
python -m pip install --upgrade pip
```

- Установить все зависимости из файла requirements.txt

```bash
pip install -r requirements.txt
```

- Накатить миграции:

```bash
cd yatube_api
python manage.py migrate
```

- Создать суперпользователя:

```bash
python manage.py createsuperuser
```

- Запустить проект:

```bash
python manage.py runserver
```

## Примеры


### Работа с публикациями

```
GET, POST /api/v1/posts/
GET, PUT, PATCH, DELETE /api/v1/posts/{id}/
```


### Работа с коментариями

```
GET, POST /api/v1/posts/{post_id}/comments/
GET, PUT, PATCH, DELETE /api/v1/posts/{post_id}/comments/{id}/
```

### Работа с сообществами

```
GET /api/v1/groups/
GET /api/v1/groups/{id}/
```

### Работа с подписками

```
GET /api/v1/follow/
PUT /api/v1/follow/
```

### Работа с JWT-токенами

```
POST api/v1/jwt/create/
POST api/v1/jwt/refresh/
POST api/v1/jwt/verify/
```
