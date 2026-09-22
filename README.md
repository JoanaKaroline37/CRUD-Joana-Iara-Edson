## 👥 Equipe de Desenvolvimento

- **Iara**
- **Edson**
- **Carol**
# 🚀 Projeto CRUD API & Async Examples (TypeScript)

Este projeto é uma aplicação desenvolvida em **TypeScript** e **Node.js** criada para demonstrar o consumo de APIs REST assíncronas utilizando a `Fetch API`, manipulação de `Promises` com `async/await` e operações completas de **CRUD** (Create, Read, Update, Delete).

---

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** TypeScript
- **Ambiente de Execução:** Node.js
- **Executor:** [tsx](https://github.com/privatenumber/tsx) *(Executor TypeScript de alta performance para Node.js)*
- **APIs Consumidas:**
  - [JSONPlaceholder](https://jsonplaceholder.typicode.com/) *(Simulação de operações CRUD)*
  - [ViaCEP](https://viacep.com.br/) *(Consulta de endereços por CEP)*

---

## 📌 Funcionalidades Demonstradas

1. **Manipulação de Promises e `async/await`:**
   - Exemplo prático de comportamento assíncrono temporizado e resolução de Promises.
2. **Consulta Externa (GET):**
   - Busca de dados de endereço em tempo real consumindo a API pública do ViaCEP.
3. **CRUD de Posts (JSONPlaceholder):**
   - 📖 **Read (GET):** Busca o post de ID 1 e exibe o seu título na consola.
   - ➕ **Create (POST):** Envia dados de um novo post (título, corpo e ID do utilizador) e exibe o objeto registado devolvido pela API.
   - ✏️ **Update (PATCH):** Atualiza o título do post de ID 1 e exibe o resultado retornado.
   - 🗑️ **Delete (DELETE):** Envia a requisição de remoção para o post de ID 1 e confirma o sucesso da operação.

---

## 📁 Estrutura do Código

```typescript
// Tipagem de Dados
type Cep = {
  cep: string;
  logradouro: string;
  bairro: string;
  localidade: string;
  uf: string;
  // ...
};

type Post = {
  userId?: number;
  id?: number;
  title: string;
  body: string;
};

// Métodos implementados:
// - buscarcep(): Consulta GET ao ViaCEP
// - buscarPost(): Read (GET)
// - criarPost(novoPost): Create (POST)
// - atualizarPost(id, novoTitulo): Update (PATCH)
// - deletarPost(id): Delete (DELETE)