# API DOCUMENTATION - MOCK DATA

## Navigation - API Documentation

1. [API Documentation](#api-documentation)
   - [Telefones](#telefones)
     - [GET /telefones_pessoas_fisicas](#get-telefonespessoasfisicas)
     - [POST /telefones_pessoas_fisicas](#post-telefonespessoasfisicas)
     - [PUT /telefones_pessoas_fisicas/{id}](#put-telefonespessoasfisicasid)
     - [DELETE /telefones_pessoas_fisicas/{id}](#delete-telefonespessoasfisicasid)
     - [GET /telefones_pessoas_juridicas](#get-telefonespessoasjuridicas)
     - [POST /telefones_pessoas_juridicas](#post-telefonespessoasjuridicas)
     - [PUT /telefones_pessoas_juridicas/{id}](#put-telefonespessoasjuridicasid)
     - [DELETE /telefones_pessoas_juridicas/{id}](#delete-telefonespessoasjuridicasid)
   - [Usuários](#usuários)
     - [GET /usuarios](#get-usuarios)
     - [POST /usuarios](#post-usuarios)
     - [PUT /usuarios/{id}](#put-usuariosid)
     - [DELETE /usuarios/{id}](#delete-usuariosid)
   - [Tipos de Usuários](#tipos-de-usuários)
     - [GET /tipos_usuarios](#get-tiposusuarios)
     - [POST /tipos_usuarios](#post-tiposusuarios)
     - [PUT /tipos_usuarios/{id}](#put-tiposusuariosid)
     - [DELETE /tipos_usuarios/{id}](#delete-tiposusuariosid)
   - [Status de Usuários](#status-de-usuários)
     - [GET /status_usuarios](#get-statususuarios)
     - [POST /status_usuarios](#post-statususuarios)
     - [PUT /status_usuarios/{id}](#put-statususuariosid)
     - [DELETE /status_usuarios/{id}](#delete-statususuariosid)


## Usuários

### GET /usuarios
Retorna uma lista de todos os usuários.

#### Exemplo de Resposta
```json
{
  "usuarios": [
    {
      "id": 1,
      "nome": "Admin",
      "email": "admin@example.com",
      "senha": "hashed_password_1",
      "tipo_usuario": [
        {
          "id": 1,
          "tipo": "admin"
        }
      ],
      "telefone_id": 1,
      "data_criacao": "2021-06-01T00:00:00Z",
      "data_atualizacao": "2021-06-01T00:00:00Z",
      "data_ultimo_login": "2021-06-01T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    },
    {
      "id": 2,
      "nome": "John Doe",
      "email": "johndoe@example.com",
      "senha": "hashed_password_2",
      "tipo_usuario": [
        {
          "id": 2,
          "tipo": "voluntario"
        }
      ],
      "telefone_id": 2,
      "data_criacao": "2022-01-15T00:00:00Z",
      "data_atualizacao": "2022-01-15T00:00:00Z",
      "data_ultimo_login": "2022-01-20T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    }
  ]
}
```

### POST /usuarios
Cria um novo usuário.

#### Parâmetros
- `nome` (string): Nome do usuário
- `email` (string): Email do usuário
- `senha` (string): Senha do usuário
- `tipo_usuario` (array): Array com objetos contendo ID e tipo de usuário
- `telefone_id` (int): ID do telefone
- `data_criacao` (string): Data de criação do usuário
- `data_atualizacao` (string): Data de atualização do usuário
- `data_ultimo_login` (string): Data do último login do usuário
- `status` (array): Array com objetos contendo ID e status do usuário

#### Exemplo de Requisição
```json
{
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status_usuario": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status_usuario": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

---

## Tipos de Usuários

### GET /tipos_usuarios
Retorna uma lista de todos os tipos de usuários.

#### Exemplo de Resposta
```json
{
  "tipos_usuarios": [
    {
      "id": 1,
      "tipo": "admin",
      "descricao": "Usuário com acesso completo ao sistema, incluindo gerenciamento de outros usuários e configurações."
    },
    {
      "id": 2,
      "tipo": "voluntario",
      "descricao": "Usuário voluntário que pode ajudar no gerenciamento de doações e abrigos."
    },
    {
      "id": 3,
      "tipo": "coordenador",
      "descricao": "Usuário responsável pela coordenação das atividades nos abrigos e supervisão dos voluntários."
    }
  ]
}
```

### POST /tipos_usuarios
Cria um novo tipo de usuário.

#### Parâmetros
- `tipo` (string): Tipo de usuário
- `descricao` (string): Descrição do tipo de usuário

#### Exemplo de Requisição
```json
{
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

---

## Status de Usuários

### GET /status_usuarios
Retorna uma lista de todos os status de usuários.

#### Exemplo de Resposta
```json
{
  "status_usuarios": [
    {
      "id": 1,
      "status": "ativo"
    },
    {
      "id": 2,
      "status": "inativo"
    },
    {
      "id": 3,
      "status": "suspenso"
    }
  ]
}
```

### POST /status_usuarios
Cria um novo status de usuário.

#### Par

âmetros
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente"
}
```

---

### API Documentation

---

## Abrigos para Pessoas

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

## Abrigos para Animais

### GET /abrigos_animais
Retorna uma lista de todos os abrigos para animais.

#### Exemplo de Resposta
```json
{
  "abrigos_animais": [
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

## Telefones


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

---

## Usuários

### GET /usuarios
Retorna uma lista de todos os usuários.

#### Exemplo de Resposta
```json
{
  "usuarios": [
    {
      "id": 1,
      "nome": "Admin",
      "email": "admin@example.com",
      "senha": "hashed_password_1",
      "tipo_usuario": [
        {
          "id": 1,
          "tipo": "admin"
        }
      ],
      "telefone_id": 1,
      "data_criacao": "2021-06-01T00:00:00Z",
      "data_atualizacao": "2021-06-01T00:00:00Z",
      "data_ultimo_login": "2021-06-01T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    },
    {
      "id": 2,
      "nome": "John Doe",
      "email": "johndoe@example.com",
      "senha": "hashed_password_2",
      "tipo_usuario": [
        {
          "id": 2,
          "tipo": "voluntario"
        }
      ],
      "telefone_id": 2,
      "data_criacao": "2022-01-15T00:00:00Z",
      "data_atualizacao": "2022-01-15T00:00:00Z",
      "data_ultimo_login": "2022-01-20T00:00:00Z",
      "status_usuario": [
        {
          "id": 1,
          "status": "ativo"
        }
      ]
    }
  ]
}
```

### POST /usuarios
Cria um novo usuário.

#### Parâmetros
- `nome` (string): Nome do usuário
- `email` (string): Email do usuário
- `senha` (string): Senha do usuário
- `tipo_usuario` (array): Array com objetos contendo ID e tipo de usuário
- `telefone_id` (int): ID do telefone
- `data_criacao` (string): Data de criação do usuário
- `data_atualizacao` (string): Data de atualização do usuário
- `data_ultimo_login` (string): Data do último login do usuário
- `status` (array): Array com objetos contendo ID e status do usuário

#### Exemplo de Requisição
```json
{
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Jane Smith",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

---

## Tipos de Usuários

### GET /tipos_usuarios
Retorna uma lista de todos os tipos de usuários.

#### Exemplo de Resposta
```json
{
  "tipos_usuarios": [
    {
      "id": 1,
      "tipo": "admin",
      "descricao": "Usuário com acesso completo ao sistema, incluindo gerenciamento de outros usuários e configurações."
    },
    {
      "id": 2,
      "tipo": "voluntario",
      "descricao": "Usuário voluntário que pode ajudar no gerenciamento de doações e abrigos."
    },
    {
      "id": 3,
      "tipo": "ong",
      "descricao": "Usuário representante de uma ONG que pode ajudar no gerenciamento de doações e abrigos."
    },
    {
      "id": 4,
      "tipo": "usuario",
      "descricao": "Usuário comum que pode solicitar doações e abrigo."
    }
  ]
}
```

### POST /tipos_usuarios
Cria um novo tipo de usuário.

#### Parâmetros
- `tipo` (string): Tipo de usuário
- `descricao` (string): Descrição do tipo de usuário

#### Exemplo de Requisição
```json
{
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "tipo": "doador",
  "descricao": "Usuário que pode doar itens e recursos."
}
```

---

## Status de Usuários

### GET /status_usuarios
Retorna uma lista de todos os status de usuários.

#### Exemplo de Resposta
```json
{
  "status_usuarios": [
    {
      "id": 1,
      "status": "ativo"
    },
    {
      "id": 2,
      "status": "inativo"
    },
    {
      "id": 3,
      "status": "suspenso"
    }
  ]
}
```

### POST /status_usuarios
Cria um novo status de usuário.

#### Parâmetros
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente"
}
```

## Telefones


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

---

## Usuários

### PUT /usuarios/{id}
Atualiza um usuário.

#### Parâmetros
- `id` (int): ID do usuário
- `nome` (string): Nome do usuário
- `email` (string): Email do usuário
- `senha` (string): Senha do usuário
- `tipo_usuario` (array): Array com objetos contendo ID e tipo de usuário
- `telefone_id` (int): ID do telefone
- `data_criacao` (string): Data de criação do usuário
- `data_atualizacao` (string): Data de atualização do usuário
- `data_ultimo_login` (string): Data do último login do usuário
- `status` (array): Array com objetos contendo ID e status do usuário

#### Exemplo de Requisição
```json
{
  "nome": "Jane Smith Atualizado",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "nome": "Jane Smith Atualizado",
  "email": "janesmith@example.com",
  "senha": "hashed_password_3",
  "tipo_usuario": [
    {
      "id": 2,
      "tipo": "voluntario"
    }
  ],
  "telefone_id": 3,
  "data_criacao": "2023-03-10T00:00:00Z",
  "data_atualizacao": "2023-03-10T00:00:00Z",
  "data_ultimo_login": "2023-03-12T00:00:00Z",
  "status": [
    {
      "id": 1,
      "status": "ativo"
    }
  ]
}
```

### DELETE /usuarios/{id}
Exclui um usuário.

#### Parâmetros
- `id` (int): ID do usuário

#### Exemplo de Resposta
```json
{
  "message": "Usuário excluído com sucesso"
}
```

---

## Tipos de Usuários

### PUT /tipos_usuarios/{id}
Atualiza um tipo de usuário.

#### Parâmetros
- `id` (int): ID do tipo de usuário
- `tipo` (string): Tipo de usuário
- `descricao` (string): Descrição do tipo de usuário

#### Exemplo de Requisição
```json
{
  "tipo": "doador atualizado",
  "descricao": "Usuário que pode doar itens e recursos atualizados."
}
```

#### Exemplo de Resposta
```json
{
  "id": 5,
  "tipo": "doador atualizado",
  "descricao": "Usuário que pode doar itens e recursos atualizados."
}
```

### DELETE /tipos_usuarios/{id}
Exclui um tipo de usuário.

#### Parâmetros
- `id` (int): ID do tipo de usuário

#### Ex

emplo de Resposta
```json
{
  "message": "Tipo de usuário excluído com sucesso"
}
```

---

## Status de Usuários

### PUT /status_usuarios/{id}
Atualiza um status de usuário.

#### Parâmetros
- `id` (int): ID do status de usuário
- `status` (string): Status do usuário

#### Exemplo de Requisição
```json
{
  "status": "pendente atualizado"
}
```

#### Exemplo de Resposta
```json
{
  "id": 4,
  "status": "pendente atualizado"
}
```

### DELETE /status_usuarios/{id}
Exclui um status de usuário.

#### Parâmetros
- `id` (int): ID do status de usuário

#### Exemplo de Resposta
```json
{
  "message": "Status de usuário excluído com sucesso"
}
```

---
