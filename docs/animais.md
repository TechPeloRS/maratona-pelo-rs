# Mock Data: Animais

Este documento descreve a API de mock data para animais.

## Tabela de Conteúdo

- [Mock Data: Animais](#mock-data-animais)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Animais](#animais)
    - [GET /animais](#get-animais)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /animais](#post-animais)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /animais/{id}](#put-animaisid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /animais/{id}](#delete-animaisid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Animais

### GET /animais
Retorna uma lista de todos os animais.

#### Exemplo de Resposta
```json
{
  "animal": [
    {
      "id": 1,
      "tipo": "Cão",
      "nome": "Rex",
      "idade": 5,
      "pessoa_id": 1,
      "identificador": "CX123456"
    },
    {
      "id": 2,
      "tipo": "Gato",
      "nome": "Mimi",
      "idade": 2,
      "pessoa_id": 3,
      "identificador": "CX123456"
    }
  ]
}
```

### POST /animais
Cria um novo animal.

#### Parâmetros
- `tipo` (string): Tipo de animal
- `nome` (string): Nome do animal
- `idade` (int): Idade do animal
- `pessoa_id` (int): ID da pessoa responsável
- `identificador` (string): Identificador do animal

#### Exemplo de Requisição
```json
{
  "tipo": "Pássaro",
  "nome": "Piu",
  "idade": 1,
  "pessoa_id": 2,
  "identificador": "PX789012"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "Pássaro",
  "nome": "Piu",
  "idade": 1,
  "pessoa_id": 2,
  "identificador": "PX789012"
}
```

### PUT /animais/{id}
Atualiza um animal.

#### Parâmetros
- `id` (int): ID do animal
- `tipo` (string): Tipo de animal
- `nome` (string): Nome do animal
- `idade` (int): Idade do animal
- `pessoa_id` (int): ID da pessoa responsável
- `identificador` (string): Identificador do animal

#### Exemplo de Requisição
```json
{
  "tipo": "Pássaro",
  "nome": "Piu Atualizado",
  "idade": 2,
  "pessoa_id": 2,
  "identificador": "PX789012"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "Pássaro",
  "nome": "Piu Atualizado",
  "idade": 2,
  "pessoa_id": 2,
  "identificador": "PX789012"
}
```

### DELETE /animais/{id}
Exclui um animal.

#### Parâmetros
- `id` (int): ID do animal

#### Exemplo de Resposta
```json
{
  "message": "Animal excluído com sucesso"
}
```
