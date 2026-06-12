# Splitwise Clone

A simplified Splitwise-inspired expense sharing application.

## Features

* User Authentication
* Group Creation
* Expense Tracking
* Equal Expense Splitting
* Balance Summary
* Debt Settlement

## Tech Stack

**Backend:** Django, Django REST Framework, JWT auth

**Frontend:** React, TailwindCSS, Vite

**Database:** PostgreSQL (production) / SQLite (local dev)

## Setup

### Backend

```bash
cd backend
python -m venv venv

# Activate venv (pick the one that matches your Python install):
# MSYS2 / Git Bash on Windows:
source venv/bin/activate
# Standard Windows Python:
# venv\Scripts\activate

python -m pip install -r requirements.txt
copy .env.example .env         # Windows
# cp .env.example .env         # macOS/Linux
python manage.py migrate
python manage.py runserver
```

> **Note:** Use `python -m pip` instead of `pip` if `pip` is not recognized.
> For PostgreSQL on Render, use `requirements-prod.txt` (includes `psycopg2-binary`).

By default, `USE_SQLITE=True` uses a local SQLite database. For PostgreSQL locally, set `USE_SQLITE=False` in `.env` and configure `DB_*` variables.

### Frontend

```bash
cd frontend
npm install
copy .env.example .env
npm run dev
```

Open [http://localhost:5173](http://localhost:5173).

## Deployment

**Frontend (Vercel):** Deploy the `frontend/` directory. Set `VITE_API_URL` to your Render backend URL.

**Backend (Render):** Deploy the `backend/` directory using `render.yaml`. Set `CORS_ALLOWED_ORIGINS` to your Vercel URL.

## Author

Md Sahil
