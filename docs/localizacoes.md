# Mock Data: Localizações

Este documento descreve a API de mock data para localizações.

## Tabela de Conteúdo

- [Mock Data: Localizações](#mock-data-localizações)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Localizações](#localizações)
    - [GET /localizacoes](#get-localizacoes)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /localizacoes](#post-localizacoes)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /localizacoes/{id}](#put-localizacoesid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /localizacoes/{id}](#delete-localizacoesid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Localizações

### GET /localizacoes
Retorna uma lista de todas as localizações.

#### Exemplo de Resposta
```json
{
  "localizacoes": [
    {
      "id": 1,
      "latitude": -30.0346,
      "longitude": -51.2177
    },
    {
      "id": 2,
      "latitude": -29.9128,
      "longitude": -51.1855
    }
  ]
}
```

### POST /localizacoes
Cria uma nova localização.

#### Parâmetros
- `latitude` (float): Latitude
- `longitude` (float): Longitude

#### Exemplo de Requisição
```json
{
  "latitude": -30.1234,
  "longitude": -51.1234
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "latitude": -30.1234,
  "longitude": -51.1234
}
```

### PUT /localizacoes/{id}
Atualiza uma localização.

#### Parâmetros
- `id` (int): ID da localização
- `latitude` (float): Latitude
- `longitude` (float): Longitude

#### Exemplo de Requisição
```json
{
  "latitude": -30.1234,
  "longitude": -51.1234
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "latitude": -30.1234,
  "longitude": -51.1234
}
```

### DELETE /localizacoes/{id}
Exclui uma localização.

#### Parâmetros
- `id` (int): ID da localização

#### Exemplo de Resposta
```json
{
  "message": "Localização excluída com sucesso"
}
```