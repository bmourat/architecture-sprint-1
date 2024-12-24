# 1. Задание: Разбиение mesto на микрофронтенды

В качесте фреймворка микрофронтэндов будем использовать  Webpack Module Federation. Он позволяет независимым приложениям использовать общий код во время выполнения. Команды, которые разрабатывают разные микрофронтенды, смогут получить доступ к коду друг друга до развёртывания.

Честно говоря не очень понял чем он отличается от Single SPA, или других инструментов. Да и в материалах курса нет четкого ответа:

> Если смотреть глобально, между этими технологиями нет принципиальных различий. Нет универсального ответа, в какой проект какой фреймворк встанет лучше

Проанализировав текущее приложение решил выделить три отдельных микрофронтенда + галвное хост приложение:

    1. Авторизация/Регистрация
    2. Профиль пользователя (редактирование/отображение)
    3. Сервис ленты (отображение/добавление мест/учет лайков)
    4. Хост


После реорганизации кода по микрофронтендам получилась следующая структура компонентов:

1. Фронтенд `auth`
    - Логин
    - Регистрация
2. Фронтенд `profile`
    - Информация о пользователе
    - Изменение аватарки
    - Редактирование профиля
3. Фронтенд `place`
    - Список мест
    - Карточка конкретного места
    - Добавление места
    - Удаление места
4. Фронтенд `host`
    - Главная страница
    - Модуль навигации
    - Информационное окно
    - Хедер
    - Футер
