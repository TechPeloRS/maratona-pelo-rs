# Mock Data: Telefone Pessoas Juridicas

Este documento descreve a API de mock data para telefones de pessoas jurídicas.

## Tabela de Conteúdo

- [Mock Data: Telefone Pessoas Juridicas](#mock-data-telefone-pessoas-juridicas)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Telefones de Pessoas Jurídicas](#telefones-de-pessoas-jurídicas)
    - [GET /telefones\_pessoas\_juridicas](#get-telefones_pessoas_juridicas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /telefones\_pessoas\_juridicas](#post-telefones_pessoas_juridicas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /telefones\_pessoas\_juridicas/{id}](#put-telefones_pessoas_juridicasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /telefones\_pessoas\_juridicas/{id}](#delete-telefones_pessoas_juridicasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Telefones de Pessoas Jurídicas

### GET /telefones_pessoas_juridicas
Retorna uma lista de todos os telefones de pessoas jurídicas.

#### Exemplo de Resposta
```json
{
  "telefone_pessoa_juridica": [
    {
      "id": 3,
      "numero": "51 9876-5432",
      "pessoa_juridica_id": 1
    },
    {
      "id": 4,
      "numero": "51 8765-4321",
      "pessoa_juridica_id": 2
    }
  ]
}
```

### POST /telefones_pessoas_juridicas
Cria um novo telefone para uma pessoa jurídica.

#### Parâmetros
- `numero` (string): Número de telefone
- `pessoa_juridica_id` (int): ID da pessoa jurídica

#### Exemplo de Requisição


```json
{
  "numero": "51 7654-3210",
  "pessoa_juridica_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "numero": "51 7654-3210",
  "pessoa_juridica_id": 3
}
```

### PUT /telefones_pessoas_juridicas/{id}
Atualiza um telefone de uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID do telefone
- `numero` (string): Número de telefone
- `pessoa_juridica_id` (int): ID da pessoa jurídica

#### Exemplo de Requisição
```json
{
  "numero": "51 7654-3210 Atualizado",
  "pessoa_juridica_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "numero": "51 7654-3210 Atualizado",
  "pessoa_juridica_id": 3
}
```

### DELETE /telefones_pessoas_juridicas/{id}
Exclui um telefone de uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID do telefone

#### Exemplo de Resposta
```json
{
  "message": "Telefone excluído com sucesso"
}
```