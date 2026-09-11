# Containerized Full-Stack MERN Application (Production & Development Architecture)

This project represents a fully containerized MERN stack application (Bloglist) - [GitHub Repository Link](https://github.com/Zenaldiry/Part5) - structured with dual environments for both rapid local development and strict, secure production deployments using Docker, Docker Compose, and Nginx.

## 🚀 Architecture & Tech Stack

- **Frontend:** React / Vite (served via Nginx in production, containerized dev setup for local work)
- **Backend:** Node.js & Express.js REST API (featuring automated test validation and multi-stage builds)
- **Database:** MongoDB (official container image with persistent volume)
- **Reverse Proxy:** Nginx (routes client requests, handles `/api/` proxying to the backend, and serves the frontend)
- **Orchestration:** Docker Compose (`docker-compose.yml` for production, `docker-compose.dev.yml` for development)
- **CI/CD & Testing:** GitHub Actions pipelines and automated E2E test suites.

---

## 📁 Project Structure

```text
my-app/
├── .github/
│   └── workflows/
│       └── e2e-tests.yml    # CI/CD Pipeline for testing and building
├── frontend/
│   ├── Dockerfile          # Production (Multi-stage + Nginx build)
│   └── dev.Dockerfile      # Local Development environment
├── backend/
│   ├── Dockerfile          # Production (Multi-stage + automated tests )
│   └── dev.Dockerfile      # Local Development environment
├── e2e_tests_by_playwright/   # End-to-end testing suite
├── nginx.conf              # Production Reverse Proxy config
├── nginx.dev.conf          # Development Reverse Proxy config
├── docker-compose.yml      # Production Orchestration
└── docker-compose.dev.yml  # Development Orchestration
```

Repository Link:https://github.com/Zenaldiry/Part5
