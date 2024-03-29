# Проект YaMDb
### Описание
Проект YaMDb собирает отзывы Review пользователей на произведения Title. Произведения делятся на категории: Книги, Фильмы, Музыка. Список категорий Category может быть расширен. Сами произведения в YaMDb не хранятся. В каждой категории есть произведения: книги, фильмы или музыка. Произведению может быть присвоен жанр из списка предустановленных. Новые жанры может создавать только администратор. Пользователи оставляют к произведениям текстовые отзывы Review и выставляют произведению рейтинг.

### Запуск проекта в dev-режиме
1. Клонировать репозиторий:
2. Перейти в папку с проектом:
3. Установить виртуальное окружение для проекта:
```
python -m venv venv
``` 
4. Активировать виртуальное окружение для проекта:
```
# для OS Lunix и MacOS
source venv/bin/activate

# для OS Windows
source venv/Scripts/activate
```
5. Установить зависимости:
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```
6. Выполнить миграции на уровне проекта:
```
cd yatube
python3 manage.py makemigrations
python3 manage.py migrate
```
7. Запустить проект локально:
```
python3 manage.py runserver

# адрес запущенного проекта
http://127.0.0.1:8000
```
8. Импорт данных из static/data:
```
python3 manage.py import_data
```
9.Внимание, если при импорте возникают конфликты с ранее загруженными данными, то можно запустить скрипт с аругментов для предварительной очистки всех моделей:
```
python3 manage.py import_data --clear
```
10.
Правда, в этом случае и суперюзер будет удален, так что скорее всего придется сделать
```
python manage.py createsuperuser
```
### Автор проекта
Артем Римша
