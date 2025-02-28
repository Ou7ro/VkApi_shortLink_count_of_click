# VkApi_shortLink_count_of_click
Скрипт принимает через консоль URI и с помощью vk.api `utils.getShortLink` возвращает сокращенный вариант.

Если введенная вами ссылка отформатирована и имеет сокращенный формат (с помощью utils.getShortLink) - выведет в консоль число переходов по ней.

## Зависимости

- Python3 должен быть уже установлен
- Затем используйте `pip` для установки зависимостей:
```pycon
pip install -r requirements.txt
```

### Переменные окружения

- VK_API_TOKEN

1. Расположите файл `Token.env` в корневой папке репозитория рядом с файлом `main.py`.
2. `Token.env` должен содержать сервисный ключ доступа для отправки запросов в vk.API.

Пример содержимого `Token.env`:
```
VK_API_TOKEN=0l9ehcnt1i9wz0ab6eltbue8ndqxsa4xv1b4a5cedab68182bb53a8
```

#### Получение

Как получить сервисный ключ, подробнее по ссылке: [сервисный ключ доступа API VK](https://dev.vk.com/ru/mini-apps/settings/development/keys#Сервисный%20ключ)

## Запуск

- Для получения сокращенного варианта ссылки запустите скрипт следующей консольной командой:
```pycon
python main.py https://www.example.com
```

`https://www.example.com` - ссылка, которую нужно сократить
p.s. Работает как c HTTP, так и с HTTPS протоколами.

Пример вывода в консоль:
```pycon
https://vk.cc/XXXXXX
```

- Для получения статистике о количестве переходов, используется ссылка, пройденная через vk.api utils.getLinkStats.

- Для получения информации о колличестве переходов по ссылке, запустите скрипт следующей консольной командой:
```pycon
python main.py https://vk.cc/XXXXXX
```

где `https://vk.cc/XXXXXX` - сокращенная ссылка

Пример вывода в консоль:
```pycon
Количество переходов по ссылке: 18
```
