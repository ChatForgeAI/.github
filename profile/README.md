<div align="center">

# ChatForge AI

### Forge Better Conversations

[![Organization](https://img.shields.io/badge/Organization-ChatForgeAI-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ChatForgeAI)
[![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)](https://nestjs.com/)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-v18+-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Supported-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://whatsapp.com/)

---

An AI-powered customer service platform that learns from your business data.

**Connect** · **Automate** · **Scale**

[Explore Repositories](#repositories) · [View Architecture](#architecture) · [Quick Start](#quick-start) · [Documentation](#documentation)

</div>

---

## What is ChatForge AI?

ChatForge AI is a complete, multi-tenant customer service automation platform. It enables businesses to deploy AI-powered chat agents across WhatsApp, Telegram, Messenger, and custom APIs — all trained on their own knowledge base.

The platform is built on three core services working together: a **React dashboard** for management, a **NestJS backend** for AI-powered message processing, and a **WhatsApp microservice** for multi-session messaging. Together, they provide everything businesses need to automate customer support with AI that actually understands their products, policies, and workflows.

Currently optimized for **Arabic and English** with professional tone and clarity, ChatForge AI is designed to scale globally with additional language support.

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  ┌──────────────┐      ┌──────────────┐      ┌──────────────┐      │
│  │              │      │              │      │              │      │
│  │   Dashboard  │─────▶│   Backend    │◀────▶│   Service    │      │
│  │   (React)    │      │   (NestJS)   │      │  (Baileys)   │      │
│  │              │      │              │      │              │      │
│  └──────────────┘      └──────────────┘      └──────────────┘      │
│         │                     │                     │               │
│         │                     │                     │               │
│         ▼                     ▼                     ▼               │
│  ┌──────────────┐      ┌──────────────┐      ┌──────────────┐      │
│  │              │      │              │      │              │      │
│  │  Management  │      │  AI + RAG    │      │  WhatsApp    │      │
│  │  & Analytics │      │  Processing  │      │  Multi-Session│      │
│  │              │      │              │      │              │      │
│  └──────────────┘      └──────┬───────┘      └──────────────┘      │
│                               │                                     │
│                               ▼                                     │
│                        ┌──────────────┐                             │
│                        │              │                             │
│                        │   WhatsApp   │                             │
│                        │      API     │                             │
│                        │              │                             │
│                        └──────────────┘                             │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

| Component | Role | Repository |
|-----------|------|------------|
| **Dashboard** | Management UI, analytics, user/admin controls | [`chatforge-dashboard`](https://github.com/ChatForgeAI/chatforge-dashboard) |
| **Backend** | AI processing, RAG, API, multi-tenant data | [`chatforge-backend`](https://github.com/ChatForgeAI/chatforge-backend) |
| **Service** | WhatsApp multi-session, QR auth, message bridge | [`chatforge-service`](https://github.com/ChatForgeAI/chatforge-service) |

---

## Repositories

### ChatForge Dashboard

> Modern React dashboard for managing AI customer service

[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=white)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)

A production-ready dashboard with role-based access, real-time messaging, FAQ management, and a cyberpunk-inspired landing page.

**Key Features:**
- Role-based admin and user views
- Real-time messaging with search
- FAQ management (CRUD)
- User administration
- Profile and settings management
- Dark + Neon/Cyberpunk landing page
- Docker deployment ready

```bash
git clone https://github.com/ChatForgeAI/chatforge-dashboard.git
cd chatforge-dashboard && npm install && npm run dev
```

[View Repository →](https://github.com/ChatForgeAI/chatforge-dashboard)

---

### ChatForge Backend

> AI-powered NestJS backend with RAG for intelligent customer service

[![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)](https://nestjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Gemini AI](https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=google-gemini&logoColor=white)](https://ai.google.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)

A sophisticated multi-tenant backend with Gemini AI integration, RAG implementation, and Arabic-optimized prompts.

**Key Features:**
- RAG-based AI responses using business FAQs
- Arabic and English support
- Multi-tenant architecture
- Smart intent detection (greetings, farewells)
- Dynamic escalation for unknown responses
- JWT authentication
- Docker deployment ready

```bash
git clone https://github.com/ChatForgeAI/chatforge-backend.git
cd chatforge-backend && npm install && npm run start:dev
```

[View Repository →](https://github.com/ChatForgeAI/chatforge-backend)

---

### ChatForge Service

> Multi-session WhatsApp microservice with AI auto-reply bridge

[![Node.js](https://img.shields.io/badge/Node.js-v18+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Baileys](https://img.shields.io/badge/Baileys-WhatsApp-25D366?style=flat-square&logo=whatsapp&logoColor=white)](https://github.com/WhiskeySockets/Baileys)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)

A high-performance Node.js service for managing multiple WhatsApp accounts simultaneously with automatic AI responses.

**Key Features:**
- Multi-session architecture (multiple WhatsApp accounts)
- AI auto-reply bridge to backend
- QR code authentication
- Real-time session status tracking
- Persistent session storage
- Automatic retry and reconnection
- Docker deployment ready

```bash
git clone https://github.com/ChatForgeAI/chatforge-service.git
cd chatforge-service && npm install && npm run dev
```

[View Repository →](https://github.com/ChatForgeAI/chatforge-service)

---

## Tech Stack

### Frontend

| Technology | Purpose |
|------------|---------|
| React 18 | UI framework |
| TypeScript 5.8 | Type safety |
| Vite 5 | Build tool |
| Tailwind CSS 3.4 | Styling |
| shadcn/ui | Component library |
| TanStack Query | Data fetching |
| React Router v6 | Routing |
| Recharts | Charts & analytics |

### Backend

| Technology | Purpose |
|------------|---------|
| NestJS | Framework |
| MongoDB + Mongoose | Database |
| Gemini AI | Language model |
| Passport.js + JWT | Authentication |
| class-validator | Validation |
| LangChain | RAG orchestration |

### WhatsApp Service

| Technology | Purpose |
|------------|---------|
| Node.js | Runtime |
| Express.js | HTTP framework |
| Baileys | WhatsApp Web API |
| MongoDB | Session storage |
| Winston | Logging |

### Infrastructure

| Technology | Purpose |
|------------|---------|
| Docker | Containerization |
| Docker Compose | Multi-service orchestration |
| Nginx | Static file serving |
| GitHub Actions | CI/CD (planned) |

---

## Quick Start

### Prerequisites

- Node.js v18+
- MongoDB (local or Atlas)
- Docker & Docker Compose (optional)
- Gemini API Key

### Clone All Repositories

```bash
# Create workspace
mkdir chatforge && cd chatforge

# Clone all repositories
git clone https://github.com/ChatForgeAI/chatforge-dashboard.git
git clone https://github.com/ChatForgeAI/chatforge-backend.git
git clone https://github.com/ChatForgeAI/chatforge-service.git
```

### Run with Docker (Recommended)

**Backend:**
```bash
cd chatforge-backend
docker compose up --build
# API runs at http://localhost:3000
```

**WhatsApp Service:**
```bash
cd chatforge-service
docker compose up --build -d
# Service runs at http://localhost:8000
```

**Dashboard:**
```bash
cd chatforge-dashboard
docker compose up --build
# Dashboard runs at http://localhost:3000
```

### Run in Development Mode

**Backend:**
```bash
cd chatforge-backend
cp .env.example .env  # Configure your environment
npm install
npm run start:dev
```

**WhatsApp Service:**
```bash
cd chatforge-service
cp .env.example .env  # Configure your environment
npm install
npm run dev
```

**Dashboard:**
```bash
cd chatforge-dashboard
npm install
npm run dev
```

---

## Environment Variables

### Backend (`chatforge-backend/.env`)

```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/chatforge
JWT_SECRET=your_super_secret_key
GEMINI_API_KEY=your_gemini_api_key
WHATSAPP_SERVICE_URL=http://localhost:8000/
```

### WhatsApp Service (`chatforge-service/.env`)

```env
DATABASE_URI=mongodb://localhost:27017/chatforge
PORT=8000
API_SECRET=your_secure_api_secret
MAX_QR_GENERATIONS=30
MESSAGES_API_URL=http://localhost:3000/v1/messages
```

### Dashboard

The dashboard uses `localStorage` for API configuration. Default endpoint:
```
https://api.chatforg.com
```

Change via the Settings page in the dashboard.

---

## Features

### AI-Powered Customer Service

| Feature | Description |
|---------|-------------|
| **RAG Implementation** | Retrieves business-specific knowledge (FAQs) to ground AI responses |
| **Arabic Optimization** | Tuned prompts for professional Arabic customer service |
| **Context Awareness** | Includes previous message history for conversation flow |
| **Smart Intent Detection** | Handles greetings and farewells without AI tokens |
| **Dynamic Escalation** | Detects unhelpful responses and escalates to human admin |

### Multi-Platform Support

| Platform | Status |
|----------|--------|
| WhatsApp | Live |
| Telegram | Coming Soon |
| Messenger | Coming Soon |
| Custom API | Live |

### Business Management

| Capability | Description |
|------------|-------------|
| **Multi-Tenant** | Each business manages their own knowledge base |
| **Knowledge Base** | Full CRUD for FAQs with AI integration |
| **User Roles** | Admin and user access levels |
| **Analytics** | Message traffic, user engagement, system performance |
| **Profile Management** | Edit profile, change password, account details |

### Dashboard Features

| Feature | Description |
|---------|-------------|
| **Real-Time Messaging** | Split-panel chat with search |
| **FAQ Management** | Create, edit, delete with accordion UI |
| **User Administration** | Data table with role management |
| **Settings** | API configuration with connection testing |
| **Landing Page** | 13-section cyberpunk design with animations |
| **Dark Mode** | Full theme support with toggle |

---

## API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/sign-in` | Authenticate user |
| POST | `/auth/sign-up` | Register new account |

### User Management
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/userMe` | Get current user profile |
| PATCH | `/userMe` | Update profile / password |
| GET | `/user` | List all users (Admin) |
| POST | `/user` | Create user (Admin) |
| PATCH | `/user/:id` | Update user (Admin) |
| DELETE | `/user/:id` | Delete user (Admin) |

### Messages
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/v1/messages` | Process incoming message |
| GET | `/messages` | List all messages (Admin) |
| GET | `/messages-user` | Get user's messages |

### FAQ
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/faq` | List all FAQs (Admin) |
| POST | `/faq` | Create FAQ |
| PATCH | `/faq/:id` | Update FAQ |
| DELETE | `/faq/:id` | Delete FAQ |
| GET | `/faq-user` | Get user's FAQs |

### WhatsApp Service
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/session/start-whatsapp-session` | Initialize WhatsApp session |
| GET | `/session/qr` | Get QR code for authentication |
| POST | `/session/restart-whatsapp-session` | Restart session |
| POST | `/session/terminate-whatsapp-session` | End session |

---

## Documentation

| Repository | Documentation |
|------------|---------------|
| Dashboard | [README](https://github.com/ChatForgeAI/chatforge-dashboard#readme) |
| Backend | [README](https://github.com/ChatForgeAI/chatforge-backend#readme) |
| Service | [README](https://github.com/ChatForgeAI/chatforge-service#readme) |

---

## Roadmap

- [x] WhatsApp integration
- [x] AI-powered responses with RAG
- [x] Multi-tenant architecture
- [x] React dashboard
- [x] Arabic language support
- [ ] Telegram integration
- [ ] Messenger integration
- [ ] Webhook support
- [ ] Analytics dashboard with Recharts
- [ ] Multi-language support (English, French, Spanish)
- [ ] Mobile app (React Native)
- [ ] Webhook integrations (Zapier, Slack)
- [ ] Advanced analytics & reporting

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository you want to contribute to
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please read the contributing guidelines in each repository before submitting.

---

## License

Each repository is licensed under its own license:

| Repository | License |
|------------|---------|
| Dashboard | [MIT](https://github.com/ChatForgeAI/chatforge-dashboard/blob/main/LICENSE) |
| Backend | [UNLICENSED](https://github.com/ChatForgeAI/chatforge-backend/blob/main/LICENSE) |
| Service | [ISC](https://github.com/ChatForgeAI/chatforge-service/blob/main/LICENSE) |

---

<div align="center">

### Built by Abd Alftah and the ChatForge AI Team

[![GitHub](https://img.shields.io/badge/GitHub-ChatForgeAI-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ChatForgeAI)

</div>
