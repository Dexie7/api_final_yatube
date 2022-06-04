
### Задание:
Обработка запросов в приложении api. Осуществляем операции CRUD с публикациями, комментариями к ним, сообществами, подписками на авторов, с получением, обновлением и проверкой токенов.

### Установка:

*Клонировать репозиторий и перейти в него в командной строке:

```
**git clone https://github.com/David18704/api_final_yatube.git**
```

```
**cd api_final_yatube**
```

*Cоздать и активировать виртуальное окружение:

```
**python -m venv env**
```

```
**source venv/Scripts/activate**
```

*Установить зависимости из файла requirements.txt:

```
**python -m pip install --upgrade pip**
```

```
**pip install -r requirements.txt**
```

*Выполнить миграции:

```
**python manage.py migrate**
```

*Запустить проект:

```
**python manage.py runserver**
```
### Примеры:
POST-запрос http://127.0.0.1:8000/api/v1/follow/
    {
        "user": "admin",
        "following": "admin1"
    }
GET-запрос  http://127.0.0.1:8000/api/v1/posts/
    {
        "id": 1
        "author": "admin",
        "text": "Тест для файла README.md"
        "pub_date": "2021-09-19T12:02:55.024756Z",
        "image": null,
        "group": null
    }
 GET-запрос  http://127.0.0.1:8000/api/v1/posts/2/comments/
 {
   "text": "Верно",
   "post": "2",
        "author": "admin"
}
 
