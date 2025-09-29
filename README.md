# Todo List Full-Stack Application

A modern, full-stack todo list application built with Node.js, Express, PostgreSQL (Neon), and React.

## Features

- ✅ Create, read, update, and delete todos
- ✅ Mark todos as complete/incomplete
- ✅ RESTful API backend
- ✅ PostgreSQL database with Neon
- ✅ Real-time updates
- ✅ Responsive design

## Tech Stack

### Backend
- Node.js
- Express.js
- PostgreSQL (Neon Database)
- CORS enabled for cross-origin requests

### Frontend
- React
- Tailwind CSS
- Axios for API calls

## API Endpoints

### Backend API
Base URL: `https://backend-morphvm-2rpls558.http.cloud.morph.so`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/todos` | Get all todos |
| GET | `/api/todos/:id` | Get a specific todo |
| POST | `/api/todos` | Create a new todo |
| PUT | `/api/todos/:id` | Update a todo |
| PATCH | `/api/todos/:id/toggle` | Toggle todo completion |
| DELETE | `/api/todos/:id` | Delete a todo |
| GET | `/api/health` | Health check |

## Project Structure

```
todo-app/
├── backend/
│   ├── server.js         # Express server
│   ├── package.json      # Backend dependencies
│   └── .env             # Environment variables
├── frontend/
│   ├── src/
│   │   ├── App.js       # Main React component
│   │   ├── App.css      # Styles
│   │   └── index.js     # React entry point
│   └── package.json     # Frontend dependencies
└── README.md
```

## Getting Started

### Prerequisites
- Node.js (v20 or higher)
- npm

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file with your database URL:
```
DATABASE_URL=your_neon_database_url
PORT=3001
```

4. Start the server:
```bash
npm start
```

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

## Database Schema

```sql
CREATE TABLE todos (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  description TEXT,
  completed BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## License

MIT
