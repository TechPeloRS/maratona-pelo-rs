# Mock Data: Endereço Pessoa Física

Este documento descreve a API de mock data para endereços de pessoas físicas.

## Tabela de Conteúdo

- [Mock Data: Endereço Pessoa Física](#mock-data-endereço-pessoa-física)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Endereço Pessoa Física](#endereço-pessoa-física)
    - [GET /enderecos\_pessoas\_fisicas](#get-enderecos_pessoas_fisicas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /enderecos\_pessoas\_fisicas](#post-enderecos_pessoas_fisicas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /enderecos\_pessoas\_fisicas/{id}](#put-enderecos_pessoas_fisicasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /enderecos\_pessoas\_fisicas/{id}](#delete-enderecos_pessoas_fisicasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Endereço Pessoa Física

### GET /enderecos_pessoas_fisicas
Retorna uma lista de todos os endereços de pessoas físicas.

#### Exemplo de Resposta
```json
{
  "endereco_pessoa_fisica": [
    {
      "id": 1,
      "logradouro": "Rua Principal, 100",
      "cidade": "Porto Alegre",
      "estado": "RS",
      "cep": "90000-000"
    },
    {
      "id": 2,
      "logradouro": "Avenida Secundária, 200",
      "cidade": "Canoas",
      "estado": "RS",
      "cep": "92000-000"
    }
  ]
}
```

### POST /enderecos_pessoas_fisicas
Cria um novo endereço para uma pessoa física.

#### Parâmetros
- `logradouro` (string): Logradouro
- `cidade` (string): Cidade
- `estado` (string): Estado
- `cep` (string): CEP

#### Exemplo de Requisição
```json
{
  "logradouro": "Rua Nova, 123",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90000-000"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "logradouro": "Rua Nova, 123",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90000-000"
}
```

### PUT /enderecos_pessoas_fisicas/{id}
Atualiza um endereço para uma pessoa física.

#### Parâmetros
- `id` (int): ID do endereço
- `logradouro` (string): Logradouro
- `cidade` (string): Cidade
- `estado` (string): Estado
- `cep` (string): CEP

#### Exemplo de Requisição
```json
{
  "logradouro": "Rua Nova, 123",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90000-000"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "logradouro": "Rua Nova, 123",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90000-000"
}
```

### DELETE /enderecos_pessoas_fisicas/{id}
Exclui um endereço de uma pessoa física.

#### Parâmetros
- `id` (int): ID do endereço

#### Exemplo de Resposta
```json
{
  "message": "Endereço excluído com sucesso"
}
```

---
