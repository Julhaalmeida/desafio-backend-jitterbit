# Desafio Backend - 

Este projeto consiste em uma **API REST**. A aplicação foi construída para gerenciar o ciclo de vida de pedidos (Orders), permitindo operações de CRUD (Create, Read, Update, Delete) com persistência em banco de dados NoSQL.

---

## Tecnologias e Arquitetura

O projeto foi estruturado utilizando o padrão de arquitetura **MVC** (Models, Controllers, Routes), garantindo uma manutenção simplificada e organização profissional do código:

* **Node.js**: Ambiente de execução Javascript Server-side.
* **Express**: Framework para gerenciamento de rotas e requisições HTTP.
* **MongoDB & Mongoose**: Banco de dados NoSQL e biblioteca de modelagem de dados.
* **Dotenv**: Gerenciamento seguro de variáveis de ambiente.

---

## Estrutura do Projeto

```text
├── config/          # Configuração da conexão com o Banco de Dados (MongoDB)
├── controllers/     # Lógica de negócio e tratamento das requisições
├── models/          # Definição dos Schemas e modelos de dados
├── routes/          # Definição dos endpoints e roteamento da API
├── .gitignore       # Arquivos ignorados pelo controle de versão (ex: node_modules, .env)
├── app.js           # Arquivo principal de inicialização do servidor
├── package.json     # Gerenciamento de dependências e scripts do projeto
└── README.md        # Documentação do repositório

## Como Executar o Projeto
Clone o repositório ou baixe os arquivos.

## Instale as dependências necessárias:
npm install

**Configure as variáveis de ambiente:**
Crie um arquivo .env na raiz do projeto e adicione suas credenciais conforme o exemplo abaixo:
PORT=3000
MONGO_URI=sua_string_de_conexao_com_o_mongodb

## Inicie a aplicação em modo de desenvolvimento:
npm run dev

## Endpoints da API
Abaixo estão as rotas disponíveis para interação com o sistema de pedidos:

Método	Endpoint	Descrição
POST	/order	Cria um novo pedido no banco de dados
GET	/order/list	Retorna a lista completa de pedidos cadastrados
GET	/order/:id	Busca os detalhes de um pedido através do seu ID
PUT	/order/:id	Atualiza os dados de um pedido existente
DELETE	/order/:id	Remove um pedido permanentemente do sistema

## Exemplo de Payload (JSON)
Para realizar requisições de criação ou atualização, utilize o seguinte formato no corpo da mensagem:

{
  "numeroPedido": "v10089016vdb",
  "valorTotal": 10000,
  "dataCriacao": "2023-07-19T12:24:11.529Z",
  "items": [
    {
      "idItem": "2434",
      "quantidadeItem": 1,
      "valorItem": 1000
    }
  ]
}
