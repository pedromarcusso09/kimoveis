# KImóveis

KImóveis é uma API RESTful desenvolvida em TypeScript utilizando Node.js, Express e TypeORM para gerenciar imóveis, categorias, usuários, sessões e agendamentos. O projeto segue boas práticas de arquitetura, separando responsabilidades em controllers, services, middlewares e repositórios.

## Funcionalidades

- Cadastro, listagem, atualização e remoção de usuários
- Autenticação de usuários (login)
- Cadastro e listagem de categorias de imóveis
- Cadastro e listagem de imóveis
- Agendamento de visitas a imóveis
- Controle de acesso por níveis de permissão (admin e usuário comum)

## Tecnologias Utilizadas

- Node.js
- TypeScript
- Express
- TypeORM
- PostgreSQL
- Jest (testes automatizados)

## Estrutura do Projeto

```
├── src/
│   ├── __tests__/           # Testes automatizados
│   ├── controllers/         # Lógica dos endpoints
│   ├── entities/            # Entidades do banco de dados
│   ├── interfaces/          # Tipagens e interfaces
│   ├── middlewares/         # Middlewares de validação e autenticação
│   ├── migrations/          # Migrations do banco de dados
│   ├── repositories/        # Repositórios customizados
│   ├── routers/             # Rotas da aplicação
│   ├── schemas/             # Schemas de validação
│   ├── services/            # Regras de negócio
│   ├── app.ts               # Configuração principal do Express
│   ├── data-source.ts       # Configuração do TypeORM
│   ├── server.ts            # Inicialização do servidor
│   └── error.ts             # Tratamento global de erros
├── package.json
├── tsconfig.json
├── jest.config.ts
└── README.md
```

## Como rodar o projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/pedromarcusso09/kimoveis
   cd kimoveis
   ```
2. **Instale as dependências:**
   ```bash
   npm install
   ```
3. **Configure o banco de dados:**
   - Crie um banco PostgreSQL e configure as variáveis de ambiente conforme necessário.
4. **Rode as migrations:**
   ```bash
   npm run typeorm migration:run
   ```
5. **Inicie o servidor:**
   ```bash
   npm run dev
   ```
6. **Execute os testes:**
   ```bash
   npm test
   ```

## Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```
DB_HOST=localhost
DB_PORT=5432
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_NAME=nome_do_banco
JWT_SECRET=sua_secret
```

## Testes

Os testes estão localizados na pasta `src/__tests__`. Utilize o comando `npm test` para executá-los.
