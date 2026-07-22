# Modelagem de Dados

## Entidades

### Pedido (orders)

| Coluna     | Tipo      | Descrição                                    |
|------------|-----------|----------------------------------------------|
| id         | INTEGER   | Identificador único, gerado automaticamente  |
| status     | TEXT      | Estado do pedido (ex.: pending, completed)   |
| created_at | TIMESTAMP | Data e hora de criação, automática           |

### Item (items)

| Coluna   | Tipo    | Descrição                            |
|----------|---------|--------------------------------------|
| id       | INTEGER | Identificador único, gerado auto.    |
| order_id | INTEGER | Chave estrangeira → orders(id)       |
| title    | TEXT    | Nome do item                         |
| price    | NUMERIC | Preço unitário                       |
| quantity | INTEGER | Quantidade                           |

