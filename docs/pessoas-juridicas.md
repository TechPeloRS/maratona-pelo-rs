# Mock Data: Pessoas Jurídicas

Este documento descreve a API de mock data para pessoas jurídicas.

## Tabela de Conteúdo

## Pessoas Jurídicas

### GET /pessoas_juridicas
Retorna uma lista de todas as pessoas jurídicas.

#### Exemplo de Resposta
```json
{
  "pessoa_juridica": [
    {
      "id": 1,
      "nome": "

Empresa Solidária",
      "cnpj": "12.345.678/0001-90",
      "endereco_id": 1,
      "telefone_id": 1,
      "email": "contato@empresasolidaria.com",
      "tipo": "Empresa"
    },
    {
      "id": 2,
      "nome": "ONG Amigos do Bem",
      "cnpj": "98.765.432/0001-21",
      "endereco_id": 2,
      "telefone_id": 2,
      "email": "contato@amigosdobem.org",
      "tipo": "ONG"
    }
  ]
}
```

### POST /pessoas_juridicas
Cria uma nova pessoa jurídica.

#### Parâmetros
- `nome` (string): Nome da pessoa jurídica
- `cnpj` (string): CNPJ da pessoa jurídica
- `endereco_id` (int): ID do endereço
- `telefone_id` (int): ID do telefone
- `email` (string): Email da pessoa jurídica
- `tipo` (string): Tipo da pessoa jurídica

#### Exemplo de Requisição
```json
{
  "nome": "Instituto de Ajuda",
  "cnpj": "99.999.999/0001-99",
  "endereco_id": 3,
  "telefone_id": 3,
  "email": "contato@institutodeajuda.org",
  "tipo": "Instituto"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Instituto de Ajuda",
  "cnpj": "99.999.999/0001-99",
  "endereco_id": 3,
  "telefone_id": 3,
  "email": "contato@institutodeajuda.org",
  "tipo": "Instituto"
}
```

### PUT /pessoas_juridicas/{id}
Atualiza uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID da pessoa jurídica
- `nome` (string): Nome da pessoa jurídica
- `cnpj` (string): CNPJ da pessoa jurídica
- `endereco_id` (int): ID do endereço
- `telefone_id` (int): ID do telefone
- `email` (string): Email da pessoa jurídica
- `tipo` (string): Tipo da pessoa jurídica

#### Exemplo de Requisição
```json
{
  "nome": "Instituto de Ajuda Atualizado",
  "cnpj": "99.999.999/0001-99",
  "endereco_id": 3,
  "telefone_id": 3,
  "email": "contato@institutodeajuda.org",
  "tipo": "Instituto"
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Instituto de Ajuda Atualizado",
  "cnpj": "99.999.999/0001-99",
  "endereco_id": 3,
  "telefone_id": 3,
  "email": "contato@institutodeajuda.org",
  "tipo": "Instituto"
}
```

### DELETE /pessoas_juridicas/{id}
Exclui uma pessoa jurídica.

#### Parâmetros
- `id` (int): ID da pessoa jurídica

#### Exemplo de Resposta
```json
{
  "message": "Pessoa jurídica excluída com sucesso"
}
```