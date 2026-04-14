# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Starter scaffold for a Task Manager REST API. The frontend (in `public/`) is complete; the backend needs to be built. The goal is to implement an Express + Mongoose API that the pre-built frontend consumes.

## Commands

- **Start dev server:** `npm start` (runs `nodemon app.js`)
- **Install dependencies:** `npm install`

No test suite or linter is configured.

## Architecture

**Backend (to be built):** `app.js` is the entry point (currently a stub). The completed app should be an Express server serving static files from `public/` and exposing a REST API backed by MongoDB via Mongoose.

**Frontend (already complete):** Static HTML/CSS/JS in `public/` using Axios (loaded via CDN). Two pages:
- `index.html` + `browser-app.js` — task list with create/delete
- `task.html` + `edit-task.js` — single task edit form (navigated to via `?id=` query param)

## Expected API Endpoints

The frontend expects these routes under `/api/v1/tasks`:

| Method | Path               | Purpose         |
|--------|--------------------|-----------------|
| GET    | /api/v1/tasks      | List all tasks  |
| POST   | /api/v1/tasks      | Create a task   |
| GET    | /api/v1/tasks/:id  | Get single task |
| PATCH  | /api/v1/tasks/:id  | Update a task   |
| DELETE | /api/v1/tasks/:id  | Delete a task   |

Response shape: `{ tasks: [...] }` for list, `{ task: {...} }` for single. Task fields: `_id`, `name`, `completed`.

## Environment

A `.env` file (gitignored) is required for the MongoDB connection string (e.g., `MONGO_URI`).


DB Schema:
User: admin_db_user,
Password: kNt3v9sRIO4UndqQ
Link: mongodb+srv://admin_db_user:kNt3v9sRIO4UndqQ@cluster0.u5cwstt.mongodb.net/?appName=Cluster0
