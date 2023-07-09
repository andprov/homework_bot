# Бот для проверки статуса домашней работы Яндекс.Практикум

python-telegram-bot 13.7
- [github](https://github.com/python-telegram-bot/python-telegram-bot)
- [homepage](https://python-telegram-bot.org)
- [wiki](https://github.com/python-telegram-bot/v13.x-wiki/wiki)

## Описание
Telegram-бот, который обращается к API сервиса Практикум.Домашка и возвращает статус
домашней работы.

Эндпоинт: https://practicum.yandex.ru/api/user_api/homework_statuses/

[Получить токен доступа](https://oauth.yandex.ru/authorize?response_type=token&client_id=1d0b9dd4d652455a9eb710d450ff456a)

## Функционал
- раз в 10 минут опрашивает API сервиса Практикум.Домашка и проверяет статус 
отправленной на ревью домашней работы;
- при обновлении статуса анализирует ответ API и отправляет соответствующее 
уведомление в Telegram;
- логирует свою работу и сообщает о проблемах в Telegram.


## Установка и запуск
**💡 Python3.9**

Клонировать репозиторий:
```
git clone <https or SSH URL>
```

Перейти в папку проекта:
```
cd homework_bot
```

Создать и активировать виртуальное окружение:
```
python3 -m venv venv
source venv/bin/activate
```

Обновить pip:
```
python3 -m pip install --upgrade pip
```

Установить библиотеки:
```
pip install -r requirements.txt
```

Создать файл .env с переменными окружения, со следующим содержанием:
```
BOT_TOKEN=<Токен бота>
ACCOUNT_SID=<ID чата>
PRACTICUM_TOKEN=<Токен доступа к API>
```

Запустить приложение:
```
python3 homework.py
```
