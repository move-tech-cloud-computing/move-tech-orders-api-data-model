# Modelagem de Dados

## Entidades

### Pedido (orders)

| Coluna     | Tipo      | Descrição                                    |
|------------|-----------|----------------------------------------------|
| id         | INTEGER   | Identificador único, gerado automaticamente  |
| customer   | TEXT      | Nome do cliente                              |
| status     | TEXT      | Estado do pedido (ex.: pending, completed)   |
| created_at | TIMESTAMP | Data e hora de criação, automática           |

### Item (items)

| Coluna      | Tipo    | Descrição                            |
|-------------|---------|--------------------------------------|
| id          | INTEGER | Identificador único, gerado auto.    |
| order_id    | INTEGER | Chave estrangeira → orders(id)       |
| sku         | TEXT    | Código do item                       |
| description | TEXT    | Descrição do item                    |
| quantity    | INTEGER | Quantidade                           |

## Relacionamento

Um pedido (`orders`) possui vários itens (`items`), indicando um relacionamento **1:N** (Um para Muitos).
