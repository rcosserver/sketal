<p align="center">
    <img src="https://github.com/vk-brain/sketal/blob/master/nothing/title.png?raw=true" alt="vk-sketal logo"/>
</p>

## sketal

#### Немного о боте
- Бот работает на python3.6 и выше. Ниже не работает. Совсем. Это важно.
- Бот использует asyncio, aiohttp и т.д.

#### Инструкция
1. Скачать python версии 3.6 или выше и установить его (с возможностью работать с ним из командной строки)
```
Можно скачать Python3.6 с оф. сайта: https://www.python.org/downloads/
```

2. Установить модули для python с помощью pip (модуля python). Список модулей находится в requirements.txt
```
python -m pip install -r requirements.txt
```

3. Заполнить настройки в settings.py (заменить нужные поля и т.д.).  
   Как минимум необходимо ввести `api ключ сообщества` вконтакте.

4. Бота можно запустить следующим способом из командной строки (windows) или терминала (linux) и т.д.:
   ```
   python bot.py
   ```

#### Как запустить бота от лица пользователя?
```
USERS = (
        ("group", "ТОКЕН СООБЩЕСТВА",),
        ("user", "ЛОГИН ПОЛЬЗОВАТЕЛЯ", "ПАРОЛЬ ПОЛЬЗОВАТЕЛЯ",),
        ("user", "ТОКЕН ПОЛЬЗОВАТЕЛЯ",),
)
```
Пример возможного содержания переменной USERS. Если вам нужно использовать пользователя для бота - замените `("group", "API КЛЮЧ СООБЩЕСТВА",),` на `("user", "ЛОГИН ПОЛЬЗОВАТЕЛЯ", "ПАРОЛЬ ПОЛЬЗОВАТЕЛЯ",),`. Обратите внимание на запятые!

#### Замечания
- При использовании CommandPlugin помните, что команды сортируются в соответствии с количесвом пробелов в команде (от большего к меньшему)

- Если вам нужна база данных, но нет PostgreSQL или MySQL - вы можете ввести имя для бд `:memory:`, тогда база будет в памяти. Но! Это приведёт к понижению производительности бота и данные будут удалены после выключения бота.

#### Участники проекта:
- [Список участников (все молодцы!)](https://github.com/vk-brain/sketal/graphs/contributors)
- [Плагинчик](https://github.com/TumkasCor)

#### Философия
- Проект создан для тех, кто готов разобраться в том, что же тут происходит. Создание плагинов и их настройка - сложный процесс.
- Никакие плагины не должны менять код основных частей бота, чтобы было легко обновляться и менять какие-то базовые вещи (переписывать плагины легче, чем восстанавливать функционал после обновлений).
- Многие функции, примеры, возможности можно найти, изучая исходный код плагинов и файлы бота. Например: `tests.py`, `vk_special_methods.py`, `handler/base_plugin.py` и т.д.
- Тесты - это важно, интересно и полезно!

@michaelkrukov http://michaelkrukov.ru/
