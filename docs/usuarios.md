# Mock Data: Usuários

Este documento descreve a API de mock data para usuários.

## Tabela de Conteúdo

- [Mock Data: Usuários](#mock-data-usuários)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Usuários](#usuários)
    - [GET /usuarios](#get-usuarios)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /usuarios](#post-usuarios)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /usuarios/{id}](#put-usuariosid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /usuarios/{id}](#delete-usuariosid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Usuários

### GET /usuarios
Retorna uma lista de todos os usuários.

#### Exemplo de Resposta
```json
{
  "usuarios": [
    {
      "id": 1,
      "nome": "Admin",
      "email": "admin@example.com",
      "senha": "hashed_password_1",
      "tipo_usuario": [
        {
          "id": 1,
          "tipo": "admin"
        }
      ],
      "telefone_id": 1,
      "data_criacao": "2021-06-01T00:00:00Z",
      "data_atualizacao": "2021-06-01T00:00:00Z",
      "data_ultimo_login": "2021-06-01T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    },
    {
      "id": 2,
      "nome": "John Doe",
      "email": "johndoe@example.com",
      "senha": "hashed_password_2",
      "tipo_usuario": [
        {
          "id": 2,
          "tipo": "voluntario"
        }
      ],
      "telefone_id": 2,
      "data_criacao": "2022-01-15T00:00:00Z",
      "data_atualizacao": "2022-01-15T00:00:00Z",
      "data_ultimo_login": "2022-01-20T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    }
  ]
}
```

### POST /usuarios
Cria um novo usuário.

#### Parâmetros
- `nome` (string): Nome do usuário
- `email` (string): Email do usuário
- `senha` (string): Senha do usuário
- `tipo_usuario` (array): Array com objetos contendo ID e tipo de usuário
- `telefone_id` (int): ID do telefone
- `data_criacao` (string): Data de criação do usuário
- `data_atualizacao` (string): Data de atualização do usuário
- `data_ultimo_login` (string): Data do último login do usuário
- `status` (array): Array com objetos contendo ID e status do usuário

#### Exemplo de Requisição
```json
{
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status_usuario": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status_usuario": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

### PUT /usuarios/{id}
Atualiza um usuário.

#### Parâmetros
- `id` (int): ID do usuário
- `nome` (string): Nome do usuário
- `email` (string): Email do usuário
- `senha` (string): Senha do usuário
- `tipo_usuario` (array): Array com objetos contendo ID e tipo de usuário
- `telefone_id` (int): ID do telefone
- `data_criacao` (string): Data de criação do usuário
- `data_atualizacao` (string): Data de atualização do usuário
- `data_ultimo_login` (string): Data do último login do usuário
- `status` (array): Array com objetos contendo ID e status do usuário

#### Exemplo de Requisição
```json
{
  "nome": "Jane Smith Atualizado",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Jane Smith Atualizado",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

### DELETE /usuarios/{id}
Exclui um usuário.

#### Parâmetros
- `id` (int): ID do usuário

#### Exemplo de Resposta
```json
{
  "message": "Usuário excluído com sucesso"
}
```