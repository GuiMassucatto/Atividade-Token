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
JWT_SECRET=sua_chave_secreta
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
  "email": "usuario@teste.com",
  "senha": "123456"
}
```

2. Copie o token retornado.

3. Acesse rotas protegidas incluindo no cabeçalho:

```
Authorization: Bearer seu_token_aqui
```

## Licença

Este projeto está licenciado sob a licença MIT.
