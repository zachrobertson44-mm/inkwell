# Inkwell – A Cosy Creative Platform for Writers

A full-stack writing platform where creators can share stories, poetry, essays, and more in a warm, editorial environment.

## Tech Stack

- **Frontend:** React + Vite
- **Backend:** Node.js + Express
- **Database:** SQLite (via better-sqlite3)
- **Auth:** JWT tokens stored in localStorage
- **Styling:** Plain CSS (warm aesthetic, no Tailwind)

## Features

- User authentication (sign up, login, JWT)
- Write and publish posts with genre tags (fiction, poetry, essay, true story, opinion)
- Like and comment on posts
- Follow writers
- Home feed with filtering and search
- User profiles with follower count
- Featured posts section
- Trending sidebar

## Design System

- **Colors:** Cream (#FAF7F2), Ink (#1A1610), Blush (#C4956A)
- **Typography:** Lora (serif) for headings/body, DM Sans for UI
- **Vibe:** Warm, editorial, like a cosy bookshop

## Project Structure

```
/client          — React + Vite frontend
/server          — Express backend
  /db.js         — SQLite schema setup
  /routes        — API endpoints
  /middleware    — Auth, validation, etc.
```

## Setup Instructions

### Prerequisites

- Node.js 16+
- npm or yarn

### Backend Setup

```bash
cd server
npm install
npm start
# Server runs on http://localhost:5000
```

### Frontend Setup

```bash
cd client
npm install
npm run dev
# App runs on http://localhost:5173
```

### Database

SQLite database initializes automatically on first server startup. Schema is created in `/server/db.js`.

## API Endpoints

See `/server/routes` for complete API documentation.

### Core Endpoints

- `POST /api/auth/signup` – Create user account
- `POST /api/auth/login` – User login
- `POST /api/posts` – Create post
- `GET /api/posts` – List all posts (with filters)
- `GET /api/posts/:id` – Get single post
- `POST /api/posts/:id/like` – Like post
- `POST /api/posts/:id/comments` – Add comment
- `GET /api/users/:id` – Get user profile
- `POST /api/users/:id/follow` – Follow user

## License

MIT
