# Desafio Backend Jitterbit

API REST desenvolvida em **Node.js** com **Express** e **MongoDB** para gerenciamento de pedidos.

## Objetivo

O objetivo deste projeto é criar uma API simples para cadastrar, consultar, listar, atualizar e remover pedidos, realizando o mapeamento dos campos recebidos no body para o formato salvo no banco de dados.

## Tecnologias utilizadas

- Node.js
- Express
- MongoDB Atlas
- Mongoose
- Dotenv
- Nodemon

## Estrutura do projeto

```bash
desafio-backend-jitterbit/
├── config/
│   └── database.js
├── controllers/
│   └── orderController.js
├── models/
│   └── orderModel.js
├── routes/
│   └── orderRoutes.js
├── .gitignore
├── app.js
├── package-lock.json
├── package.json
└── README.md
Como executar o projeto

# 1. Instalar as dependências

npm install

# 2. Criar o arquivo .env

PORT=3000
MONGO_URI=sua_string_de_conexao_com_o_mongodb

# 3. Executar o projeto

npm run dev

## Endpoints

POST /order
GET /order/:id
GET /order/list
PUT /order/:id
DELETE /order/:id

Mapping dos dados

A API recebe:
{
  "numeroPedido": "v10089016vdb",
  "valorTotal": 10000,
  "dataCriacao": "2023-07-19T12:24:11.5299601+00:00",
  "items": [
    {
      "idItem": "2434",
      "quantidadeItem": 1,
      "valorItem": 1000
    }
  ]
}






