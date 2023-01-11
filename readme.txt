# WIP

### Roadmap:
- 🔴 Админ панель
  * ~~Категории~~
    - ~~Добавление~~
    - ~~Изменение~~
  * Товары
    - ~~Добавление~~ 
    - Изменение
  * ~~Пользователи~~
    - ~~Просмотр профиля~~
    - ~~Изменение ролей~~
  * Статистика
  * Настройки
- ~~🗄️ Каталог~~
- 🛒 Корзина
  * ~~Товары~~ 
  * ~~Доставка~~
  * Оформление заказа
- 📁 Профиль
- ~~ℹ️ FAQ~~
- Платежи
  * Вручную
  * Telegram API
  * Qiwi/yoomoney?
- Readme

<hr>

# 🇷🇺Russian
# Зачем и кому нужен этот бот?

Зачастую люди, желающие открыть маленький интернет-бизнес, делают это с помощью профиля в социальных сетях, что требует вручную обрабатывать каждую заявку. Этот бот позволит каждому быстро открыть автоматизированный магазин на базе телеграм бота, что значительно уменьшит время обработки заказов.

# Что есть в боте?
- Бот поддерживает оплату через платежные системы (Telegram API). 
- Админ панель для управления магазином
    - Добавление/изменение/удаление товара
    - Добавление/изменение/удаление категорий
    - Просмотр/изменение ролей пользователей
    - Настройка бота
    - Статистика по продажам с графиками и возможностью экспорта в Excel.
- Каталог товаров с категориями и подкатегориями
- Поиск по каталогу
- Корзина с возможностью выбора способа доставки и оплаты
- Личный кабинет с историей заказов
- FAQ с возможностью изменения вопросов и ответов через админ панель

# Как установить?

Бота можно установить двумя способами:
- [Docker(рекомендуется)](#docker)
- [Ручная установка](#manual)

## Docker

placeholder

## Manual
### Установка зависимостей

#### Python 3.10

Windows:
```powershell
scoop install python # или установить с официального сайта
```

Ubuntu:
```bash
sudo apt-get install python3.10 python3-pip
```

Fedora:
```bash
sudo dnf install python3.10 python3-pip
```

Arch:
```bash
sudo pacman -S python3.10 python3-pip
```

Gentoo:
```bash
sudo emerge -av dev-lang/python:3.10 dev-python/pip
```

#### Poetry
Linux/Macos/Windows(WSL):
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

Windows Powershell:
```powershell
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | py -
```

### Установка бота

#### Клонирование репозитория
```bash
git clone https://github.com/w1png/shop-telegram-bot
cd shop-telegram-bot
```

#### Создание .env файла
Linux/Macos:
```bash
touch .env
echo "TOKEN=токен" >> .env
```

Windows:
```powershell
New-Item -Path .env -ItemType File
@echo off
echo "TOKEN=токен" >> .env
```

#### Запуск бота
```bash 
poetry install # установка зависимостей и создание виртуального окружения
poetry run python3.10 src/__init__.py # запуск бота
```

