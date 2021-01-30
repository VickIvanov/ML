# Документация
Документация к `R-Vision Assistant` - аналитическому сервису по мониторингу угроз кибербезопасности, разработанной на хакатоне «Hack.Genesis», заказчик решения - R-Vision.

#### [**Ссылка на Прототип проекта**](https://rvision-stellar.web.app/)

# Вступление и описание решения

Система `R-Vision Assistant` является прототипом аналитического сервиса по мониторингу угроз кибербезопасности для полноценной помощи специалистам по ИБ.

Проект `R-vision Assistant` - cервис для сбора, визуализации и аналитики данных по угрозам кибербезопасности.

- Выводит оперативный дашборд специалиста по ИБ, дает наглядную картину в любой момент - "что нового/вообще происходит в мире и в его сети сейчас"

- Отображает подробную аналитику по событиям кибербезопасности за предыдущие периоды - в удобном и наглядном интерфейсе

- Позволяет отследить текущие тренды по угрозам, увидеть различные срезы и фильтры по событиям, сделать выводы и применить их в своей работе

Уникальностью решения является не только удобный и понятный UX/UI-интерфейс, но и возможность работы с большим количество источников о киберугрозах, а также возможность добавления новых. Кроме этого - удобный и наглядный интерфей и большое количество вариантов визуализации и аналитических инструментов.

Стек проекта: `NextJS`, `TypeScript`, `React`, `PostgreSQL`, `Mongo`, `Python`, `NLP Services`, `Docker`.

У нас есть [***рабочая MVP-версия (минимально работоспособная версия продукта)***](https://rvision-stellar.web.app/), которая не только обладает удобным интерфейсом, но достаточным функционалом, чтобы продемонстрировать основные аспекты решения задачи кейса. Мы запустили ее на [внешнем сервере](https://rvision-stellar.web.app/).

Спасибо организаторам за интересную задачу, мы будем рады продолжить сотрудничество!

# Техническое описание проекта
## Установка
Т.к. в проекте используется микросервисная архитектура, большая часть сервисов доступна для скачивания в виде контейнеров.

Для локального развертывания решения необходимо авторизоваться в GitHub Package Registry [по инструкции](https://docs.github.com/en/free-pro-team@latest/packages/using-github-packages-with-your-projects-ecosystem/configuring-docker-for-use-with-github-packages#authenticating-to-github-packages) и в корне проекта выполнить команду `docker-compose up --build`

Важно, что у вас должен быть установлен и запущен `Docker`.

> После того, как установка всех необходимых зависимостей будет выполнена, вы сможете потестировать систему локально по ссылке http://localhost/

## Структура
Проект представляет собой монорепозиторий с прилинкованным субрепозиторием для Frontend (ссылка на папку `frontend-service @ 881641e`).
Исходный код серверной backend-части — в папке `backend-service`, исходный код ML-моделей на Python — в виде отдельного микросервиса в папке `data-service`.

Каждая директория по возможности содержит файл `Makefile` с базовыми командами.

## Архитектура приложения
Приложение состоит из микро-сервисов, включая сервис авторизации, сервис моделей, сервис-ui и  т.д. 
ML модели размещены отдельно и запускаются в docker-контейнерах в требуемом окружении.

# Дополнительные материалы

- [**Прототип проекта, т.е. рабочая MVP-версия (минимально работоспособная версия продукта)**](https://rvision-stellar.web.app/).
- [Предварительная дорожная карта и смета](https://docs.google.com/spreadsheets/d/1UB8UeQOZ4nmgI7dRckGbxiV1xdOJTnLcRfTKUTH4xAA/edit?usp=sharing) общих затрат по разработке и внедрению на архитектуре заказчика для пилотной версии проекта.
