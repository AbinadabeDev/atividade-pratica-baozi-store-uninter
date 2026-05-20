# Guia de finalização da atividade - Baozi Store API

Este guia mostra exatamente o que ainda precisa ser feito na sua máquina antes de enviar a atividade.

## 1. Abrir o projeto na IDE

### IntelliJ IDEA
1. Abra o IntelliJ.
2. Clique em **File > Open**.
3. Selecione a pasta `baozi-store-api`.
4. Aguarde o Maven baixar as dependências.
5. Verifique se o projeto está usando **Java 17 ou superior**.
6. Execute a classe:

```text
src/main/java/br/com/uninter/baozistore/BaoziStoreApiApplication.java
```

### Terminal

Dentro da pasta do projeto:

```bash
mvn spring-boot:run
```

A API deve subir em:

```text
http://localhost:8080
```

## 2. Testar o banco H2

Acesse no navegador:

```text
http://localhost:8080/h2-console
```

Preencha:

```text
JDBC URL: jdbc:h2:mem:baozidb
User: sa
Password: deixe em branco
```

## 3. Importar a collection no Postman

1. Abra o Postman.
2. Clique em **Import**.
3. Selecione o arquivo `Baozi_Store_Postman_Collection.json`.
4. Abra a collection **Baozi Store API - Atividade Pratica**.
5. Antes de rodar, substitua a variável `clienteNome` pelo seu nome seguido do RU real.

Exemplo:

```text
AbinadabeOliveira1234567
```

## 4. Ordem recomendada dos prints

Tire prints mostrando método HTTP, URL, body JSON e retorno da API.

1. POST `/clientes` - Criar Cliente
2. POST `/produtos` - Criar Produto
3. POST `/pedidos` - Criar Pedido
4. GET `/clientes` - Listagem geral
5. GET `/produtos` - Listagem geral
6. GET `/pedidos` - Listagem geral
7. GET `/clientes/{id}` - Consulta por ID
8. GET `/produtos/{id}` - Consulta por ID
9. GET `/pedidos/{id}` - Consulta por ID
10. DELETE `/pedidos/{id}` - Apagar Pedido
11. DELETE `/produtos/{id}` - Apagar Produto
12. DELETE `/clientes/{id}` - Apagar Cliente

Atenção: delete primeiro o pedido, depois o produto e depois o cliente, porque o pedido possui relacionamento com cliente e produto.

## 5. Atualizar o documento final

No arquivo `Baozi_Store_Atividade_Pratica.docx`:

1. Troque `RU: 0000000` pelo seu RU real.
2. Troque `Sua cidade - Seu estado` pelos dados reais.
3. Na seção 4, substitua os quadros pelos prints reais do Postman.
4. Na seção 5, cole o link do repositório GitHub.
5. Exporte o documento para PDF.

## 6. Subir para o GitHub

Dentro da pasta do projeto:

```bash
git init
git add .
git commit -m "feat: implementa API REST da Baozi Store"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/baozi-store-api.git
git push -u origin main
```

Depois, copie o link do repositório e cole na seção 5 do documento.
