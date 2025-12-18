<div align="center">

# 🗺️ Holdeye

**Interactive mapping and chat application with real-time capabilities**

[![TypeScript](https://img.shields.io/badge/TypeScript-5.6.0-blue?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-green?logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.3.1-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![Fastify](https://img.shields.io/badge/Fastify-5.0.0-000000?logo=fastify&logoColor=white)](https://www.fastify.io/)
[![Vite](https://img.shields.io/badge/Vite-5.3.1-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Prisma](https://img.shields.io/badge/Prisma-5.22.0-2D3748?logo=prisma&logoColor=white)](https://www.prisma.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Latest-336791?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![AWS](https://img.shields.io/badge/AWS-Lambda-FF9900?logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Docker](https://img.shields.io/badge/Docker-Latest-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[Features](#-features) • [Tech Stack](#-tech-stack) • [Installation](#-installation) • [Usage](#-usage) • [Contributing](#-contributing)

</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [API Documentation](#-api-documentation)
- [Development](#-development)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 About

**Holdeye** is a modern full-stack web application that combines interactive mapping capabilities with real-time chat functionality. Built with cutting-edge technologies, it provides a seamless user experience for geographic data visualization and communication.

### Key Highlights

- 🗺️ **Interactive Maps** – Powered by Leaflet and MapTiler for rich geographic visualization
- 💬 **Real-Time Chat** – WebSocket-based chat system with message persistence
- 🚀 **Serverless Ready** – Deployable on AWS Lambda for scalable infrastructure
- 🐳 **Containerized** – Docker support for easy local development and deployment
- 🔒 **Secure** – JWT authentication and comprehensive security middleware
- 📱 **Responsive** – Modern UI built with React and Ant Design

---

## ✨ Features

### 🗺️ Mapping Features
- ✅ Interactive map visualization with MapTiler integration
- ✅ Custom polygon drawing and editing
- ✅ Marker clustering and heat maps
- ✅ Geographic search functionality
- ✅ Custom scale controls and print capabilities

### 💬 Chat Features
- ✅ Real-time chat interface
- ✅ Message history persistence
- ✅ Multiple chat sessions support
- ✅ Typing indicators
- ✅ Message timestamps

### 🔧 Backend Features
- ✅ RESTful API with Fastify
- ✅ Swagger/OpenAPI documentation
- ✅ JWT-based authentication
- ✅ Rate limiting and security headers
- ✅ Error handling and validation
- ✅ Database migrations with Prisma
- ✅ AWS DynamoDB integration

### 🎨 Frontend Features
- ✅ Modern React application with TypeScript
- ✅ Responsive design with CSS Modules
- ✅ Internationalization (i18n) support
- ✅ Error boundaries and loading states
- ✅ Context-based state management

---

## 🛠️ Tech Stack

### Backend

| Technology | Version | Purpose |
|------------|---------|---------|
| [Fastify](https://www.fastify.io/) | 5.0.0 | High-performance web framework |
| [Prisma](https://www.prisma.io/) | 5.22.0 | Next-generation ORM |
| [PostgreSQL](https://www.postgresql.org/) | Latest | Relational database |
| [AWS DynamoDB](https://aws.amazon.com/dynamodb/) | - | NoSQL database for chat |
| [JWT](https://jwt.io/) | 9.0.2 | Authentication tokens |
| [Swagger](https://swagger.io/) | 9.1.0 | API documentation |
| [AWS Lambda](https://aws.amazon.com/lambda/) | - | Serverless deployment |
| [Docker](https://www.docker.com/) | Latest | Containerization |

### Frontend

| Technology | Version | Purpose |
|------------|---------|---------|
| [React](https://reactjs.org/) | 18.3.1 | UI library |
| [TypeScript](https://www.typescriptlang.org/) | 5.2.2 | Type-safe JavaScript |
| [Vite](https://vitejs.dev/) | 5.3.1 | Build tool and dev server |
| [Leaflet](https://leafletjs.com/) | 1.9.4 | Interactive maps |
| [MapTiler](https://www.maptiler.com/) | 4.0.2 | Map tiles provider |
| [Ant Design](https://ant.design/) | 5.19.3 | UI component library |
| [React Router](https://reactrouter.com/) | 6.25.1 | Client-side routing |
| [CSS Modules](https://github.com/css-modules/css-modules) | - | Scoped styling |

### DevOps & Tools

| Technology | Purpose |
|------------|---------|
| [Docker Compose](https://docs.docker.com/compose/) | Multi-container orchestration |
| [ESLint](https://eslint.org/) | Code linting |
| [Prettier](https://prettier.io/) | Code formatting |
| [GitHub Actions](https://github.com/features/actions) | CI/CD pipelines |
| [Serverless Framework](https://www.serverless.com/) | AWS Lambda deployment |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                      Holdeye Architecture                      │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌──────────────┐      ┌──────────────┐      ┌──────────┐  │
│  │   React App  │◄─────►│  Fastify API │◄─────►│PostgreSQL│  │
│  │   (Vite)     │ HTTP  │  (Lambda)    │ Prisma│          │  │
│  └──────┬───────┘      └──────┬───────┘      └───────────┘  │
│         │                      │                              │
│         │                      │                              │
│         │              ┌───────▼───────┐                      │
│         │              │   DynamoDB    │                      │
│         │              │   (Chat Data)  │                      │
│         │              └───────────────┘                      │
│         │                                                      │
│         │              ┌───────────────┐                      │
│         └──────────────►│  MapTiler API │                      │
│                        │  (Map Tiles)  │                      │
│                        └───────────────┘                      │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

### Data Flow

1. **Frontend** → React app serves the UI and handles user interactions
2. **API Gateway** → Fastify routes handle HTTP requests
3. **Database Layer** → Prisma manages PostgreSQL connections
4. **Chat Storage** → DynamoDB stores chat messages
5. **Map Services** → MapTiler provides map tiles and geocoding

---

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** ≥ 18.x ([Download](https://nodejs.org/))
- **npm** ≥ 8.x or **yarn**
- **Docker** ≥ 20.10 ([Download](https://www.docker.com/get-started))
- **Docker Compose** ≥ 1.29
- **Serverless CLI** (optional, for AWS deployments)

```bash
npm install -g serverless
```

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/holdeye.git
cd holdeye
```

### 2. Install Dependencies

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd ../frontend
npm install
```

### 3. Environment Setup

**Backend Environment Variables:**

Create `backend/app/env/.env`:
```env
# Database Configuration
POSTGRES_USER=user
POSTGRES_PASSWORD=password
POSTGRES_DB=holdeye_db

# Network Configuration
API_PORT=3000
POSTGRES_PORT=5432
API_IP=172.20.0.3
POSTGRES_IP=172.20.0.2
PRISMA_IP=172.20.0.4
SUBNET=172.20.0.0/16

# Prisma Configuration
DOCKER_DATABASE_URL=postgresql://${POSTGRES_USER}:${POSTGRES_PASSWORD}@postgres:5432/${POSTGRES_DB}
LOCAL_DATABASE_URL=postgresql://${POSTGRES_USER}:${POSTGRES_PASSWORD}@localhost:5432/${POSTGRES_DB}

# JWT Configuration
JWT_SECRET=your-secret-key-here

# AWS Configuration
AWS_REGION=us-east-1
CHATS_TABLE=Chats

# API Base URL
API_BASE_URL=http://localhost:3000
```

**Prisma Environment:**

Create `backend/prisma/.env`:
```env
DATABASE_URL=postgresql://user:password@localhost:5432/holdeye_db
```

**Frontend Configuration:**

Update `frontend/config/stages-urls.json` with your API endpoints.

---

## ⚙️ Configuration

### Database Setup

1. **Start Docker containers:**
   ```bash
   cd backend/usefull-scripts
   ./start-docker.sh
   ```

2. **Initialize database:**
   ```bash
   ./init-docker.sh
   ```

This will:
- Generate Prisma client
- Run database migrations
- Seed initial data (if available)

### MapTiler Configuration

Update the MapTiler API key in `frontend/src/components/MapComponent.tsx`:

```typescript
const mtLayer = new MaptilerLayer({
  apiKey: "your-maptiler-api-key",
  style: "your-style-id",
});
```

---

## 💻 Usage

### Development Mode

**Backend:**
```bash
cd backend
npm run dev
# API available at http://localhost:3000
# Swagger docs at http://localhost:3000/docs
```

**Frontend:**
```bash
cd frontend
npm run dev
# App running at http://localhost:5173
```

### Docker Development

**Start all services:**
```bash
cd backend/usefull-scripts
./start-docker.sh          # Starts backend + PostgreSQL containers
./init-docker.sh           # Runs Prisma generation, migration & seeding
```

**Stop services:**
```bash
./stop_docker.sh
```

### Production Build

**Backend:**
```bash
cd backend
npm run deploy  # Deploy to AWS Lambda
```

**Frontend:**
```bash
cd frontend
npm run build   # Build production bundle
npm run preview # Preview production build locally
```

---

## 📁 Project Structure

```
holdeye/
│
├── 📄 README.md
├── 📄 LICENSE
│
├── 🐳 backend/
│   ├── app/
│   │   ├── app.ts                    # Fastify application entry point
│   │   ├── docker/
│   │   │   └── Dockerfile           # Backend Docker image
│   │   ├── env/                      # Environment variables
│   │   └── src/
│   │       ├── config/               # Configuration files
│   │       │   ├── cors.ts
│   │       │   ├── helmet.ts
│   │       │   ├── rate-limit.ts
│   │       │   └── swagger.ts
│   │       ├── entities/             # Type definitions
│   │       ├── enums/                # Enum definitions
│   │       ├── libs/                 # Utility libraries
│   │       ├── middlewares/          # Custom middlewares
│   │       ├── repositories/         # Data access layer
│   │       ├── routes/               # API routes
│   │       │   ├── chat/            # Chat endpoints
│   │       │   └── health/          # Health check
│   │       └── services/             # Business logic
│   │           ├── chat-service.ts
│   │           ├── dynamo-service.ts
│   │           └── jwt-service.ts
│   ├── prisma/
│   │   └── schema.prisma            # Database schema
│   ├── usefull-scripts/             # Utility scripts
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── serverless.yml               # AWS Lambda config
│   └── package.json
│
├── 🎨 frontend/
│   ├── public/
│   │   ├── locales/                 # i18n translations
│   │   └── data.geojson
│   ├── src/
│   │   ├── components/               # React components
│   │   │   ├── dashboardLayout/
│   │   │   ├── ErrorBoundary/
│   │   │   ├── MapComponent.tsx
│   │   │   ├── sidebar/
│   │   │   └── tchat/
│   │   ├── contexts/                 # React contexts
│   │   ├── routes/                   # Route definitions
│   │   ├── services/                 # API services
│   │   ├── views/                    # Page components
│   │   │   ├── chat/
│   │   │   ├── homeContent/
│   │   │   └── notFound/
│   │   ├── config/                   # Configuration
│   │   ├── utils/                    # Utility functions
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── config/
│   ├── Dockerfile
│   ├── vite.config.ts
│   └── package.json
│
└── .github/
    └── workflows/                    # CI/CD pipelines
        ├── ci-frontend.yml
        └── cd-frontend-deployment.yml
```

---

## 📚 API Documentation

### Swagger UI

Once the backend is running, access the interactive API documentation at:

```
http://localhost:3000/docs
```

### Available Endpoints

#### Chat Endpoints

- `POST /chat` - Create a new chat
- `GET /chat` - List all chats
- `PUT /chat/:chatId` - Update a chat

#### Health Check

- `GET /health` - Application health status

---

## 🔧 Development

### Available Scripts

#### Backend

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with hot reload |
| `npm run prisma:generate` | Generate Prisma client |
| `npm run prisma:migrate` | Run database migrations |
| `npm run prisma:seed` | Seed database with initial data |
| `npm run lint:check` | Check code with ESLint |
| `npm run lint:fix` | Fix ESLint errors |
| `npm run format:check` | Check code formatting |
| `npm run format:fix` | Format code with Prettier |
| `npm run typescript:check` | Type-check TypeScript |
| `npm run test:all` | Run all checks |
| `npm run deploy` | Deploy to AWS Lambda |

#### Frontend

| Command | Description |
|---------|-------------|
| `npm run dev` | Start Vite development server |
| `npm run build` | Build production bundle |
| `npm run preview` | Preview production build |
| `npm run lint:check` | Check code with ESLint |
| `npm run lint:fix` | Fix ESLint errors |
| `npm run format:check` | Check code formatting |
| `npm run format:fix` | Format code with Prettier |
| `npm run typescript:check` | Type-check TypeScript |
| `npm run test:all` | Run all checks |

### Docker Scripts

Located in `backend/usefull-scripts/`:

| Script | Description |
|--------|-------------|
| `start-docker.sh` | Start Docker containers (API + DB) |
| `stop_docker.sh` | Stop and remove containers |
| `init-docker.sh` | Run migrations, seed DB, and start services |
| `generate-local.sh` | Generate Prisma client (local setup) |
| `migrate-local.sh` | Run Prisma migrations (local setup) |

---

## 🚢 Deployment

### AWS Lambda (Serverless)

**Backend:**
```bash
cd backend
npm run deploy
```

### Static Hosting (Frontend)

The frontend can be deployed to:
- AWS S3 + CloudFront
- Vercel
- Netlify
- Any static hosting service

```bash
cd frontend
npm run build
# Deploy the 'build' directory
```

### Docker Deployment

```bash
# Build images
docker-compose build

# Start services
docker-compose up -d
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'feat: add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Commit Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

### Code Style

- Follow ESLint and Prettier configurations
- Write meaningful commit messages
- Add comments for complex logic
- Update documentation as needed

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Fastify](https://www.fastify.io/) - Fast and low overhead web framework
- [Prisma](https://www.prisma.io/) - Next-generation ORM
- [React](https://reactjs.org/) - UI library
- [Leaflet](https://leafletjs.com/) - Interactive maps
- [MapTiler](https://www.maptiler.com/) - Map tiles provider
- [Ant Design](https://ant.design/) - UI component library

---

<div align="center">

**Made with ❤️ by the Holdeye team**

[⬆ Back to top](#-holdeye)

</div>
