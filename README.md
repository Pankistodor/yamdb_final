# infra_sp2
### Описание
Тестовый проект по контейнеризации и разворачиванию Docker
### Технологии
Python 3.7

Django 2.2.19

Djangorestframework 3.12.1

Gunicorn 20.0.4

Postgres

Nginx

Docker
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
``` 
- В папке с проектом для сборки образов выполните команду:
```
docker-compose up
```
- В папке с проектом для обновлениябазы данных выполните команду:
```
docker-compose exec web python manage.py migrate --noinput
```
- В папке с проектом для создания суперпользователя выполните команду:
```
docker-compose exec web python manage.py createsuperuser
```
- В папке с проектом для сборки статических файлов выполните команду:
```
docker-compose exec web python manage.py collectstatic --no-input 
```
### Автор
 pankistodor@gmail.com

### Тесты
![example workflow](https://github.com/Pankistodor/yamdb_final/actions/yamdb_workflow.yml/badge.svg)