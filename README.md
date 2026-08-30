# 🧠 MentorMind 3.0

> **AI-Powered Project Management Platform**

[![Version](https://img.shields.io/badge/version-3.0-purple)](https://github.com/Suresh-Master001/MentorMind_V3.0)
[![Node](https://img.shields.io/badge/node-%3E%3D18-green)](https://nodejs.org)
[![MongoDB](https://img.shields.io/badge/MongoDB-7.0-green)](https://mongodb.com)
[![React](https://img.shields.io/badge/React-18-blue)](https://reactjs.org)
[![License](https://img.shields.io/badge/license-MIT-purple)](LICENSE)

---

## 📋 Overview

MentorMind 3.0 is a cutting-edge project management platform powered by Google Gemini AI. It automatically generates, assigns, and tracks tasks - transforming how teams collaborate and deliver projects. Built with a modern MERN stack (MongoDB, Express, React, Node.js) and real-time capabilities via Socket.io.

---

## ✨ Key Features

### 🤖 AI-Powered Capabilities
- **Smart Task Generation** - Describe your project once and get 6-12 detailed technical tasks with estimates, skills, and priorities
- **Intelligent Auto-Assignment** - Gemini AI scores team members across skill match (40%), time capacity (25%), workload (20%), and availability (15%)
- **Automated Delay Detection** - Cron-based monitoring sends alerts for overdue tasks

### 📊 Project Management
- **Role-Based Access** - Admin, Team Lead, and Member roles with tailored permissions
- **Real-Time Notifications** - Socket.io-powered instant updates for assignments, completions, and delays
- **Advanced Analytics** - Interactive dashboards with performance metrics, trend analysis, and team reports
- **Work Log Tracking** - Time tracking and progress monitoring per task

### 🔒 Enterprise-Grade Security
- JWT-based authentication with bcrypt password hashing
- Role-based access control (RBAC)
- Secure MongoDB data storage
- CORS and input validation

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18 + Vite, Tailwind CSS, Lucide Icons, Chart.js |
| **Backend** | Node.js + Express.js |
| **Database** | MongoDB (Mongoose ODM) |
| **AI Engine** | Google Gemini AI |
| **Real-Time** | Socket.io |
| **Auth** | JWT (JSON Web Tokens) |
| **Notifications** | Socket.io + Nodemailer |
| **Scheduling** | Node-cron |

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)
- Google Gemini API key

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/Suresh-Master001/MentorMind_V3.0.git
cd MentorMind_V3.0
```

#### 2. Server Setup
```bash
cd Server
npm install
cp .env.example .env
```

Edit `.env` with your credentials:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_google_gemini_api_key
```

#### 3. Client Setup
```bash
cd ../Client
npm install
cp .env.example .env
```

Edit `.env`:
```env
VITE_API_URL=http://localhost:5000/api
```

#### 4. Run the Application
```bash
# Terminal 1 - Server
cd Server
npm run dev

# Terminal 2 - Client
cd Client
npm run dev
```

Or use the batch runner:
```bash
run_all.bat
```

The app will be accessible at: **http://localhost:5173**

---

## 📁 Project Structure

```
MentorMind_V3.0/
├── Client/                    # React frontend (Vite)
│   ├── public/
│   │   └── MentorMind_Logo.png
│   ├── src/
│   │   ├── components/        # Reusable UI components
│   │   ├── context/           # React context providers (Auth)
│   │   ├── pages/             # Route pages
│   │   ├── services/          # API service layer
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── index.html
│   ├── tailwind.config.js
│   └── vite.config.js
│
├── Server/                    # Express backend
│   ├── config/                # DB configuration
│   ├── controllers/           # Route handlers
│   ├── middleware/            # Auth & role middleware
│   ├── models/                # Mongoose schemas
│   ├── routes/                # API route definitions
│   ├── services/              # Business logic (AI, cron, etc.)
│   ├── server.js              # Entry point
│   └── package.json
│
├── run_all.bat                # Batch launcher
└── README.md
```

---

## 👥 User Roles & Permissions

| Role | Capabilities |
|------|-------------|
| **Admin** | Full access - manage org, projects, users, reports |
| **Team Lead** | Create/manage projects & tasks, view analytics |
| **Member** | View assigned tasks, execute work, self-assign |

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/register` | Register new user |
| `POST` | `/api/auth/login` | Login |
| `GET` | `/api/projects` | List projects |
| `POST` | `/api/projects` | Create project |
| `GET` | `/api/tasks` | List tasks |
| `POST` | `/api/tasks/generate` | AI-generate tasks |
| `GET` | `/api/analytics` | Get analytics |
| `GET` | `/api/notifications` | Get notifications |

---

## 🌐 Live Demo

Visit the platform at: [MentorMind 3.0](https://mentormind-3-0.vercel.app)

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🏢 About MentorMind

**MentorMind 3.0** is an AI-powered project management platform designed to help teams plan, assign, and deliver work faster — from intelligent task generation to real-time collaboration.

- 🌐 Website: [mentormind.com](https://mentormind.com)
- 🔄 Smart task generation & auto-assignment
- 📊 Real-time collaboration & notifications
- 🔒 Advanced analytics & reporting
- 🔐 Role-based access control & security

---

<p align="center">
  Made with ❤️ by the <a href="https://mentormind.com">MentorMind</a> team
</p>