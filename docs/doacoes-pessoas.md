# Mock Data: Doações para Pessoas

Este documento descreve a API de mock data para doações para pessoas.

## Tabela de Conteúdo

- [Mock Data: Doações para Pessoas](#mock-data-doações-para-pessoas)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Doações para Pessoas](#doações-para-pessoas)
    - [GET /doacoes\_pessoas](#get-doacoes_pessoas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /doacoes\_pessoas](#post-doacoes_pessoas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /doacoes\_pessoas/{id}](#put-doacoes_pessoasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /doacoes\_pessoas/{id}](#delete-doacoes_pessoasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Doações para Pessoas

### GET /doacoes_pessoas
Retorna uma lista de todas as doações para pessoas.

#### Exemplo de Resposta
```json
{
  "doacao_pessoa": [
    {
      "id": 1,
      "tipo": "alimentos",
      "descricao": "Arroz, feijão, macarrão",
      "quantidade": "100 kg",
      "abrigo_pessoa_id": 1,
      "localizacao_id": 1
    },
    {
      "id": 2,
      "tipo": "roupas",
      "descricao": "Roupas masculinas e femininas",
      "quantidade": "200 peças",
      "abrigo_pessoa_id": 1,
      "localizacao_id": 1
    }
  ]
}
```

### POST /doacoes_pessoas
Cria uma nova doação para pessoas.

#### Parâmetros
- `tipo` (string): Tipo de doação
- `descricao` (string): Descrição da doação
- `quantidade` (string): Quantidade da doação
- `abrigo_pessoa_id` (int): ID do abrigo
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "tipo": "higiene pessoal",
  "descricao": "Sabonetes, shampoos, pastas de dente",
  "quantidade": "150 unidades",
  "abrigo_pessoa_id": 2,
  "localizacao_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "higiene pessoal",
  "descricao": "Sabonetes, shampoos, pastas de dente",
  "quantidade": "150 unidades",
  "abrigo_pessoa_id": 2,
  "localizacao_id": 2
}
```

### PUT /doacoes_pessoas/{id}
Atualiza uma doação para pessoas.

#### Parâmetros
- `id` (int): ID da doação
- `tipo` (string): Tipo de doação
- `descricao` (string): Descrição da doação
- `quantidade` (string): Quantidade da doação
- `abrigo_pessoa_id` (int): ID do abrigo
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "tipo": "higiene pessoal",
  "descricao": "Sabonetes, shampoos, pastas de dente",
  "quantidade": "150 unidades",
  "abrigo_pessoa_id": 2,
  "localizacao_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "higiene pessoal",
  "descricao": "Sabonetes, shampoos, pastas de dente",
  "quantidade": "150 unidades",
  "abrigo_pessoa_id": 2,
  "localizacao_id": 2
}
```

### DELETE /doacoes_pessoas/{id}
Exclui uma doação para pessoas.

#### Parâmetros
- `id` (int): ID da doação

#### Exemplo de Resposta
```json
{
  "message": "Doação excluída com sucesso"
}
```

