# Chamadas de teste via cURL

> Use estas chamadas apenas para validar rapidamente. Para a entrega oficial, use o Postman e tire os prints solicitados.

```bash
curl -X POST http://localhost:8080/clientes \
  -H "Content-Type: application/json" \
  -d '{"nome":"AbinadabeOliveira0000000","clienteDesde":"2026-05-12"}'
```

```bash
curl -X POST http://localhost:8080/produtos \
  -H "Content-Type: application/json" \
  -d '{"nome":"Baozi de Carne Suína","preco":12.90,"estoque":true}'
```

```bash
curl -X POST http://localhost:8080/pedidos \
  -H "Content-Type: application/json" \
  -d '{"clienteId":1,"produtoId":1,"quantidade":3}'
```

```bash
curl http://localhost:8080/clientes
curl http://localhost:8080/produtos
curl http://localhost:8080/pedidos
curl http://localhost:8080/clientes/1
curl http://localhost:8080/produtos/1
curl http://localhost:8080/pedidos/1
curl -X DELETE http://localhost:8080/pedidos/1
```
