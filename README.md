# Проект «API для Yatube».

### Описание проекта:

Проект api_yatube - это API социальной сети yatube.

С помощью api_yatube можно запрашивать данные о постах, группах, комментариях в социальной сети Yatube, а также создавать новые.

Yatube - это учебный проект курса "backend-python" от Яндекс-Практикума.

## Стек технологий

* Python 3.11,
* Django 4.2,
* DRF,
* JWT + Djoser


### Как запустить проект:

- Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone git@github.com:TonyxRazzor/api_final_yatube.git
```

```bash
cd api_final_yatube
```

- Cоздать и активировать виртуальное окружение:

```bash
python3 -m venv env
```

```bash
source env/bin/activate
```

- Установить зависимости из файла requirements.txt:

```bash
python3 -m pip install --upgrade pip
```

```bash
pip install -r requirements.txt
```

- Выполнить миграции:

```bash
python3 manage.py migrate
```

- Запустить проект:

```bash
python3 manage.py runserver
```

### Примеры запросов к API:

- Получить список всех постов (GET):
```r
http://127.0.0.1:8000/api/v1/posts/
```

- Получить определенный пост (GET):
```r
http://127.0.0.1:8000/api/v1/posts/1/
```

- Получить коментарии определенного поста (GET):
```r
http://127.0.0.1:8000/api/v1/posts/1/comments/
```

- Получить список всех групп (GET):
```r
http://127.0.0.1:8000/api/v1/groups/
```

- Создать новый пост (POST):

(Требуется аутентификация)
```r
http://127.0.0.1:8000/api/v1/posts/
```


## Добавить группу в проект нужно через админ панель Django:

- Создаем суперпользователя:

```bash
python manage.py createsuperuser
```

- После авторизации, переходим в раздел Groups и создаем группы.

```r
http://127.0.0.1:8000/admin/
```


## Доступ авторизованным пользователем доступен по JWT-токену (Joser), который можно получить выполнив POST запрос по адресу:

```r
http://127.0.0.1:8000/api/v1/jwt/create/
```

- Передав в body данные пользователя (например в postman):

```json
{
"username": "Username",
"password": "Password"
}
```

Автор:
* ToNy_RaZZoR