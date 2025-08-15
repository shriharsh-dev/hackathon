# Skill Up India – AI-Powered Spoken English Practice Platform

Welcome to **Skill Up India**, a full-stack hackathon project designed to help users practice spoken English and soft skills through realistic, AI-driven conversations. The platform features a React frontend, a Spring Boot backend, and a FastAPI-based AI microservice powered by Google Gemini.

---

## 🗂️ Project Structure

```
hackathon/
│
├── ai-skill-up-india/           # Python FastAPI AI microservice (LLM, feedback, gamification)
│   ├── main.py
│   ├── feedback_utils.py
│   ├── models.py
│   ├── scenarios.py
│   ├── requirements.txt
│   ├── Dockerfile
│   ├── .env
│   └── root.crt
│
├── skill-up-india/              # Java Spring Boot backend API (session, scenario, proxy to AI)
│   ├── src/
│   ├── pom.xml
│   ├── Dockerfile
│   └── ...
│
├── react-skill-up-india-vite/   # React + Vite frontend (user interface)
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── Dockerfile
│   └── ...
│
├── docker-compose.yml           # Multi-container orchestration
└── README.md                    # You are here!
```

---

## 🚀 Quick Start

### 1. Prerequisites

- [Docker](https://www.docker.com/) & [Docker Compose](https://docs.docker.com/compose/)
- (Optional) [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) for local frontend dev
- (Optional) [Java 21+](https://adoptopenjdk.net/) and [Maven](https://maven.apache.org/) for backend dev

### 2. One-Command Launch (Recommended)

```sh
docker-compose up --build
```

- Frontend: [http://localhost:3000](http://localhost:3000)
- Backend API: [http://localhost:8080](http://localhost:8080)
- AI Service: [http://localhost:8000](http://localhost:8000)

---

## 🧩 Folder Details

### `ai-skill-up-india/`
- **Purpose:** Handles all AI/LLM logic, feedback, and gamification.
- **Tech:** Python 3.9, FastAPI, Google Gemini API.
- **Key Files:**
  - `main.py`: FastAPI app, `/process_turn` endpoint.
  - `feedback_utils.py`: LLM prompt construction & response parsing.
  - `models.py`: Pydantic models for API.
  - `scenarios.py`: Scenario definitions.
  - `requirements.txt`: Python dependencies.
  - `Dockerfile`: Container build.

### `skill-up-india/`
- **Purpose:** REST API backend, session management, scenario routing, proxy to AI service.
- **Tech:** Java 21, Spring Boot, Maven.
- **Key Files:**
  - `src/main/java/com/skillupbharat/api`: Controllers, DTOs, services.
  - `pom.xml`: Maven config.
  - `Dockerfile`: Container build.

### `react-skill-up-india-vite/`
- **Purpose:** Modern React frontend for user interaction.
- **Tech:** React 19, Vite, TypeScript, Bootstrap.
- **Key Files:**
  - `src/App.tsx`: Main UI logic.
  - `src/api.ts`: API calls to backend.
  - `Dockerfile`: Container build.

---

## 🛠️ Development

### Frontend (React)
```sh
cd react-skill-up-india-vite
npm install
npm run dev
```

### Backend (Spring Boot)
```sh
cd skill-up-india
./mvnw spring-boot:run
```

### AI Service (FastAPI)
```sh
cd ai-skill-up-india
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

---

## 🌟 Features

- **Scenario-based Conversations:** Choose from job interviews, retail, presentations, and more.
- **Real-time Feedback:** AI provides clarity, grammar, vocabulary, and pace scores, plus actionable tips.
- **Gamification:** Earn XP, badges, and track your progress.
- **Speech Recognition:** Speak or type your responses (browser support required).
- **Modern UI:** Responsive, clean, and easy to use.

---

## 🧑‍💻 Contributors

- Backend: Java, Spring Boot
- Frontend: React, TypeScript, Bootstrap
- AI: Python, FastAPI, Google Gemini

---
