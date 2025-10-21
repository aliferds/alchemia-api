# Alchemia Backend

This project is the API code for the game alchemia.

## Estrutura de Endpoints da API para Alchemia

| Método | Endpoint | Uso | Autorização |
| :--- | :--- | :--- | :--- |
| `POST` | **`/transmute`** | **Combina itens** (ex: `{ item1: "fogo", item2: "água" }`), verifica receita. | Player |
| `POST` | `/auth/signin` | Logar | Admin |
| `POST` | `/recipes` | Cria uma nova regra/receita. | Admin |
| `PATCH` | `/recipes/{id}` | Edita uma regra/receita existente. | Admin |
| `DELETE` | `/recipes/{id}` | Apaga uma regra/receita. | Admin |
