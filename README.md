# API-de-games

## Endpoints
### GET /games
Esse endpoint é responsavel por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.
Exemplo de resposta:
```
[
    {
        "id": 23,
        "title": "Call of Duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 2,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2323,
        "title": "Teste",
        "price": "679",
        "year": "5555"
    }
]
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido, Token expirado.

Exemplo de resposta:
```
{
  "err": "Token inválido!"
}
```

### POST /auth
Esse endpoint é responsavel por fazer o processo de login.
#### Parametros
email: E-mail do usuario cadastrado no sistema.

password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail.

Exemplo:
```
{
    "email": "contato@gabrielbastiani.com.br",
    "password": "nodejs<3"
}
```
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.
Exemplo de resposta:
```
[
    {
        "id": 23,
        "title": "Call of Duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 2,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2323,
        "title": "Teste",
        "price": "679",
        "year": "5555"
    }
]
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Senha ou e-mail incorretos.

Exemplo de resposta:
```
{
  "err": "Credenciais inválidas!"
}
```
