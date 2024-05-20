# Mock Data: Pessoas Físicas

Este documento descreve a API de mock data para pessoas físicas.

## Tabela de Conteúdo

- [Mock Data: Pessoas Físicas](#mock-data-pessoas-físicas)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Pessoas Físicas](#pessoas-físicas)
    - [GET /pessoas\_fisicas](#get-pessoas_fisicas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /pessoas\_fisicas](#post-pessoas_fisicas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /pessoas\_fisicas/{id}](#put-pessoas_fisicasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /pessoas\_fisicas/{id}](#delete-pessoas_fisicasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Pessoas Físicas

### GET /pessoas_fisicas
Retorna uma lista de todas as pessoas físicas.

#### Exemplo de Resposta
```json
{
  "pessoa_fisica": [
    {
      "id": 1,
      "nome": "Maria Silva",
      "idade": 34,
      "sexo": "Feminino",
      "telefone_pessoa_fisica": 3,
      "abrigo_id": 1
    },
    {
      "id": 2,
      "nome": "João Santos",
      "idade": 45,
      "sexo": "Masculino",
      "telefone_pessoa_fisica": 4,
      "abrigo_id": 1
    }
  ]
}
```

### POST /pessoas_fisicas
Cria uma nova pessoa física.

#### Parâmetros
- `nome` (string): Nome da pessoa
- `idade` (int): Idade da pessoa
- `sexo` (string): Sexo da pessoa
- `telefone_pessoa_fisica` (int): ID do telefone
- `abrigo_id` (int): ID do abrigo

#### Exemplo de Requisição
```json
{
  "nome": "Carlos Souza",
  "idade": 50,
  "sexo": "Masculino",
  "telefone_pessoa_fisica": 6,
  "abrigo_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "nome": "Carlos Souza",
  "idade": 50,
  "sexo": "Masculino",
  "telefone_pessoa_fisica": 6,
  "abrigo_id": 2
}
```

### PUT /pessoas_fisicas/{id}
Atualiza uma pessoa física.

#### Parâmetros
- `id` (int): ID da pessoa física
- `nome` (string): Nome da pessoa
- `idade` (int): Idade da pessoa
- `sexo` (string): Sexo da pessoa
- `telefone_pessoa_fisica` (int): ID do telefone


- `abrigo_id` (int): ID do abrigo

#### Exemplo de Requisição
```json
{
  "nome": "Carlos Souza Atualizado",
  "idade": 51,
  "sexo": "Masculino",
  "telefone_pessoa_fisica": 6,
  "abrigo_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "nome": "Carlos Souza Atualizado",
  "idade": 51,
  "sexo": "Masculino",
  "telefone_pessoa_fisica": 6,
  "abrigo_id": 2
}
```

### DELETE /pessoas_fisicas/{id}
Exclui uma pessoa física.

#### Parâmetros
- `id` (int): ID da pessoa física

#### Exemplo de Resposta
```json
{
  "message": "Pessoa excluída com sucesso"
}
```
