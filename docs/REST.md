# API-документация

## Использование OpenAPI

Во всех микросервисах используется спецификация **OpenAPI** (совместимая с Swagger / ReDoc) для описания REST API.

Документация пишется в формате `YAML` или `JSON`, и должна удовлетворять стандартам указанных ниже.

В `каждом` репозитории должна быть папка docs с openapi документацией:

```
/your-service
│
├── docs/
│ └── openapi.yaml
└── ...
```

*Это позволяет централизованно просматривать и валидировать API всех сервисов, а также генерировать SDK/клиенты.*

## Формат ответов API

Все REST API возвращают данные в следующей структуре(внутри body):

```
{
  "code": "string",      // Код состояния операции (например, OK, SERVER_ERROR)
  "result": object|null, // Полезная нагрузка данных
  "error": "string|null" // Сообщение об ошибке (при наличии)
}
```

Пример успешного ответа:
```json
{
  "code": "OK",
  "result": {
    "tokenId": "e03232b1-926a-4816-8e93-e23a3ecf7836",
    "expiresAt": 1751887797,
    "refreshExpiresAt": 1751970597
  }
}
```

Пример ответа с ошибкой:
```json
{
  "code": "SERVER_ERROR",
  "result": null,
  "error": "Failed to store token"
}
```

## Нэйминг
| Тип элемента        | Формат         | Примеры                           |
| ------------------- | -------------- | --------------------------------- |
| **Поля JSON**       | `camelCase`    | `tokenId`, `expiresAt`, `isAdmin` |
| **Идентификаторы**  | UUID, `*Id`    | `userId`, `orderId`               |
| **Дата и время**    | UNIX timestamp | `createdAt`, `expiresAt`          |
| **Булевы значения** | `is*`, `has*`  | `isActive`, `hasAccess`           |


## REST-эндпоинты

- Используются методы: GET, POST, PUT, PATCH, DELETE

- Формат URL — kebab-case (единообразно внутри сервиса)

Примеры:

```
POST /token

GET /users/{id}

DELETE /orders/{orderId}
```
