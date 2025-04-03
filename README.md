# Тестовое задание для вакансии Frontend-разработчика

## Описание

Это тестовое задание для вакансии Frontend-разработчика. В рамках задания была выполнена страница для отображения сделок из системы amoCRM, с возможностью взаимодействия с API, отображения данных в таблице, а также получения и отображения развернутых данных по сделкам и контактам.

Основные задачи:

1. Сверстать страницу с таблицей сделок.
2. Получить данные из amoCRM по API и отобразить их на странице.
3. Обработать CORS-политику с использованием локального или внешнего прокси-сервера.
4. Реализовать функционал отображения статусов задач с использованием цветных кругов.
5. Добавить возможность развертывания карточек сделок с дополнительной информацией при нажатии.

## Структура проекта

- **index.html**: Основной HTML файл с разметкой страницы.
- **style.css**: Файл с кастомными стилями для страницы.
- **script.js**: Основной файл с логикой взаимодействия с API и отображением данных.
- **README.md**: Инструкция по запуску и использованию проекта.

## Инструкция по запуску

1. **Создание аккаунта в amoCRM**:

   - Зарегистрируйте аккаунт на [amoCRM](https://www.amocrm.ru/).
   - В разделе **амоМаркет** создайте "Внешнюю интеграцию" для получения доступа к API.
   - Получите **access_token** с использованием authorization_code. Подробнее в документации [amoCRM API](https://www.amocrm.ru/developers/).

2. **Запуск проекта**:

   - Скачайте проект.
   - Откройте файл `index.html` в браузере.
   - Для работы с API можно использовать локальный или внешний прокси-сервер для обхода CORS.

3. **Для обхода CORS можно использовать**:

--Локальный прокси-сервер

--Браузерное расширение для отключения CORS (например, "Allow CORS")

--Запуск с флагом --disable-web-security (В моем случае, пытался через proxy_url. Но там ограничение по запросам 429 ошибка)

4. **Параметры и настройки**:

   - Внесите ваш **access_token** в файл `script.js` в соответствующем месте, чтобы подключить API.
   - Убедитесь, что вы создали как минимум 6 сделок в amoCRM, как описано в подготовке.

5. **Проверка функциональности**:
   - На странице будут отображены сделки и связанные с ними контакты.
   - При клике на карточку сделки будет выполняться запрос для получения развернутых данных.
   - Статусы задач будут отображаться в виде цветных кругов:
     - **Красный**: задача просрочена (поставлена на вчера).
     - **Зеленый**: задача на сегодня.
     - **Желтый**: задача в будущем.

## Используемые технологии

- **HTML**: Для структуры страницы.
- **CSS**: Для стилизации страницы (с использованием Bootstrap).
- **JavaScript**: Для взаимодействия с API amoCRM и реализации логики на странице.
- **amoCRM API**: Для получения данных о сделках и контактах.

## Примечания

- Важно: API запросы ограничены до 2-х карточек в секунду для соблюдения лимитов amoCRM.
- В коде предусмотрен механизм для обработки CORS-политики.
- Для запуска проекта необходимо иметь доступ к аккаунту amoCRM и valid access_token.

## Ссылка на репозиторий

[Ссылка на репозиторий](https://gitlab.com/yogurtt771/EmfiTask)
