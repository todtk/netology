# Домашнее задание к лекции 8.«Работа с библиотекой requests, http-запросы»

## Задача №1
Кто самый умный супергерой?  
Есть [API по информации о супергероях](https://akabab.github.io/superhero-api/api/) с информацией по всем супергероям. 
Нужно определить кто самый умный(intelligence) из трех супергероев- Hulk, Captain America, Thanos.


## Задача №2
У Яндекс.Диска есть очень удобное и простое API. Для описания всех его методов существует [Полигон](https://yandex.ru/dev/disk/poligon/).
Нужно написать программу, которая принимает на вход путь до файла на компьютере и сохраняет на Яндекс.Диск с таким же именем.
1. Все ответы приходят в формате json;
2. Загрузка файла по ссылке происходит с помощью метода put и передачи туда данных;
3. Токен можно получить кликнув на полигоне на кнопку "Получить OAuth-токен".  

HOST: https://cloud-api.yandex.net:443

*Важно:* Токен публиковать в github не нужно, переменную для токена нужно оставить пустой! 

Шаблон для программы
```python
class YaUploader:
    def __init__(self, token: str):
        self.token = token

    def upload(self, file_path: str):
        """Метод загружает файлы по списку file_list на яндекс диск"""
        # Тут ваша логика
        # Функция может ничего не возвращать


if __name__ == '__main__':
    # Получить путь к загружаемому файлу и токен от пользователя
    path_to_file = ...
    token = ...
    uploader = YaUploader(token)
    result = uploader.upload(path_to_file)
```
## \*Задача №3(необязательная)
Самый важный сайт для программистов это [stackoverflow](https://stackoverflow.com/). И у него тоже есть [API](https://api.stackexchange.com/docs)
Нужно написать программу, которая выводит все вопросы за последние два дня и содержит тэг 'Python'.
Для этого задания токен не требуется.
---
## Материалы по теме.
Рекомендованные статьи на русском языке:
1. [Простой метапоисковый алгоритм на Python](https://habr.com/ru/articles/272711/)
2. [Grab — python библиотека для парсинга сайтов](https://habr.com/ru/articles/127584/)
3. [Узнаем текущую погоду и прогноз простеньким скриптом на Python'е](https://habr.com/ru/articles/315264/)
4. [Web Scraping с помощью python](https://habr.com/ru/articles/280238/)
5. [Разработка веб-скрапера для извлечения данных с портала открытых данных России data.gov.ru](https://habr.com/ru/articles/323202/)

Официальная документация:
1. [Extensible library for opening URLs](https://docs.python.org/3/library/urllib.request.html)
2. [Requests: HTTP for Humans](https://docs.python-requests.org/en/latest/)
