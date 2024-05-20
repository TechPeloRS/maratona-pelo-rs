# Mock Data: Status Usuário

Este documento descreve a API de mock data para status de usuários.

## Tabela de Conteúdo

- [Mock Data: Status Usuário](#mock-data-status-usuário)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Status de Usuários](#status-de-usuários)
    - [GET /status\_usuarios](#get-status_usuarios)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /status\_usuarios](#post-status_usuarios)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [PUT /status\_usuarios/{id}](#put-status_usuariosid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Requisição](#exemplo-de-requisição-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)
    - [DELETE /status\_usuarios/{id}](#delete-status_usuariosid)
      - [Parâmetros](#parâmetros-3)
      - [Exemplo de Resposta](#exemplo-de-resposta-4)

## Status de Usuários

### GET /status_usuarios
Retorna uma lista de todos os status de usuários.

#### Exemplo de Resposta
```json
{
  "status_usuarios": [
    {
      "id": 1,
      "status": "ativo"
    },
    {
      "id": 2,
      "status": "inativo"
    },
    {
      "id": 3,
      "status": "suspenso"
    }
  ]
}
```

### POST /status_usuarios
Cria um novo status de usuário.

#### Parâmetros
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente"
}
```

Cria um novo status de usuário.

#### Parâmetros

Parâmetros
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente"
}
```

### PUT /status_usuarios/{id}
Atualiza um status de usuário.

#### Parâmetros
- `id` (int): ID do status de usuário
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente atualizado"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente atualizado"
}
```

### DELETE /status_usuarios/{id}
Exclui um status de usuário.

#### Parâmetros
- `id` (int): ID do status de usuário

#### Exemplo de Resposta
```json
{
  "message": "Status de usuário excluído com sucesso"
}
```
