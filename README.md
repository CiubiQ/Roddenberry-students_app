# FujiTech-students_app

This repository contains an app made by FujiTech students participating in mentoring program.

🚀 The purpose of this repository is to showcase the group work of students participating in mentoring sessions, where they develop a complete application (frontend and backend).
The application development is conducted under the guidance of a mentor, who is responsible for code review and organizing the workflow using the Scrum methodology (acting as the Scrum Master).

## 🛠 Tech stack:

- Vue 3
- TypeScript
- FastAPI
- vitest, playwright and pytest

## 🧑🏼‍💻 Methodology:

Scrum, 2 weeks sprints

## How to run the project:

1. Clone the repository
2. Install dependencies:

   # Install backend dependencies

   pip install -r backend/requirements.txt

   # Install frontend dependencies

   npm install --prefix frontend

3. Run backend:
   uvicorn backend.main:app --reload

4. Run frontend:
   npm run dev --prefix frontend

## API Communication

The frontend communicates with the backend through a proxy configuration:

- Frontend makes requests to `/api/*` endpoints
- Nuxt dev proxy forwards these requests to the backend
- Backend handles requests at root endpoints (without `/api` prefix)

Example:

- Frontend request to `/api/` → Backend handles at `/`
- Frontend runs on: `http://localhost:3000`
- Backend runs on: `http://localhost:8000`

> **Important:** Backend must be running before starting the frontend to ensure proper API communication.
