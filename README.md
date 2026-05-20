# Baozi Store API

API REST simples desenvolvida em Java com Spring Boot, Spring Data JPA e banco relacional H2 para a atividade prática de Desenvolvimento Web Back-End.

## Tecnologias

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database
- Maven
- Postman

## Como executar

```bash
mvn spring-boot:run
```

A API ficará disponível em:

```text
http://localhost:8080
```

Console do H2:

```text
http://localhost:8080/h2-console
```

Configurações do H2:

```text
JDBC URL: jdbc:h2:mem:baozidb
User: sa
Password: deixe em branco
```

## Endpoints

### Clientes

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/clientes` | Cria cliente |
| GET | `/clientes` | Lista clientes |
| GET | `/clientes/{id}` | Consulta cliente por ID |
| PUT | `/clientes/{id}` | Atualiza cliente |
| DELETE | `/clientes/{id}` | Apaga cliente |

Exemplo de criação:

```json
{
  "nome": "AbinadabeOliveira0000000",
  "clienteDesde": "2026-05-12"
}
```

### Produtos

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/produtos` | Cria produto |
| GET | `/produtos` | Lista produtos |
| GET | `/produtos/{id}` | Consulta produto por ID |
| PUT | `/produtos/{id}` | Atualiza produto |
| DELETE | `/produtos/{id}` | Apaga produto |

Exemplo de criação:

```json
{
  "nome": "Baozi de Carne Suína",
  "preco": 12.90,
  "estoque": true
}
```

### Pedidos

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/pedidos` | Cria pedido |
| GET | `/pedidos` | Lista pedidos |
| GET | `/pedidos/{id}` | Consulta pedido por ID |
| PUT | `/pedidos/{id}` | Atualiza pedido |
| DELETE | `/pedidos/{id}` | Apaga pedido |

Exemplo de criação:

```json
{
  "clienteId": 1,
  "produtoId": 1,
  "quantidade": 3
}
```
