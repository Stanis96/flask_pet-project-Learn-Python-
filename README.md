# Веб-приложение на основе фреймворка Flask: сайт подбора беспроводных наушников
 
Концепция:
Веб-сайт предоставляет пользователям возможность подбирать определенный 
товар под конкретные нужды, используя всеми привычную фильтрацию поиска, 
но без задействования технических характеристик товара 
(пользователь основывается на свои предпочтения и желания к искомому продукту).

На данный момент реализован функционал:
1. Регистрация и авторизация пользователей;
2. Назначение на роль админа через БД (SQLite);
3. Добавление товаров с помощью страницы сайта (досупна только админам);
4. Получение данных из БД на главную страницу веб-приложения.

## Установка 

Скачайте проект с github:
```
https://github.com/Stanis96/Learn-Python_Project
```

Создайте виртуальное окружение и установите зависимости:
```
pip install -r requirements.txt
```

Создайте файл `config.py` в директории \app и задайте в нем базовые переменные:
(скопируйте код ниже в `config.py`, подставив свои значения)
```
import os
basedir = os.path.abspath(os.path.dirname(__file__))

class Config:
    SECRET_KEY = os.environ.get('SECRET_KEY') or 'Ваше значение'
    SQLALCHEMY_DATABASE_URI = 'sqlite:///' + os.path.join(basedir, '..', 'headphones.db')
    SQLALCHEMY_TRACK_MODIFICATIONS = False
```

## Запуск программы

Для запуска программы на ОС Windows из коммандной строки запустите файл `run.bat`, произойдет запуск
сервера и выведет IP-адрес на экран. Для запуска программы на ОС Linux/MacOs, в корне проекта выполните 
в консоли команду `chmod +x run.sh` - это сделает файл исполняемым. Далее для запуска проекта нужно
 писать в корне проекта в консоле `./run.sh`.
```
- для ОС Windows: run.bat
- для ОС Linux/MacOs: ./run.sh
```