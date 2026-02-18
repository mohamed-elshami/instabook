<p align="center">
  <img src="instabook.svg" width="120" alt="Instabook Logo" />
</p>

# Instabook API

Backend API for **Instabook** — a social media platform (Facebook-like) built with [NestJS](https://nestjs.com). It provides REST APIs and real-time features (e.g. chat), uses **MongoDB** for data, and **Cloudinary** for images and videos. A **Next.js** frontend is planned to consume this API.

## Tech Stack

- **Framework:** NestJS 11
- **Database:** MongoDB (Mongoose)
- **Auth:** JWT (access + refresh)
- **Media:** Cloudinary (images & videos)
- **Real-time:** WebSockets (e.g. Socket.IO)

## Prerequisites

- Node.js (v18+)
- MongoDB (local or [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
- [Cloudinary](https://cloudinary.com) account (for uploads)

## Project Setup

```bash
# Install dependencies
npm install

# Copy environment template and fill in your values
cp .env.example .env
```

## Environment Variables

Create a `.env` file in the project root. Example variables:

| Variable | Description |
|----------|-------------|
| `PORT` | Server port (default: 3000) |
| `NODE_ENV` | `development` \| `production` |
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret for access tokens |
| `JWT_EXPIRES_IN` | Access token expiry (e.g. `7d`) |
| `REFRESH_TOKEN_SECRET` | Secret for refresh tokens |
| `REFRESH_TOKEN_EXPIRES_IN` | Refresh token expiry (e.g. `30d`) |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |
| `CORS_ORIGIN` | Allowed frontend origin (e.g. Next.js URL) |

## Running the App

```bash
# Development (watch mode)
npm run start:dev

# Production build
npm run build
npm run start:prod
```

Default base URL: `http://localhost:3000` (or the port set in `PORT`).

## Scripts

| Command | Description |
|---------|-------------|
| `npm run build` | Build for production |
| `npm run start` | Start (no watch) |
| `npm run start:dev` | Start in watch mode |
| `npm run start:prod` | Run production build |
| `npm run lint` | Run ESLint |
| `npm run test` | Run unit tests |
| `npm run test:e2e` | Run e2e tests |
| `npm run test:cov` | Run tests with coverage |

## Planned Features / Modules

- **Auth** — Register, login, JWT, refresh tokens
- **Users** — Profiles, avatar, follow/followers
- **Posts** — Create, edit, delete, feed, media
- **Comments** — Comments on posts
- **Reactions** — Likes/reactions on posts and comments
- **Upload / Media** — Cloudinary integration for images and videos
- **Chat** — Conversations and messages (REST + WebSocket)
- **Notifications** — In-app notifications (real-time via WebSocket)

## Frontend

The API is designed to be consumed by a **Next.js** frontend (to be built). Configure `CORS_ORIGIN` in `.env` to match your frontend URL.

## License

Private / Unlicensed.
