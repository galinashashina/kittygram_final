### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram_backend.git
```

```
cd kittygram_backend
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

Как запустить через Docker
Убедитесь, что у вас установлен Docker и Docker Compose.
1. Создайте .env файл в корне проекта
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=securepassword
DB_HOST=db
DB_PORT=5432
2. Запустите проект:
docker compose -f docker-compose.production.yml up -d --build
3. После запуска:
Kittygram будет доступен по адресу: http://localhost:9000
Админка Django: http://localhost:9000/admin/
