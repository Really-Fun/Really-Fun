## Привет, я Илья (ReallyFun) 👋

Python-разработчик, студент 2 курса КФУ (ИВМиИТ, прикладная математика и информатика), Казань.
Пишу на Python и asyncio, интересуюсь бэкендом и архитектурой. **Ищу стажировку или junior-позицию Python backend**, готов к удалёнке.

<p>
  <img src="https://img.shields.io/badge/Python-3.13+-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/asyncio-✓-3776AB?style=flat-square" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-Arch-1793D1?style=flat-square&logo=arch-linux&logoColor=white" />
</p>

---

### 🛠️ Главный проект: [Quantis](https://github.com/Really-Fun/Quantis)

Open-source десктопный плеер-агрегатор: Яндекс.Музыка, YouTube и SoundCloud в одном приложении. Я автор и мейнтейнер.

- **Стек:** Python 3.13, PySide6, asyncio, aiohttp, aiosqlite, Poetry
- **Архитектура:** слои UI (MVVM) → контроллеры → сервисы → провайдеры; зависимости собираются в composition root и передаются через конструкторы; компоненты общаются через EventBus; мост между event loop asyncio и Qt
- **Плагины:** сторонний `.zip` с манифестом подписывается на события плеера и может добавить свою страницу в интерфейс
- **Качество:** ~360 тестов на pytest, ruff, black и mypy; всё это гоняет CI на каждый PR; документация по [архитектуре](https://github.com/Really-Fun/Quantis/blob/main/docs/architecture.md)
- **Размер:** ~28k строк, сборка установщика под Windows, Android-клиент в разработке ([QuantisAndroid](https://github.com/Really-Fun/QuantisAndroid))

### 🌐 [QuantisSite](https://github.com/Really-Fun/QuantisSite): бэкенд и сайт для Quantis

Сайт проекта с каталогом плагинов, новостями релизов и комнатами совместного прослушивания: участники комнаты слышат один и тот же трек, синхронно ставят паузу и общаются в чате. Подключаются и из браузера, и из десктопного клиента Quantis.

- **Стек:** Django, Django Channels, Daphne (ASGI), PostgreSQL, Redis, Docker Compose, nginx
- **Реальное время:** WebSocket-комнаты на Channels; рассылка событий между воркерами через Redis channel layer; список онлайн-участников хранится в Redis
- **Доступ:** авторизация по сессии, комнаты с паролем (хешируется как пароль пользователя), проверка Origin с отдельным режимом для нативного клиента
- **Инфраструктура:** многоступенчатый Dockerfile, процесс работает не от root; Postgres и Redis во внутренней сети, у всех сервисов healthcheck; nginx с TLS, ограничением частоты запросов на логин, CSP и HSTS; файлы плагинов отдаются через `X-Accel-Redirect`
- **Конфигурация:** настройки через `.env`; в проде приложение не запустится без `SECRET_KEY`, `ALLOWED_HOSTS` и пароля БД; локально работает на SQLite и in-memory каналах

### 📂 Другие проекты

| Проект | Что это | Стек |
| :--- | :--- | :--- |
| [MindTracker](https://github.com/Really-Fun/MindTracker) | Веб-приложение на Django | Django, HTML |
| [EgeBot](https://github.com/Really-Fun/EgeBot) | Telegram-бот для подготовки к ЕГЭ (командный проект) | Python, aiogram |
| [TestTask](https://github.com/Really-Fun/TestTask) | Тестовое задание: новостной бот | Python |

### 🌍 Open source

- [MarshalX/yandex-music-api#677](https://github.com/MarshalX/yandex-music-api/pull/677): исправление по issue #673
- [wger-project/wger#2251](https://github.com/wger-project/wger/pull/2251): правки русской локализации

---

### 🎯 Цели на ближайшее время

- [ ] Попасть в команду бэкенд-разработки стажёром или джуном
- [ ] Сделать публичный бэкенд-сервис на FastAPI + PostgreSQL + Docker с тестами и CI
- [ ] Сделать содержательный вклад в асинхронную open-source библиотеку
- [ ] Разобраться с Kubernetes на практике

---

### 🧠 Алгоритмы

<a href="https://www.codewars.com/users/Rillifan"><img src="https://www.codewars.com/users/Rillifan/badges/large" alt="Codewars Badge" /></a>

<details>
<summary>📚 Курсы на Stepik</summary>

| Курс | Сертификат |
| :--- | :--- |
| [«Поколение Python»: для продвинутых](https://stepik.org/course/68343) | [🏆](https://stepik.org/cert/2122005) |
| [ООП на Python](https://stepik.org/course/98974) | [🏆](https://stepik.org/cert/2147870) |
| [Django](https://stepik.org/course/183363) | [🏆](https://stepik.org/cert/2526419) |
| [Selenium](https://stepik.org/course/188355) | [🏆](https://stepik.org/cert/2533804) |
| Инди-курс по Python | [🏆](https://stepik.org/cert/2128099) |

</details>

<picture>
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Really-Fun/Really-Fun/output/github-contribution-grid-snake-dark.svg">
</picture>

---

### 📬 Контакты

[![Telegram](https://img.shields.io/badge/Telegram-@ReallyFun1-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/ReallyFun1)
[![Email](https://img.shields.io/badge/Email-ilyareztcov%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ilyareztcov@gmail.com)
[![Habr Career](https://img.shields.io/badge/Хабр_Карьера-reallyfun-6C8CD5?style=flat-square)](https://career.habr.com/reallyfun)
