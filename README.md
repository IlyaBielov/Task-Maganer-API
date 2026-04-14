# Task Manager API

A REST API for managing tasks, built with Express and MongoDB/Mongoose.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create a `.env` file in the root directory with your MongoDB connection string:
   ```
   MONGO_URI=your_mongodb_connection_string
   ```

3. Start the server:
   ```bash
   npm start
   ```

The server runs on port 3000 by default (configurable via `PORT` in `.env`).

## API Endpoints

| Method | Path               | Description     |
|--------|--------------------|-----------------|
| GET    | /api/v1/tasks      | List all tasks  |
| POST   | /api/v1/tasks      | Create a task   |
| GET    | /api/v1/tasks/:id  | Get single task |
| PATCH  | /api/v1/tasks/:id  | Update a task   |
| DELETE | /api/v1/tasks/:id  | Delete a task   |

## Project Structure

```
├── app.js                  # Entry point
├── controllers/tasks.js    # Route handlers
├── db/connect.js           # MongoDB connection
├── errors/custom-error.js  # Custom error class
├── middleware/
│   ├── async.js            # Async wrapper
│   ├── error-handler.js    # Error handling middleware
│   └── not-found.js        # 404 middleware
├── models/Task.js          # Mongoose schema
├── routes/tasks.js         # Route definitions
└── public/                 # Frontend (pre-built)
```

## Tech Stack

- Node.js
- Express
- MongoDB / Mongoose
