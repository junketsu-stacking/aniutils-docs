# <img align="left" src="./assets/logo.png"> AniUtils

> **AnimeUtils** — мультисервисный REST API и UI для синхронизации списков аниме и манги между популярными сервисами, такими как: Shikimori, AniList, Remanga и MyAnimeList

---

## О проекте

AnimeUtils позволяет:
- Синхронизировать данные между платформами
- Авторизоваться через внешние сервисы (OAuth2)
- Импортировать и экспортировать списки
- Использовать единый веб-интерфейс


---

## Сервисы

| Сервис | Стек                          | Описание                 |
|--------|-------------------------------|--------------------------|
| **Frontend** | ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=000) ![](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=black)  | UI-интерфейс пользователя (OAuth2) |
| **Backend API** | ![](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white) ![](https://img.shields.io/badge/-FastAPI-009688?logo=fastapi&logoColor=white) ![](https://img.shields.io/badge/-Kafka-231F20?logo=apache-kafka&logoColor=white) ![](https://img.shields.io/badge/-PostgreSQL-336791?logo=postgresql&logoColor=white)    | Работа с пользователем в нашей системе |
| **Shikimori API Service** | ![](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white) ![](https://img.shields.io/badge/-Flask-000000?logo=flask&logoColor=white)     | Интеграция с Shikimori (GraphQL) |
| **AniList API Service** | ![](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![](https://img.shields.io/badge/-.NET%208.0-blueviolet?logo=dotnet)              | Интеграция с AniList (GraphQL) |
| **MAL API Service** | ![](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![](https://img.shields.io/badge/-.NET%208.0-blueviolet?logo=dotnet) | Интеграция с MyAnimeList    |
| **Remanga API Service** | ![](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)            | Интеграция с Remanga (главы, истории) |
| **Access Controller** | ![](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white) ![](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white)     | Генерация и валидация токенов |
| **Anime Syncer** | ![Go](https://img.shields.io/badge/Go-%2300ADD8.svg?&logo=go&logoColor=white) ![](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white) | Асинхронная синхронизация данных |
| **Remanga Job** | ![](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white) ![](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white) ![](https://img.shields.io/badge/-MongoDB-47A248?logo=mongodb&logoColor=white) | Джобы на прочтения манги |

---

## Архитектура микросервисов

<img src="./assets/junketsu.png" alt="Architecture diagram" width="100%">

---

## Безопасность

- JWT токены
- OAuth2 авторизация
- Все соединения через HTTPS
- Хеширование чувствительных данных

---

## Вклад

Мы открыты к любому вкладу!  
Присоединяйтесь к разработке после прочтения [правил участия](./CONTRIBUTING.md).

---

## Лицензия

MIT License © [Junketsu Team](https://github.com/junketsu-stacking)

---
