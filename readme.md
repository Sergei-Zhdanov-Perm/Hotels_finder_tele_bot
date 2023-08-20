<h1 align="center">Hotels_finder_tele_bot



***

## Краткое описание

Hotels_finder_tele_bot позволяет найти выгодное предложение на платформе [Hotels.com](https://hotels.com/).
<br> Пользователь с помощью специальных команд бота может выполнить следующие действия (получить следующую информацию): <br/>
1. Узнать топ самых дешёвых отелей в городе (команда /lowprice). 
2. Узнать топ самых дорогих отелей в городе (команда /highprice). 
3. Узнать топ отелей, наиболее подходящих по цене и расположению от центра (самые дешёвые и находятся ближе всего к центру) (команда /bestdeal). 
4. Узнать историю поиска отелей (команда /history) 


**Для разработки и функционирования проекта используется открытый API Hotels, который расположен на сайте [rapidapi.com](https://rapidapi.com/apidojo/api/hotels4/).**

***


### Запуск проекта (на Windows)

- Создайте на своем компютере папку проекта
- Создайте файл `.env` и добавьте в него переменные окружения, следующего вида:
<br>
    BOT_TOKEN= "ваш бот токен"<br>
    RAPID_API_KEY= "ваш rapid_api key"<br>
<br>
- Активируйте виртуальное окружение 
- Установите все зависимости библиотек из файла requirements.txt
- Запустите бота командой `python main.py` из Терминала из папки с проектом 

***

## Описание работы команд

### Команда /start

После ввода команды: 
1. Выводится приветствие пользователю

### Команда /help

После ввода команды: 
1. Выводится список всех команд, кратким описанием что делает каждая команда


### Команда /lowprice

После ввода команды у пользователя запрашивается: 
1. Город, где будет проводиться поиск
2. Выдается список возможных вариантов городов в виде inline-клавиатуры, пользователь выбирает нужный
3. Количество отелей, которые необходимо вывести в результате (не больше заранее определённого максимума)
4. Запрашиваются минимальная и максимальная стоимость отеля в долларах США
5. Необходимость загрузки и вывода фотографий для каждого отеля (“Да/Нет”). При положительном ответе пользователь также вводит количество необходимых фотографий (не больше заранее определённого максимума)
6. Выводится календарь с возможностью выбора даты заезда или выезда. 

### Команда /highprice 

После ввода команды у пользователя запрашивается: 
1. Город, где будет проводиться поиск
2. Выдается список возможных вариантов городов в виде inline-клавиатуры, пользователь выбирает нужный
3. Количество отелей, которые необходимо вывести в результате (не больше заранее определённого максимума)
4. Запрашиваются минимальная и максимальная стоимость отеля в долларах США
5. Необходимость загрузки и вывода фотографий для каждого отеля (“Да/Нет”). При положительном ответе пользователь также вводит количество необходимых фотографий (не больше заранее определённого максимума)
6. Выводится календарь с возможностью выбора даты заезда или выезда. 

### Команда /bestdeal

После ввода команды у пользователя запрашивается: 
1. Город, где будет проводиться поиск
2. Выдается список возможных вариантов городов в виде inline-клавиатуры, пользователь выбирает нужный
3. Количество отелей, которые необходимо вывести в результате (не больше заранее определённого максимума)
4. Запрашиваются минимальная и максимальная стоимость отеля в долларах США
5. Необходимость загрузки и вывода фотографий для каждого отеля (“Да/Нет”). При положительном ответе пользователь также вводит количество необходимых фотографий (не больше заранее определённого максимума)
6. Выводится календарь с возможностью выбора даты заезда или выезда. 
7. Диапазон расстояния, на котором находится отель от центра

### Команда /history

После ввода команды пользователю выводится история поиска отелей: 
1. Выдает список выполненных пользователем запросом, но не более 5
2. Дату и время ввода команды
3. То слово (город), по которому пользователь искал отели
4. Если пользователю фотографии были не нужны, то они выведены не будут


## Описание внешнего вида и UI
Окно Telegram-бота при запущенном Python-скрипте воспринимает следующие команды:
- /start - запуск бота
- /help — помощь по командам бота 
- /lowprice — вывод самых дешёвых отелей в городе
- /highprice — вывод самых дорогих отелей в городе 
- /bestdeal — вывод отелей, наиболее подходящих по цене и расположению от центра
- /history — вывод истории поиска отелей

Для команд lowprice, highprice и bestdeal сообщение с результатом содержит краткую информацию по каждому отелю. 
В эту информацию входит: 
- Название отеля
- Адрес
- Цена за ночь (в долларах США)
- Как далеко отель расположен от центра
- N фотографий отеля (если пользователь счёл необходимым их вывод)



## В разработке использованы

pyTelegramBotAPI==4.4.0<br>
python-dotenv==0.19.2<br>
pip~=21.1.2<br>
wheel~=0.36.2<br>
certifi~=2022.6.15<br>
requests~=2.28.1<br>
idna~=3.3<br>
urllib3~=1.26.11<br>
setuptools~=57.0.0<br>
loguru~=0.6.0<br>
