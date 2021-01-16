# O2K-Manager 

- `cmd` - main.go файл для сбора бинарника
- `internal` - вся логика приложения (в Go пакеты internal не экспортируемы, подробнее https://golang.org/doc/go1.4#internalpackages)
- `schema` - пакет для .sql файлов 

### internal

- `repository` - слой репозитория, логика работы с БД
- `service` - слой для бизнес-логики, использует зависимости со слоя `repository` но ничего не знает про `transport`
- `transport` - слой работы с транспортными протоколами (HTTP, gRPC) 

