# Mock Data: Telefone Pessoa Física

Este documento descreve a API de mock data para telefones de pessoas físicas.

## Tabela de Conteúdo

- [Mock Data: Telefone Pessoa Física](#mock-data-telefone-pessoa-física)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Telefones de Pessoas Físicas](#telefones-de-pessoas-físicas)
    - [GET /telefones\_pessoas\_fisicas](#get-telefones_pessoas_fisicas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /telefones\_pessoas\_fisicas](#post-telefones_pessoas_fisicas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /telefones\_pessoas\_fisicas/{id}](#put-telefones_pessoas_fisicasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /telefones\_pessoas\_fisicas/{id}](#delete-telefones_pessoas_fisicasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Telefones de Pessoas Físicas

### GET /telefones_pessoas_fisicas
Retorna uma lista de todos os telefones de pessoas físicas.

#### Exemplo de Resposta
```json
{
  "telefone_pessoa_fisica": [
    {
      "id": 3,
      "numero": "51 9876-5432",
      "pessoa_fisica_id": 1
    },
    {
      "id": 4,
      "numero": "51 8765-4321",
      "pessoa_fisica_id": 2
    }
  ]
}
```

### POST /telefones_pessoas_fisicas
Cria um novo telefone para uma pessoa física.

#### Parâmetros
- `numero` (string): Número de telefone
- `pessoa_fisica_id` (int): ID da pessoa física

#### Exemplo de Requisição
```json
{
  "numero": "51 7654-3210",
  "pessoa_fisica_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "numero": "51 7654-3210",
  "pessoa_fisica_id": 3
}
```

### PUT /telefones_pessoas_fisicas/{id}
Atualiza um telefone de uma pessoa física.

#### Parâmetros
- `id` (int): ID do telefone
- `numero` (string): Número de telefone
- `pessoa_fisica_id` (int): ID da pessoa física

#### Exemplo de Requisição
```json
{
  "numero": "51 7654-3210 Atualizado",
  "pessoa_fisica_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "numero": "51 7654-3210 Atualizado",
  "pessoa_fisica_id": 3
}
```

### DELETE /telefones_pessoas_fisicas/{id}
Exclui um telefone de uma pessoa física.

#### Parâmetros
- `id` (int): ID do telefone

#### Exemplo de Resposta
```json
{
  "message": "Telefone excluído com sucesso"
}
```
