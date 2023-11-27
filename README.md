# Интеграция Bitrix24 с сервисом HeadHunter 

## Описание проекта
Проект представляет собой частичную синхронизацию популярного сервиса для поиска сотрудников и вакансий с одной из известных crm систем - Bitrix24.
Основная задача - дублировать отклики по вакансиям напрямую в Bitrix24.

## Как работает?
При запуске приложение проверяет авторизацию на портале Bitrix24(наличие адреса портала в базе данных). В случае отсутствия, авторизация происходит по техногологии <a href="https://dev.1c-bitrix.ru/learning/course/index.php?COURSE_ID=99&LESSON_ID=2486"> Полный протокол OAuth 2.0 </a>.Полученные на стороне front-end код авторизации и адрес портала отправляются на back, где авторизация в Bitrix24 завершается.
Затем приложение с некоторой периодичностью проверяет авторизацию в HeadHunter, в случае отрицательного ответа отображает кнопку для возможности войти. После чего, если пользователь обладает необходимыми правами(права пользователя в Bitrix24 накладываются поверх прав, выданных приложению) подгружается таблица с названиями вакансий и возможными настройками. Основные настройки предполагают, что пользователь укажет:
- **по каким вакансиям переносить отклики(Активность)**
- **кто будет назанчен ответственным за созданную сделку(Ответственный)**
- **создавать ли комментарий, сжатая информация из всего резюме, помещаемая в одно поле(Комментарий)**
- **в какую воронку упадет новый отклик(Воронки)**


Также можно выбрать только необходимую информацию из отлика, сопоставив ее с соответствующими полями в Bitrix24
- **сопоставление полей(Настройки)**

## Галерея

![Изображение 1](https://github.com/tyrypic/integration-headhunter/blob/main/screen1.png)
![Изображение 1](https://github.com/tyrypic/integration-headhunter/blob/main/screen2.png)
...

## Моя роль в проекте
Опишите, какие были ваши обязанности, ответственности и вклад в проект.

## Технологии, используемые в проекте
- Технология 1 (например, React.js)
- Технология 2 (например, Node.js)
- ...

## Принципы и инструменты разработки
- Код-стиль и форматирование: Prettier
- Линтер: ESLint (с конкретными правилами, если необходимо уточнить)
- Система контроля версий: Git (с применением GitFlow или другой стратегии, если применимо)
- Прочие инструменты: (например, Webpack, Babel, etc.)

## Команда
- Общее количество человек: X
- Роли в команде:
  - Разработчиков: Y
  - Дизайнеров: Z
  - QA: A
  - ...

## Основные достижения и результаты
Опишите, какие ключевые моменты и достижения были получены в ходе работы над проектом.

## Особые вызовы и преодоленные препятствия
Расскажите о трудностях, с которыми столкнулись в процессе разработки, и как их преодолели.

## Ссылки
- Демо проекта: [ссылка на демо-версию или рабочий продукт]
- Код проекта: [ссылка на репозиторий, если есть возможность поделиться]

## Отзывы и обратная связь
Если есть отзывы от клиентов, коллег или других стейкхолдеров о вашей работе над проектом, это отличное место, чтобы их разместить.
