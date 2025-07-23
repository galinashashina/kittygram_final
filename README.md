# можно хоть какую нибудь подсказку, я все перепробовала, не понимаю в чем проблема

# Социальная сеть любителей котов Kittygram
### URL
Проект развернут на сайте:
https://kittygram999.zapto.org/
### Описание
Kittygram — платформа для публикации котиков.
Kittygram — это веб-приложение, в котором пользователи могут делиться фотографиями своих любимых котов и просматривать чужих. Проект состоит из фронтенда на React и бэкенда на Django, разворачивается в Docker и автоматически деплоится через GitHub Actions.
### Технологии
Python 3.11.1,
Django 4.1,
Django REST framework,
React
### Запуск проекта в dev-режиме
- Клонируйте репозиторий и перейдите в него в командной строке:
```
git clone https://github.com/kovdmit/kittygram_final.git
```
```
cd kittygram_final
```
- Запустите проект с помощью команды:
```
docker compose up
```
- Соберите статику Django с помощью команды:
```
docker compose exec backend python manage.py collectstatic
```
- Скопируйте статику командой:
```
docker compose exec backend cp -r /app/collected_static/. /static/static/
```
