# Kittygram 

## Описание проекта:
Kittygram — социальная сеть для обмена фотографиями котиков. Проект состоит из бэкенд-приложения на Django и фронтенд-приложения на React. Проект позволяет просматривать, публиковать и редактировать посты с изображениями котов с указанием дополнительной ифнормации (имя, возраст, цвет и достижения котика).

## Технологии:

Python  
Django  
React  
Nginx  
Gunicorn  
Certbot
Docker 
Github Actions

## Инструкция по запуску:

### Клонируйте репозиторий:   
```sh/bash
git@github.com:AliceBolgarina/.git
```
   
```sh/bash
cd kittygram
```
Выполнить запуск:

```sh/bash
sudo docker compose -f docker-compose.yml up
```

Выполнить миграции и сбор статики: 

```sh/bash
sudo docker compose -f docker-compose.yml exec backend python manage.py migrate
sudo docker compose -f -docker-compose.yml exec backend python manage.py collectstatic --no-input
sudo docker compose -f docker-compose.yml exec backend cp -r /app/collected_static/. /static/static/
```

## Автор: 
   
[Алиса Болгарина](https://github.com/AliceBolgarina)
