# Mock Data: Abrigo para Pessoas

Este documento descreve a API de mock data para abrigos para pessoas.

## Tabela de Conteúdo

- [Mock Data: Abrigo para Pessoas](#mock-data-abrigo-para-pessoas)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
    - [GET /abrigos\_pessoas](#get-abrigos_pessoas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /abrigos\_pessoas](#post-abrigos_pessoas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /abrigos\_pessoas/{id}](#put-abrigos_pessoasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /abrigos\_pessoas/{id}](#delete-abrigos_pessoasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)




### GET /abrigos_pessoas
Retorna uma lista de todos os abrigos para pessoas.

#### Exemplo de Resposta
```json
{
  "abrigo_pessoa": [
    {
      "id": 1,
      "nome": "Abrigo Central",
      "endereco_pessoa_juridica_id": 1,
      "telefone_pessoa_juridica_id": 1,
      "localizacao_id": 1
    },
    {
      "id": 2,
      "nome": "Abrigo Norte",
      "endereco_pessoa_juridica_id": 2,
      "telefone_pessoa_juridica_id": 2,
      "localizacao_id": 2
    }
  ]
}
```

### POST /abrigos_pessoas
Cria um novo abrigo para pessoas.

#### Parâmetros
- `nome` (string): Nome do abrigo
- `endereco_pessoa_juridica_id` (int): ID do endereço
- `telefone_pessoa_juridica_id` (int): ID do telefone
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "nome": "Abrigo Sul",
  "endereco_pessoa_juridica_id": 3,
  "telefone_pessoa_juridica_id": 3,
  "localizacao_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Abrigo Sul",
  "endereco_pessoa_juridica_id": 3,
  "telefone_pessoa_juridica_id": 3,
  "localizacao_id": 3
}
```

---

### PUT /abrigos_pessoas/{id}
Atualiza um abrigo para pessoas.

#### Parâmetros
- `id` (int): ID do abrigo
- `nome` (string): Nome do abrigo
- `endereco_pessoa_juridica_id` (int): ID do endereço
- `telefone_pessoa_juridica_id` (int): ID do telefone
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "nome": "Abrigo Sul Atualizado",
  "endereco_pessoa_juridica_id": 3,
  "telefone_pessoa_juridica_id": 3,
  "localizacao_id": 3
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Abrigo Sul Atualizado",
  "endereco_pessoa_juridica_id": 3,
  "telefone_pessoa_juridica_id": 3,
  "localizacao_id": 3
}
```

### DELETE /abrigos_pessoas/{id}
Exclui um abrigo para pessoas.

#### Parâmetros
- `id` (int): ID do abrigo

#### Exemplo de Resposta
```json
{
  "message": "Abrigo excluído com sucesso"
}
```
