# MyApp

Небольшое HTTP-приложение на Go с логированием запросов и поддержкой `X-Request-Id`.

## Запуск

Требуется Go 1.27 или новее.

```bash
go run ./cmd/myapp
```

Сервер будет доступен по адресу `http://localhost:8080`.

## Маршруты

- `GET /` — возвращает приветственное сообщение.
- `GET /ping` — возвращает JSON со статусом и текущим временем.
- `GET /fail` — возвращает пример ошибки `400 Bad Request`.

Пример проверки:

```bash
curl http://localhost:8080/ping
```

## Сборка

```bash
go build -o bin/myapp ./cmd/myapp
```
