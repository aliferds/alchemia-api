# Alchemia Backend

This project is the API code for the game alchemia.

## Estrutura de Endpoints da API para Alchemia

| Categoria | Método | Endpoint Sugerido | Uso | Autorização |
| :--- | :--- | :--- | :--- | :--- |
| **Autenticação** | `POST` | `/auth/signup` | Criar uma nova conta de jogador. | Público |
| | `POST` | `/auth/signin` | Logar com credenciais. | Público |
| | `GET` | `/users/me` | Verifica o status de login e retorna dados do usuário (inclui nível de autorização). | Logado |
| **Usuário** | `PATCH` | `/users/me` | Atualizar dados do próprio usuário. | Logado |
| | `DELETE` | `/users/me` | Remover a própria conta. | Logado |
| **Jogo (Inventário)**| `GET` | `/inventory` | Retorna itens descobertos. (Convidado: itens iniciais; Logado: itens do DB). | Logado / Convidado |
| | `POST` | **`/transmute`** | **Combina dois itens** (ex: `{ item1: "fogo", item2: "água" }`), verifica receita e atualiza o inventário (se logado). | Logado / Convidado |
| **Admin (Regras)** | `GET` | `/recipes` | Lista todas as regras de combinação (para dashboard de administração). | Admin |
| | `POST` | `/recipes` | Cria uma nova regra/receita. | Admin |
| | `PATCH` | `/recipes/{id}` | Edita uma regra/receita existente. | Admin |
| | `DELETE` | `/recipes/{id}` | Apaga uma regra/receita. | Admin |