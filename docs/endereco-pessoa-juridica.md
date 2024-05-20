# Mock Data: Endereço Pessoa Jurídica

Este documento descreve a API de mock data para endereços de pessoas jurídicas.

## Tabela de Conteúdo

- [Mock Data: Endereço Pessoa Jurídica](#mock-data-endereço-pessoa-jurídica)
  - [Tabela de Conteúdo](#tabela-de-conteúdo)
  - [Endereço Pessoa Jurídica](#endereço-pessoa-jurídica)
    - [GET /enderecos\_pessoas\_juridicas](#get-enderecos_pessoas_juridicas)
      - [Exemplo de Resposta](#exemplo-de-resposta)
    - [POST /enderecos\_pessoas\_juridicas](#post-enderecos_pessoas_juridicas)
      - [Parâmetros](#parâmetros)
      - [Exemplo de Requisição](#exemplo-de-requisição)
      - [Exemplo de Resposta](#exemplo-de-resposta-1)
    - [PUT /enderecos\_pessoas\_juridicas/{id}](#put-enderecos_pessoas_juridicasid)
      - [Parâmetros](#parâmetros-1)
      - [Exemplo de Requisição](#exemplo-de-requisição-1)
      - [Exemplo de Resposta](#exemplo-de-resposta-2)
    - [DELETE /enderecos\_pessoas\_juridicas/{id}](#delete-enderecos_pessoas_juridicasid)
      - [Parâmetros](#parâmetros-2)
      - [Exemplo de Resposta](#exemplo-de-resposta-3)

## Endereço Pessoa Jurídica

### GET /enderecos_pessoas_juridicas
Retorna uma lista de todos os endereços de pessoas jurídicas.

#### Exemplo de Resposta
```json
{
  "endereco_pessoa_juridica": [
    {
      "id": 1,
      "logradouro": "Rua Principal, 100",
      "cidade": "Porto Alegre",
      "estado": "RS",
      "cep": "90000-000"
    },
    {
      "id": 2,
      "logradouro": "Avenida Central, 200",
      "cidade": "Canoas",
      "estado": "RS",
      "cep": "92000-000

"
    }
  ]
}
```

### POST /enderecos_pessoas_juridicas
Cria um novo endereço para uma pessoa jurídica.

#### Parâmetros
- `logradouro` (string): Logradouro
- `cidade` (string): Cidade
- `estado` (string): Estado
- `cep` (string): CEP

#### Exemplo de Requisição
```json
{
  "logradouro": "Avenida Nova, 456",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90100-000"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "logradouro": "Avenida Nova, 456",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90100-000"
}
```

### PUT /enderecos_pessoas_juridicas/{id}
Atualiza um endereço para uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID do endereço
- `logradouro` (string): Logradouro
- `cidade` (string): Cidade
- `estado` (string): Estado
- `cep` (string): CEP

#### Exemplo de Requisição
```json
{
  "logradouro": "Avenida Nova, 456",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90100-000"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "logradouro": "Avenida Nova, 456",
  "cidade": "Porto Alegre",
  "estado": "RS",
  "cep": "90100-000"
}
```

### DELETE /enderecos_pessoas_juridicas/{id}
Exclui um endereço de uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID do endereço

#### Exemplo de Resposta
```json
{
  "message": "Endereço excluído com sucesso"
}
```


