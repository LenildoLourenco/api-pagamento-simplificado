# API Pagamento Simplificado

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

Este projeto é uma API construída usando **Java, Java Spring e H2 como banco de dados.**

A API foi desenvolvida para resolver o [PicPay Backend Challenge](https://github.com/PicPay/picpay-desafio-backend) usando Java Spring.

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/LenildoLourenco/api-pagamento-simplificado.git
```

2. Instale dependências com Maven

## Uso

1. Inicie a aplicação com Maven
2. A API estará acessível em http://localhost:8080


## API Endpoints
A API fornece os seguintes endpoints:

**GET USUÁRIOS**
```markdown
GET /users - Recuperar uma lista de todos os usuários.
```
```json
[
    {
        "id": 1,
        "firstName": "Gabriel",
        "lastName": "Silva",
        "document": "12345695223",
        "email": "gabriel@example.com",
        "password": "senha",
        "balance": 20.00,
        "userType": "MERCHANT"
    },
    {
        "id": 5,
        "firstName": "Pedro",
        "lastName": "Silva",
        "document": "12378965412",
        "email": "pedro@example.com",
        "password": "senha",
        "balance": 0.00,
        "userType": "COMMON"
    }
]
```

**POST USUÁRIOS**
```markdown
POST /users - Cadastre um novo usuário.
```
```json
{
    "firstName": "Bob",
    "lastName": "Silva",
    "password": "senha",
    "document": "12348523689",
    "email": "bob@example.com",
    "userType": "COMMON",
    "balance": 10
}
```

**POST TRANSAÇÕES**
```markdown
POST /transactions - Cadastrar uma nova transação entre usuários (COMMON para COMMON ou COMMON para MERCHANT).
```

```json

{
  "senderId": 5,
  "receiverId": 1,
  "value": 10
}
```

## Banco de Dados
O projeto utiliza [H2 Database](https://www.h2database.com/html/tutorial.html) como o banco de dados.




