### Описание проекта

Социальная сеть yatube с возможностью создавать посты с картинками, подписываться на авторов, 
комментировать посты, писать посты в тематические сообщества. Это учебный проект для изучения проектирования API (permissions, пагинация, throttling, 
фильтрация, сортировка, поиск) и других backend техник в Python. 

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/elina-kanz/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
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

### Примеры запросов

GET-запрос для получения списка всех публикаций, POST-запрос для создания публикации (доступно только для авторизированных пользователей) 

```
http://127.0.0.1:8000/api/v1/posts/
```

GET-запрос для получения публикации по id, PUT-запрос для редактирования (доступно только для автора поста)

```
http://127.0.0.1:8000/api/v1/posts/{id}/
```

GET-запрос для получения списка всех комментариев к посту по его id, POST-запрос для создания комментария 
(только для авторизированных пользователей)

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
