<h1 align="center">
  Task Manager API
</h1>

## Sobre o Projeto

API RESTful para gerenciamento de tarefas construída com JSON Server, oferecendo endpoints CRUD completos sem necessidade de configuração de banco de dados tradicional. Desenvolvida para deploy serverless na Vercel, permitindo inicialização rápida de projetos que necessitam de backend para gerenciamento de tasks com categorização por período (manhã, tarde, noite) e controle de status.

---

## Funcionalidades

- **CRUD Completo** - Criação, leitura, atualização e exclusão de tarefas
- **Categorização Temporal** - Organização de tarefas por período do dia (morning, afternoon, evening)
- **Controle de Status** - Gerenciamento de estados (not_started, done, completed)
- **API REST Padrão** - Endpoints padronizados seguindo convenções REST
- **Deploy Serverless** - Configurado para deploy automático na Vercel
- **Zero Configuração** - Banco de dados em arquivo JSON, sem setup adicional

---

## Tecnologias

### Backend
- **[JSON Server](https://github.com/typicode/json-server)** - Framework para criação de API REST fake com base em arquivos JSON
- **[Node.js](https://nodejs.org/)** - Runtime JavaScript para execução do servidor

### DevOps & Ferramentas
- **[Vercel](https://vercel.com/)** - Plataforma de deploy serverless com configuração otimizada
- **[Yarn](https://yarnpkg.com/)** - Gerenciador de dependências

---

## Estrutura do Projeto

```
task-manager-api/
├── api/
│   └── server.js          # Configuração do servidor JSON Server
├── db.json                # Base de dados JSON com tasks
├── package.json           # Dependências e scripts
└── vercel.json            # Configuração de deploy Vercel
```

---

## Endpoints da API

### Tasks

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET | `/tasks` | Lista todas as tarefas |
| GET | `/tasks/:id` | Busca tarefa por ID |
| POST | `/tasks` | Cria nova tarefa |
| PUT | `/tasks/:id` | Atualiza tarefa completa |
| PATCH | `/tasks/:id` | Atualiza campos específicos |
| DELETE | `/tasks/:id` | Remove tarefa |

### Estrutura de Dados

```json
{
  "id": "uuid",
  "title": "string",
  "description": "string",
  "time": "morning | afternoon | evening",
  "status": "not_started | done | completed"
}
```

---

## Instalação e Uso

```bash
# Instalar dependências
yarn install

# Executar servidor local (porta 3000)
yarn start
```

A API estará disponível em `http://localhost:3000`

---

## Deploy

O projeto está configurado para deploy automático na Vercel. Basta conectar o repositório e fazer push para a branch principal.

---

## English Version

### About

RESTful API for task management built with JSON Server, providing complete CRUD endpoints without traditional database setup. Designed for serverless deployment on Vercel, enabling rapid project initialization for task management backends with time-period categorization (morning, afternoon, evening) and status tracking.

### Features

- **Full CRUD Operations** - Create, read, update, and delete tasks
- **Time-Based Categorization** - Task organization by day period (morning, afternoon, evening)
- **Status Management** - State control (not_started, done, completed)
- **Standard REST API** - Endpoints following REST conventions
- **Serverless Deployment** - Configured for automatic Vercel deployment
- **Zero Configuration** - JSON file-based database with no additional setup

### Tech Stack

**Backend:** JSON Server, Node.js

**DevOps:** Vercel, Yarn

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/tasks` | List all tasks |
| GET | `/tasks/:id` | Get task by ID |
| POST | `/tasks` | Create new task |
| PUT | `/tasks/:id` | Update entire task |
| PATCH | `/tasks/:id` | Update specific fields |
| DELETE | `/tasks/:id` | Delete task |

### Installation

```bash
# Install dependencies
yarn install

# Run local server (port 3000)
yarn start
```

API will be available at `http://localhost:3000`
