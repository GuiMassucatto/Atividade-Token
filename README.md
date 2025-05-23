# Projeto: Login JWT

Este projeto implementa um sistema básico de autenticação utilizando JWT (JSON Web Tokens) para proteger rotas e controlar sessões de usuários em uma API.

## Tecnologias Utilizadas

- Node.js
- Express
- jsonwebtoken
- bcryptjs
- dotenv

## Como testar o projeto

1. Extraia os arquivos do `.zip` para uma pasta local.

2. Abra o terminal e acesse a pasta do projeto:

```bash
cd caminho/para/a/pasta
```

3. Instale as dependências:

```bash
npm install
```

4. Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
PORT=3000
SECRET_JWT=4ffb1c229f29dfa21b739453dba1689c2a0bb2de3c0ac11b5be4b69ed37a7d6bcb4e7f90807a61793af0aaf89d47420a180947dd195bc89cfc211c472847934b
```

5. Inicie o servidor com:

```bash
npm start
```

Ou, se estiver usando nodemon:

```bash
npm run dev
```

6. Teste os endpoints usando uma ferramenta como Postman ou Insomnia:

- POST `/login`: envia `email` e `senha`, retorna um token JWT.
- GET `/protected`: rota protegida, requer `Authorization: Bearer <token>` no cabeçalho.

## Exemplo de uso

1. Faça login com:

```json
{
  "email": "usuario@gmail.com",
  "senha": "123456789"
}
```

2. Copie o token retornado.

3. Acesse rotas protegidas incluindo no cabeçalho:

```
Authorization: Bearer seu_token_aqui
```
