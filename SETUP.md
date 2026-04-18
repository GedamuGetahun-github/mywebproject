# Setup Guide

## Prerequisites
- Node.js 18+
- MongoDB (local or Atlas)
- Gmail account (for email notifications)

## Frontend Setup

No installation needed. Open `frontend/index.html` in any browser.

Works offline using localStorage. Connects to backend automatically when server is running.

## Backend Setup

```bash
cd backend
npm install
cp .env.example .env
```

Edit `.env` with your values:
- `MONGODB_URI` — your MongoDB connection string
- `JWT_SECRET` — any long random string
- `EMAIL_USER` / `EMAIL_PASS` — Gmail + App Password

```bash
npm run dev
# Server runs at http://localhost:3001
```

## Admin Dashboard

- URL: `frontend/admin/login.html`
- Username: `admin`
- Password: `gedamu2026` (change in `.env`)

## Deploy to Railway (Free)

1. Push to GitHub
2. Go to [railway.app](https://railway.app) → New Project → Deploy from GitHub
3. Set root directory to `backend`
4. Add environment variables from `.env`
5. Deploy

## Deploy Frontend to Netlify (Free)

1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the `frontend/` folder
3. Done — instant URL

## Environment Variables Reference

| Variable | Required | Description |
|---|---|---|
| `PORT` | No | Server port (default 3001) |
| `MONGODB_URI` | Yes | MongoDB connection string |
| `JWT_SECRET` | Yes | Secret for JWT tokens |
| `ADMIN_USERNAME` | Yes | Admin login username |
| `ADMIN_PASSWORD` | Yes | Admin login password |
| `EMAIL_USER` | No | Gmail address for notifications |
| `EMAIL_PASS` | No | Gmail App Password |
| `FRONTEND_URL` | No | Frontend URL for CORS |
