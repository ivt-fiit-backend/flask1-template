# Flask

## Задание

Создайте REST API на базе Flask со следующими моделями:

* Книга
  * Наименование
  * Описание

* Автор
  * Фамилия (строка до 50 символов)
  * Имя (строка до 50 символов)
  * Отчество (строка до 50 символов, необязательное)

Обе модели должны быть связаны отношением типа Many-to-Many.

Модели должны предоставить следующие действия:

* `GET` `/books/` — постраничный список книг
* `POST` `/books/` — создание книги
* `GET` `/books/<id>/` — описание книги
* `PUT` `/books/<id>/` — изменение книги
* `DELETE` `/books/<id>/` — удаление книги
* `GET` `/authors/` — постраничный список авторов
* `POST` `/authors/` — создание автора
* `GET` `/authors/<id>/` — описание автора
* `PUT` `/authors/<id>/` — изменение автора
* `DELETE` `/authors/<id>/` — удаление автора

Проект должен иметь админку для редактирования данных.

Убедитесь, что REST API работает с Curl или Postman.

## Работа с виртуальным окружением

Создание и активация виртуального окружения в Windows:

```powershell
py -m venv venv
```

Активация виртуального окружения в командной строке Windows:

```console
venv\scripts\activate.bat
```

Активация виртуального окружения в Powershell:

```powershell
venv\scripts\activate.ps1
```

Если Powershell не запускает скрипты, запустите Powershell с правами администратора и выполните:

```powershell
Get-ExecutionPolicy
Set-ExecutionPolicy Unrestricted
Get-ExecutionPolicy
```

## Работа с Flask Migrate

Инициализация проекта:

```powershell
python manage.py init
```

Реструктуризация базы данных:

```powershell
python manage.py makemigrations <имя приложения>
python manage.py migrate
```

## Запуск веб-сервера

Включение отладочного режима в командной строке Windows:

```console
set FLASK_DEBUG=1
```

Включение отладочного режима в Powershell:

```powershell
$ENV:FLASK_DEBUG=1
```

Запуск веб-сервера:

```powershell
flask run
```

## Ссылки

* https://flask.palletsprojects.com/en/2.2.x/
* https://flask-restx.readthedocs.io/en/latest/
* https://flask-sqlalchemy.palletsprojects.com/en/3.0.x/
* https://flask-migrate.readthedocs.io/en/latest/
* https://flask-admin.readthedocs.io/en/latest/
* https://flask-marshmallow.readthedocs.io/en/latest/
