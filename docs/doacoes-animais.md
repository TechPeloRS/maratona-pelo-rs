# Mock Data: Doações para Animais

Este documento descreve a API de mock data para doações para animais.

## Tabela de Conteúdo

## Doações para Animais

### GET /doacoes_animais
Retorna uma lista de todas as doações para animais.

#### Exemplo de Resposta
```json
{
  "doacao_animal": [
    {
      "id": 1,
      "tipo": "ração",
      "descricao": "Ração para cães e gatos",
      "quantidade": "50 kg",
      "abrigo_animal_id": 1,
      "localizacao_id": 1
    },
    {
      "id": 2,
      "tipo": "medicamentos",
      "descricao": "Remédios para animais",
      "quantidade": "30 unidades",
      "abrigo_id": 1,
      "localizacao_id": 1
    }
  ]
}
```

### POST /doacoes_animais
Cria uma nova doação para animais.

#### Parâmetros
- `tipo` (string): Tipo de doação
- `descricao` (string): Descrição da doação
- `quantidade` (string): Quantidade da doação
- `abrigo_animal_id` (int): ID do abrigo
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "tipo": "acessórios",
  "descricao": "Coleiras, brinquedos",
  "quantidade": "20 unidades",
  "abrigo_animal_id": 2,
  "localizacao_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "acessórios",
  "descricao": "Coleiras, brinquedos",
  "quantidade": "20 unidades",
  "abrigo_animal_id": 2,
  "localizacao_id": 2
}
```

### PUT /doacoes_animais/{id}
Atualiza uma doação para animais.

#### Parâmetros
- `id` (int): ID da doação
- `tipo` (string): Tipo de doação
- `descricao` (string): Descrição da doação
- `quantidade` (string): Quantidade da doação
- `abrigo_animal_id` (int): ID do abrigo
- `localizacao_id` (int): ID da localização

#### Exemplo de Requisição
```json
{
  "tipo": "acessórios",
  "descricao": "Coleiras, brinquedos",
  "quantidade": "20 unidades",
  "abrigo_animal_id": 2,
  "localizacao_id": 2
}
```

#### Exemplo de Resposta
```json
{
  "id": 3,
  "tipo": "acessórios",
  "descricao": "Coleiras, brinquedos",
  "quantidade": "20 unidades",
  "abrigo_animal_id": 2,
  "localizacao_id": 2
}
```

### DELETE /doacoes_animais/{id}
Exclui uma doação para animais.

#### Parâmetros
- `id` (int): ID da doação

#### Exemplo de Resposta
```json
{
  "message": "Doação excluída com sucesso"
}
```