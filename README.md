# Containerized Full-Stack Development Environment (MERN Stack with Docker & Nginx)

This project represents the successful transformation of a standard MERN stack application (Bloglist) into a fully containerized local development environment. It utilizes Docker Compose, featuring hot-reloading, reverse proxy routing, and isolated persistent storage.

## 🚀 Architecture & Tech Stack

- **Frontend:** React / Vite (configured with containerized development setup)
- **Backend:** Node.js & Express.js REST API
- **Database:** MongoDB (official container image with persistent volume)
- **Reverse Proxy:** Nginx (routes client requests, handles `/api/` proxying to the backend, and serves the frontend)
- **Orchestration:** Docker Compose (`docker-compose.dev.yml`)

---

## 📁 Project Structure

```text
my-app/
├── frontend/
│   └── dev.Dockerfile
├── backend/
│   └── dev.Dockerfile
├── nginx.dev.conf
└── docker-compose.dev.yml
```

- [GitHub Repository Link](https://github.com/Zenaldiry/Part5)
