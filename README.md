# Уважаемый гость! Если пользуешься данным репозиторием буду рад если нажмешь ⭐ в правом верхнем углу экрана.

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white) ![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray) 



# Проект «Yatube»

Yatube представляет собой проект социальной сети в которой реализованы следующие возможности: 
- публиковать записи
- комментировать записи
- подписываться или отписываться от авторов

## Стек технологий

- Python 3.11
- Django 4.2
- Django REST framework 3.12.4
- JWT + Djoser

## Запуск проекта в dev-режиме

- Клонировать репозиторий
- Установить, активировать и обновить виртуальное окружение

```bash
python -m venv venv
source venv/Scripts/activate
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

## Запуск тестов

Находясь в главной папке проекта, где есть папка  `tests`, при активированном виртуальном окружении выполнить 

```bash
pytest
```

## Примеры


### Работа с публикациями

```
GET, POST /api/v1/posts/
GET, PUT, PATCH, DELETE /api/v1/posts/{id}/
```


### Работа с комментариями

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
