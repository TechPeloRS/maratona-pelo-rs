# Mock Data: Tipos Usuários

Este documento descreve a API de mock data para tipos de usuários.

## Tabela de Conteúdo

- [Mock Data: Tipos Usuários](#mock-data-tipos-usuários)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Tipos de Usuários](#tipos-de-usuários)
    - [GET /tipos\_usuarios](#get-tipos_usuarios)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /tipos\_usuarios](#post-tipos_usuarios)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /tipos\_usuarios/{id}](#put-tipos_usuariosid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /tipos\_usuarios/{id}](#delete-tipos_usuariosid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Requisição](#exemplo-de-requisição-2)

## Tipos de Usuários

### GET /tipos_usuarios
Retorna uma lista de todos os tipos de usuários.

#### Exemplo de Resposta
```json
{
  "tipos_usuarios": [
    {
      "id": 1,
      "tipo": "admin",
      "descricao": "Usuário com acesso completo ao sistema, incluindo gerenciamento de outros usuários e configurações."
    },
    {
      "id": 2,
      "tipo": "voluntario",
      "descricao": "Usuário voluntário que pode ajudar no gerenciamento de doações e abrigos."
    },
    {
      "id": 3,
      "tipo": "coordenador",
      "descricao": "Usuário responsável pela coordenação das atividades nos abrigos e supervisão dos voluntários."
    }
  ]
}
```

### POST /tipos_usuarios
Cria um novo tipo de usuário.

#### Parâmetros
- `tipo` (string): Tipo de usuário
- `descricao` (string): Descrição do tipo de usuário

#### Exemplo de Requisição
```json
{
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

### PUT /tipos_usuarios/{id}
Atualiza um tipo de usuário.

#### Parâmetros
- `id` (int): ID do tipo de usuário
- `tipo` (string): Tipo de usuário
- `descricao` (string): Descrição do tipo de usuário

#### Exemplo de Requisição
```json
{
  "tipo": "doador atualizado",
  "descricao": "Usuário que pode doar itens e recursos atualizados."
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "tipo": "doador atualizado",
  "descricao": "Usuário que pode doar itens e recursos atualizados."
}
```

### DELETE /tipos_usuarios/{id}
Exclui um tipo de usuário.

#### Parâmetros
- `id` (int): ID do tipo de usuário

#### Exemplo de Requisição

Exemplo de Resposta
```json
{
  "message": "Tipo de usuário excluído com sucesso"
}
```
