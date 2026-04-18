# API Documentation

Base URL: `http://localhost:3001/api`

## Authentication

All protected routes require: `Authorization: Bearer <token>`

---

## Auth Endpoints

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| POST | `/auth/signup` | Public | Register new user |
| POST | `/auth/signin` | Public | Login user |
| POST | `/auth/admin` | Public | Admin login |

### POST /auth/signup
```json
{ "name": "John", "email": "john@example.com", "password": "password123" }
```

### POST /auth/signin
```json
{ "email": "john@example.com", "password": "password123" }
```

---

## Repair Requests

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| POST | `/repairs` | User | Submit repair request |
| GET | `/repairs/mine` | User | Get own repairs |
| GET | `/repairs` | Admin | Get all repairs |
| PATCH | `/repairs/:id` | Admin | Update status/cost |
| DELETE | `/repairs/:id` | Admin | Delete repair |

---

## Reviews

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| GET | `/reviews` | Public | Get all reviews |
| POST | `/reviews` | User | Submit review |
| DELETE | `/reviews/:id` | Admin | Delete review |

---

## Messages

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| POST | `/messages` | Public | Send contact message |
| GET | `/messages` | Admin | Get all messages |
| PATCH | `/messages/:id/read` | Admin | Mark as read |
| DELETE | `/messages/:id` | Admin | Delete message |

---

## Stats

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| GET | `/stats` | Admin | Dashboard overview stats |

---

## Health Check

| Method | Endpoint | Auth | Description |
|---|---|---|---|
| GET | `/health` | Public | Server status |
