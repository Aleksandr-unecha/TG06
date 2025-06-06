# TG06
 
# Telegram-бот финансового помощника

## Описание
Telegram-бот для управления личными финансами, отслеживания курсов валют, получения советов по экономии и сохранения данных о расходах. Использует SQLite для хранения данных и API `exchangerate-api.com` для получения информации о курсах валют.

---

## Основные функции
1. **Регистрация**  
   Сохраняет данные пользователя (Telegram ID и имя) в базе данных.
2. **Курс валют**  
   Отображает актуальные курсы USD и EUR к RUB через API.
3. **Советы по экономии**  
   Предоставляет случайные советы для управления бюджетом.
4. **Личные финансы**  
   Позволяет вводить категории расходов и их суммы, сохраняя их в базе данных.

---

## Технологии
- [aiogram](https://github.com/aiogram/aiogram)  — фреймворк для работы с Telegram Bot API.
- [SQLite](https://www.sqlite.org/index.html)  — локальная база данных.
- [Requests](https://docs.python-requests.org/)  — для запросов к API.
- API: [exchangerate-api.com](https://exchangerate-api.com/). 

---

## Установка
1. **Создайте виртуальное окружение**:  
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows

## Установите зависимости :
   ```bash
   pip install aiogram requests
   ```

## Настройте конфигурацию :
Замените TOKEN в config.py на ваш токен Telegram-бота.
Замените API-ключ в строке url = "https://v6.exchangerate-api.com/v6/..." на ваш собственный.

## Создайте базу данных :
База данных user.db создастся автоматически при первом запуске бота.

## Запуск:
   ```bash
   python bot.py
   ```

## Использование
1. Регистрация :
   Нажмите кнопку "Регистрация в телеграм боте" для сохранения данных в системе.
2. Курс валют :
   Выберите "Курс валют", чтобы получить актуальную информацию о ценах на USD и EUR.
3. Советы по экономии :
   Кнопка "Советы по экономии" выдаст случайный совет.
4. Личные финансы :
   Введите три категории расходов (например, "Продукты", "Транспорт", "Развлечения") и соответствующие суммы. Данные сохранятся в базе данных.

## Примеры интерфейса
Привет! Я ваш личный финансовый помощник. Выберите одну из опций:
[Регистрация] [Курс валют]
[Советы]    [Личные финансы]

1 USD = 75.20 RUB
1 EUR = 89.50 RUB

Совет 1: Ведите бюджет и следите за своими расходами.

## Лицензия
MIT License
