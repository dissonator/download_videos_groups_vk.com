# Скрипт для загрузки списка видео файлов со страницы группы или пользователя социальной сети Вконтакте

Процес работы:

1. Скрипт получает список видео файлов со страницы видеозаписей (вкладка Добавленные) группы или пользователя социальной сети Вконтакте

2. Если видео размещено на сервере VK.com, то происходит парсинг ссылки (BeautifulSoup) для скачавания и собственно сама загрузка файла. Файл помещается в ту же директорию от куда скрипт был запущен.

3. Если видео размещено на Youtube.com, то парсинг и загрузка производятся с использованием https://github.com/nficano/pytube

4. Для работы неободимо создать тестовое приложение https://vk.com/apps?act=manage и получить токен https://vk.com/dev/first_guide
Пример запроса:
https://oauth.vk.com/authorize?client_id=...вашId...&display=page&redirect_uri=https://oauth.vk.com/blank.html&scope=video,photos&response_type=token&v=5.52