
# Assignment 13 – FastAPI Calculator

A production‑ready FastAPI application with authentication, calculation logging, and near‑complete test coverage, with robust CI/CD, Docker support, and deployment readiness.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.11+
- Docker & Docker Compose
- PostgreSQL (local or containerized)

### Environment Variables
Create a `.env` file in the project root:

```env
DATABASE_URL=postgresql://postgres:postgres@db:5432/fastapi_db
JWT_SECRET=your_secret_key
```

---

## 🐳 Running with Docker

Build and start the stack:

```bash
docker compose up --build
```

This will:
- Start the FastAPI app on `http://localhost:8000`
- Start a Postgres database (`fastapi_db`)
- Initialize schema and seed a test user (`johndoe`)

---

## 🧪 Testing

### Unit & Integration Tests
Run inside your dev environment:

```bash
pytest --cov=app
```

Coverage reports are written to `htmlcov/`.

### End‑to‑End (E2E) Tests
E2E tests simulate real user flows (register, login, run calculations):

```bash
pytest tests/e2e
```

These require the app and database containers to be running.

---

## 🎨 Front‑End

The project includes a simple front‑end served by FastAPI templates.  
To run locally without Docker:

```bash
uvicorn app.main:app --reload
```

Visit `http://localhost:8000` in your browser.

---

## 🔗 Docker Hub

The latest image is published here:  
👉 [Docker Hub – danatryon/assignment13](https://hub.docker.com/r/your‑repo/assignment13)

Pull it directly:

```bash
docker pull danatryon/assignment13:latest
```

---

## ✅ Features
- User registration & JWT authentication
- Calculator with addition, subtraction, multiplication, division
- Calculation logs persisted in Postgres
- 98%+ pytest coverage
- CI/CD pipeline with security checks
- Dockerized deployment

---

## 📂 Project Structure
```
app/
  ├── auth/          # JWT & dependencies
  ├── models/        # SQLAlchemy models
  ├── schemas/       # Pydantic schemas
  ├── operations/    # Business logic
  ├── main.py        # FastAPI entrypoint
tests/
  ├── unit/          # Unit tests
  ├── integration/   # Integration tests
  └── e2e/           # End-to-end tests
```

---

