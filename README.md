<div align="center">

# 💰 Holdeye

**Full-stack platform to track, analyze, and manage crypto and NFT investments across multiple portfolios in real time**

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

**Holdeye** is a comprehensive full-stack web application designed to track and manage crypto and NFT investments. It enables users to create and monitor multiple portfolios across different investment strategies (trading, staking, liquidity pools, ICOs, etc.). With real-time data, advanced analytics, and an intuitive dashboard, Holdeye offers a powerful and user-friendly experience for active investors.

### Key Highlights

- 💼 **Multi-Portfolio Management** – Organize investments across multiple portfolios by strategy or asset type
- 📊 **Real-Time Analytics** – Live data and performance metrics for crypto and NFT holdings
- 📈 **Advanced Visualizations** – Detailed graphs and charts for portfolio analysis
- 🔄 **Real-Time Updates** – WebSocket integration for instant data synchronization
- 🚀 **Serverless Ready** – Deployable on AWS Lambda for scalable infrastructure
- 🐳 **Containerized** – Docker support for easy local development and deployment
- 🔒 **Secure** – JWT authentication and comprehensive security middleware
- 📱 **Responsive** – Modern UI built with React and Ant Design

---

## ✨ Features

### 💼 Portfolio Management
- ✅ Create and manage multiple investment portfolios
- ✅ Organize portfolios by strategy (trading, staking, liquidity pools, ICOs)
- ✅ Track assets by type (crypto, NFT)
- ✅ Portfolio performance tracking
- ✅ Historical data analysis

### 📊 Analytics & Tracking
- ✅ Real-time price tracking for crypto assets
- ✅ NFT collection monitoring
- ✅ Performance metrics and statistics
- ✅ Portfolio allocation visualization
- ✅ Balance distribution analysis
- ✅ Liquidity monitoring

### 📈 Dashboard Features
- ✅ All-in-one dashboard for comprehensive overview
- ✅ Interactive charts and graphs
- ✅ Key statistics visualization
- ✅ Trend analysis
- ✅ Customizable views

### 🔄 Real-Time Capabilities
- ✅ WebSocket integration for live updates
- ✅ Real-time price feeds
- ✅ Instant portfolio value updates
- ✅ Live transaction tracking

### 🔧 Backend Features
- ✅ RESTful API with Fastify
- ✅ Swagger/OpenAPI documentation
- ✅ JWT-based authentication
- ✅ Rate limiting and security headers
- ✅ Error handling and validation
- ✅ Database migrations with Prisma
- ✅ AWS DynamoDB integration for real-time data

### 🎨 Frontend Features
- ✅ Modern React application with TypeScript
- ✅ Responsive design with CSS Modules
- ✅ Internationalization (i18n) support
- ✅ Error boundaries and loading states
- ✅ Context-based state management
- ✅ Ant Design component library

---

## 🛠️ Tech Stack

### Backend

| Technology | Version | Purpose |
|------------|---------|---------|
| [Fastify](https://www.fastify.io/) | 5.0.0 | High-performance web framework |
| [Prisma](https://www.prisma.io/) | 5.22.0 | Next-generation ORM |
| [PostgreSQL](https://www.postgresql.org/) | Latest | Relational database |
| [AWS DynamoDB](https://aws.amazon.com/dynamodb/) | - | NoSQL database for real-time data |
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
| [Ant Design](https://ant.design/) | 5.19.3 | UI component library |
| [React Router](https://reactrouter.com/) | 6.25.1 | Client-side routing |
| [CSS Modules](https://github.com/css-modules/css-modules) | - | Scoped styling |
| [WebSocket](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket) | - | Real-time communication |

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
│                    Holdeye Architecture                       │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌──────────────┐      ┌──────────────┐      ┌──────────┐  │
│  │   React App  │◄─────►│  Fastify API │◄─────►│PostgreSQL│  │
│  │   (Vite)     │ HTTP  │  (Lambda)    │ Prisma│          │  │
│  └──────┬───────┘      └──────┬───────┘      └───────────┘  │
│         │                      │                              │
│         │ WebSocket            │                              │
│         │                      │                              │
│         │              ┌───────▼───────┐                      │
│         │              │   DynamoDB    │                      │
│         │              │ (Real-time)   │                      │
│         │              └───────────────┘                      │
│         │                                                      │
│         │              ┌───────────────┐                      │
│         └──────────────►│  Crypto APIs  │                      │
│                        │ (Price Data)  │                      │
│                        └───────────────┘                      │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

### Data Flow

1. **Frontend** → React app serves the UI and handles user interactions
2. **API Gateway** → Fastify routes handle HTTP requests and WebSocket connections
3. **Database Layer** → Prisma manages PostgreSQL connections for portfolio data
4. **Real-Time Storage** → DynamoDB stores real-time price and transaction data
5. **External APIs** → Integration with crypto/NFT price APIs for live data

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

### Crypto/NFT API Integration

Configure your crypto and NFT price API endpoints in the backend services. Update the API keys and endpoints in your environment variables.

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
│   │       │   └── health/           # Health check
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

#### Portfolio Endpoints

- `GET /portfolios` - List all portfolios
- `GET /portfolios/:id` - Get portfolio details
- `POST /portfolios` - Create a new portfolio
- `PUT /portfolios/:id` - Update a portfolio
- `DELETE /portfolios/:id` - Delete a portfolio
- `GET /portfolios/:id/transactions` - Get portfolio transactions

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
- [Ant Design](https://ant.design/) - UI component library
- [Vite](https://vitejs.dev/) - Next generation frontend tooling

---

<div align="center">

**Made with ❤️ to help you track and manage your crypto investments**

[⬆ Back to top](#-holdeye)

</div>
