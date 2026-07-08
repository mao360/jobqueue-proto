# jobqueue-proto

Protobuf-контракты и сгенерированный Go-код для scheduler и worker.
Распространяется как Go-модуль через git-теги, без BSR.

## Сервисы

- `SchedulerService` — для клиентов: `CreateJob`, `GetJob`, `CancelJob` (unary), `WatchJob` (server stream), `SubmitBatch` (client stream)
- `WorkerGatewayService` — для воркеров: `Connect` (bidi)

## Команды

- Подключить: `go get github.com/mao360/jobqueue-proto@v0.2.0`
- Проверка: `buf lint`
- Генерация: `buf generate`

## CI

`buf lint`, `buf breaking` против `main` на PR, проверка актуальности `gen/`. Релизы — git-теги.