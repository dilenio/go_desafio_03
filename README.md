# Desafio 3 - Clean Architecture

Para rodar essa aplicação siga os seguintes passos:

1. Na pasta `/cmd/ordersystem` tem um arquivo `.env` com as variaveis de ambiente.

2. Para subir o banco de dados mysql

```
docker-compose up -d
```

3. Para rodar as migrations no banco de dados

```
migrate -path=sql/migrations -database="mysql://root:root@tcp(localhost:3306)/orders" -verbose up
```

4. Usando webserver: Na pasta api existem dois arquivos http para fazer as chamadas create_order e list_orders.
5. Usando grpc: Rode o comando abaixo e dentro dele use `call CreateOrder` ou `call ListOrders`

```
evans -r repl
```

6. Usando Graphql: No browser abra o endereço abaixo

```
http://localhost:8080
```
