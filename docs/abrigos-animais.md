# Mock Data: Abrigo para Animais

Este documento descreve a API de mock data para abrigos para animais.

## Tabela de Conteúdo

- [Mock Data: Abrigo para Animais](#mock-data-abrigo-para-animais)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Abrigos para Animais](#abrigos-para-animais)
    - [GET /abrigos\_animais](#get-abrigos_animais)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /abrigos\_animais](#post-abrigos_animais)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /abrigos\_animais/{id}](#put-abrigos_animaisid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /abrigos\_animais/{id}](#delete-abrigos_animaisid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Abrigos para Animais

### GET /abrigos_animais
Retorna uma lista de todos os abrigos para animais.

#### Exemplo de Resposta
```json
{
  "abrigo_animal": [
    {
      "id": 1,
      "nome": "Abrigo Central de Animais",
      "endereco_pessoa_juridica_id": 2,
      "telefone_pessoa_juridica_id": 2,
      "localizacao_id": 2
    },
    {
      "id": 2,
      "nome": "Abrigo Norte de Animais",
      "endereco_pessoa_juridica_id": 4,
      "telefone_pessoa_juridica_id": 4,
      "localizacao_id": 4
    }
  ]
}
```

### POST /abrigos_animais
Cria um novo abrigo para animais.

#### Parâmetros
- `nome` (string): Nome do abrigo
- `endereco_pessoa_juridica_id` (int): ID do endereço
- `telefone_pessoa_juridica_id` (int): ID do telefone
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "nome": "Abrigo Oeste de Animais",
  "endereco_pessoa_juridica_id": 5,
  "telefone_pessoa_juridica_id": 5,
  "localizacao_id": 5
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Abrigo Oeste de Animais",
  "endereco_pessoa_juridica_id": 5,
  "telefone_pessoa_juridica_id": 5,
  "localizacao_id": 5
}
```

### PUT /abrigos_animais/{id}
Atualiza um abrigo para animais.

#### Parâmetros
- `id` (int): ID do abrigo
- `nome` (string): Nome do abrigo
- `endereco_pessoa_juridica_id` (int): ID do endereço
- `telefone_pessoa_juridica_id` (int): ID do telefone
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "nome": "Abrigo Oeste de Animais Atualizado",
  "endereco_pessoa_juridica_id": 5,
  "telefone_pessoa_juridica_id": 5,
  "localizacao_id": 5
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Abrigo Oeste de Animais Atualizado",
  "endereco_pessoa_juridica_id": 5,
  "telefone_pessoa_juridica_id": 5,
  "localizacao_id": 5
}
```

### DELETE /abrigos_animais/{id}
Exclui um abrigo para animais.

#### Parâmetros
- `id` (int): ID do abrigo

#### Exemplo de Resposta
```json
{
  "message": "Abrigo excluído com sucesso"
}
```
