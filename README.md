# Holdeye

![Holdeye Logo](logo.png)

## 📌 Project Overview

**Holdeye** is a full-stack web application designed to track and manage crypto and NFT investments. It enables users to create and monitor multiple portfolios across different investment strategies (trading, staking, liquidity pools, ICOs, etc.). With real-time data, advanced analytics, and an intuitive dashboard, Holdeye offers a powerful and user-friendly experience for active investors.

---

## 🚀 Features

- **Multi-Portfolio Management** – Create multiple investment portfolios, organized by strategy or asset type.
- **Real-Time Tracking** – Access live data and performance metrics for crypto and NFT holdings.
- **Advanced Analytics** – Visualize key statistics, trends, and portfolio allocations with detailed graphs.
- **All-in-One Dashboard** – Monitor historical performance, liquidity, balance distribution, and more.
- **Cross-Device Access** – Seamless experience across desktop and mobile platforms.

---

## 🛠️ Tech Stack

### Backend
- **Framework**: [Fastify](https://www.fastify.io/)
- **ORM**: [Prisma](https://www.prisma.io/)
- **Database**: PostgreSQL
- **Authentication**: JWT
- **API Docs**: Swagger
- **Deployment**: Docker, Docker Compose, Serverless (AWS Lambda)

### Frontend
- **Framework**: [React](https://reactjs.org/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Routing**: React Router
- **State Management**: React Context API
- **Real-Time Communication**: WebSocket
- **Styling**: CSS Modules
- **i18n**: Internationalization support
- **Tooling**: ESLint, Prettier, TypeScript
- **Deployment**: Static Hosting (S3, CloudFront)

### DevOps
- **CI/CD**: GitHub Actions
- **Containers**: Docker
- **Orchestration**: Docker Compose
- **Version Control**: Git

---

## 🗂️ Project Structure

```
holdeye/
├── README.md
├── backend/
│   ├── app/
│   │   ├── app.ts
│   │   ├── env/.env_example
│   │   └── src/ (routes, services, middleware, etc.)
│   ├── prisma/
│   │   ├── schema.prisma
│   │   └── .env_example
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── serverless.yml
│   └── usefull-scripts/
├── frontend/
│   ├── public/locales/
│   ├── src/
│   │   ├── App.tsx
│   │   ├── components/
│   │   ├── routes/
│   ├── Dockerfile
│   └── vite.config.ts
└── .github/workflows/
    ├── ci-frontend.yml
    └── cd-frontend-deployment.yml
```

---

## 📦 Prerequisites

Make sure you have the following tools installed:

- **Node.js** ≥ 18.x  
- **npm** ≥ 8.x or **yarn**  
- **Docker** ≥ 20.10  
- **Docker Compose** ≥ 1.29  
- **Serverless CLI** (optional, for AWS Lambda deployments)

```bash
npm install -g serverless
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/holdeye.git
cd holdeye
```

### 2. Install Dependencies

- **Backend**:
  ```bash
  cd backend
  npm install
  ```
- **Frontend**:
  ```bash
  cd ../frontend
  npm install
  ```

### 3. Environment Variables

- **Backend**:
  ```bash
  cp backend/app/env/.env_example backend/app/env/.env
  cp backend/prisma/.env_example backend/prisma/.env
  ```
- **Frontend**:
  Set API base URL and other configs in `.env` or `frontend/config/stages-urls.json`.

---

## 🧪 Running the Project

### Backend (Node.js)

```bash
cd backend
npm run dev
# API available at http://localhost:3000
```

### Frontend (Vite)

```bash
cd frontend
npm run dev
# App running at http://localhost:5173
```

### Using Docker (Backend)

```bash
cd backend/usefull-scripts
./start-docker.sh          # Starts backend + PostgreSQL containers
./init-docker.sh           # Runs Prisma generation, migration & seeding
```

---

## 🔁 Useful Scripts

### Backend

| Command                  | Description                                  |
|--------------------------|----------------------------------------------|
| `npm run dev`            | Start Fastify dev server (with watch)        |
| `npm run prisma:generate`| Generate Prisma client                       |
| `npm run prisma:migrate` | Run migrations                               |
| `npm run prisma:seed`    | Seed initial data                            |
| `npm run lint:check`     | Lint code                                    |
| `npm run format:check`   | Check formatting with Prettier               |

### Frontend

| Command           | Description                        |
|-------------------|------------------------------------|
| `npm run dev`     | Start Vite dev server              |
| `npm run build`   | Build production bundle            |
| `npm run preview` | Preview production build locally   |

### Docker Scripts (backend/usefull-scripts)

| Script               | Description                                  |
|----------------------|----------------------------------------------|
| `start-docker.sh`    | Start containers (API + DB)                  |
| `stop_docker.sh`     | Stop and remove containers                   |
| `init-docker.sh`     | Run migrations, seed DB, and start services  |
| `generate-local.sh`  | Prisma generate (local setup)                |
| `migrate-local.sh`   | Prisma migrate (local setup)                 |

---

## 🧪 GitHub Workflows

- **`ci-frontend.yml`** – Frontend build and test pipeline
- **`cd-frontend-deployment.yml`** – Continuous deployment (e.g., to S3 or CloudFront)

---

## 🤝 Contributing

Want to contribute? Feel free to fork the repo and open a pull request. We welcome contributions of all kinds — code, bugs, docs, and feedback.

---

## 📄 License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for more details.