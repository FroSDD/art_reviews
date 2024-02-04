![yamdb_final event parameter](https://github.com/FroSDD/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?event=push)

## Социальная сеть для отзывов о фильмах, книгах и музыке

Проект является бэкендом портала обзоров на различные произведения искусства, включающий систему публикации сведений о произведении, обзоров и комментариев к ним.
Включает в себя базу данных и открытый API.

### API позволяет:
* Администраторам: публиковать сведения о произведениях
* Получить сведения об оцениваемых произведениях
* Публиковать обзоры и рецензии
* Публиковать комментарии к обзорам и рецензиям

### Документация проекта:
Доступна по адресу
```
http://127.0.0.1:8000/redoc/
```
После запуска проекта.

### Как запустить проект на удаленном сервере:
Клонировать репозиторий и перейти в него в командной строке:
```
https://github.com/FroSDD/art_reviews
```

Выполнить вход на свой удаленный сервер

Произвести установку docker:
```
sudo apt install docker.io
```

Установить docker-compose:
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Запустить docker-compose:
```
docker-compose up -d --build
```

Собрать файлы статики и выполнить миграции:
```
docker-compose exec web python3 manage.py makemigrations
```
```
docker-compose exec web python3 manage.py migrate
```
```
docker-compose exec web python3 manage.py collectstatic --no-input
```
Создать суперпользователя:
```
docker-compose exec web python3 manage.py createsuperuser
```

### Использованные технологии:
* Django
* Django Rest Framework
* Nginx
* PostgreSQL
* Docker
* GitHub Actions

### Развернутый проект:
http://158.160.104.159/api/v1/

### Автор: 
[Anton Novikov](https://github.com/FroSDD/)

E-mail: novikov.an_v@mail.ru
