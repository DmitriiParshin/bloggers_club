# Bloggers_club - социальная сеть блогеров
## Стек технологий
[![Python](https://img.shields.io/badge/-Python-464646?style=flat-square&logo=Python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat-square&logo=Django)](https://www.djangoproject.com/)
[![Docker](https://img.shields.io/badge/-Docker-464646?style=flat-square&logo=Docker)](https://www.docker.com/)
[![Bootstrap](https://img.shields.io/badge/-Bootstrap-464646?style=flat-square&logo=Bootstrap)](https://getbootstrap.com/)
## Описание проекта
Социальная сеть блогеров для публикации личных дневников с возможностью подписок на блогеров и добавления комментариев к публикациям.
Разработан по MVT архитектуре. Используется пагинация постов и кэширование. Регистрация реализована с верификацией данных, сменой и восстановлением пароля через почту. Написаны тесты проверяющие работу сервиса.
## Запуск проекта
1. Клонируйте репозиторий с проектом и перейдите в каталог с ним:
```
git clone https://github.com/DmitriiParshin/world_of_recipes
cd world_of_recipes
```
2. Создайте файл `.env` и заполните его как показано на примере:
```
touch .env
```
>_DB_ENGINE=YOUR_DB_ENGINE  
DB_NAME=YOUR_DB_NAME  
DB_USER=YOUR_DB_USER  
DB_PASSWORD=YOUR_DB_PASSWORD  
DB_HOST=YOUR_DB_HOST  
DB_PORT=YOUR_DB_PORT_  

3. Запустите контейнеры:
```
sudo docker-compose up -d --build
```
4. Создайте и выполните миграции:
```
sudo docker-compose exec web python manage.py makemigrations
sudo docker-compose exec web python manage.py migrate
```
5. Соберите статику:
```
sudo docker-compose exec web python manage.py collectstatic --no-input
```
6. Создайте суперпользователя:
```
sudo docker-compose exec web python manage.py createsuperuser
```
Перейдите на http://localhost:8000/ и авторизуйтесь
## Автор
[Паршин Дмитрий](https://github.com/DmitriiParshin)