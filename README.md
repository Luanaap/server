# NLW Agents

Este projeto foi desenvolvido durante o evento **NLW da Rocketseat**.

## Descrição

API backend para gerenciamento de salas, utilizando Fastify, Drizzle ORM e PostgreSQL.

## Tecnologias e Bibliotecas Principais

- **Node.js** + **TypeScript**
- **Fastify**: Framework web para Node.js
- **Drizzle ORM**: ORM para integração com banco de dados PostgreSQL
- **Zod**: Validação de esquemas e tipos
- **fastify-type-provider-zod**: Integração de validação Zod com Fastify
- **@fastify/cors**: Middleware CORS para Fastify
- **postgres**: Cliente PostgreSQL para Node.js
- **drizzle-kit**: Ferramenta de migrations e geração de schema
- **drizzle-seed**: Seed de dados para o banco
- **Biome**: Linter e formatter de código

## Padrões de Projeto e Arquitetura

- **Camada de rotas**: Organizada em `src/http/routes`
- **Validação de dados**: Utiliza Zod para schemas e validação
- **ORM**: Drizzle ORM para manipulação de dados e migrations
- **Configuração por ambiente**: Variáveis de ambiente validadas via Zod
- **Migrations e Seeds**: Automatizados com Drizzle Kit e Drizzle Seed
- **Banco de dados**: PostgreSQL, com suporte a inicialização via Docker

## Setup e Configuração

### Pré-requisitos

- Node.js 18+
- Docker (para banco de dados local)

### Instalação

```bash
npm install

docker-compose up -d

# Configure as variáveis de ambiente em um arquivo .env
# Exemplo:
# DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### Migrations e Seed

```bash
npx drizzle-kit migrate

npm run db:seed
```

### Rodando o servidor

```bash
npm run dev

npm start
```

## Observações

- O projeto utiliza **Biome** para lint e formatação de código.
- O banco de dados padrão é PostgreSQL, configurado para rodar em Docker.
- As rotas principais estão em `src/http/routes`.
