# Health Service

Минимальный Go-сервис на Echo с health-check эндпоинтом.

## Запуск

### Docker

```bash
docker build -t health-service .
docker run -p 8080:8080 health-service
```

### Проверка

```bash
curl http://localhost:8080/health
# {"status":"OK"}
```

## Эндпоинты

| Метод | Путь      | Описание     | Ответ    |
|-------|-----------|--------------|----------|
| GET   | `/health` | Health check | `200 OK` |