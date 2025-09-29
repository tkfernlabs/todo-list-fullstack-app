# Todo List Full-Stack Application

A modern, full-stack todo list application built with React, Node.js, and PostgreSQL (Neon).

## 🚀 Live Demo

- **Frontend**: https://frontend-prod-morphvm-2rpls558.http.cloud.morph.so
- **Backend API**: https://backend-morphvm-2rpls558.http.cloud.morph.so

## 📋 Features

- ✅ Create new todos with title and optional description
- ✅ View all todos in a clean, organized list
- ✅ Mark todos as complete/incomplete
- ✅ Edit existing todos
- ✅ Delete todos with confirmation
- ✅ Real-time updates
- ✅ Responsive design with Tailwind CSS v3
- ✅ RESTful API architecture
- ✅ PostgreSQL database with Neon

## 🛠️ Tech Stack

### Frontend
- **React** - UI framework
- **Vite** - Build tool and dev server
- **Tailwind CSS v3** - Styling framework
- **Axios** - HTTP client for API calls

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **PostgreSQL** - Database (hosted on Neon)
- **CORS** - Cross-origin resource sharing

## 📦 Project Structure

```
todo-app/
├── backend/
│   ├── server.js          # Express server and API routes
│   ├── package.json       # Backend dependencies
│   └── .env              # Environment variables (not in repo)
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   └── TodoList.jsx  # Main todo list component
│   │   ├── App.jsx           # Root component
│   │   ├── main.jsx          # Application entry point
│   │   └── index.css         # Tailwind CSS imports
│   ├── dist/                 # Production build files
│   ├── index.html            # HTML template
│   ├── vite.config.js        # Vite configuration
│   ├── tailwind.config.js    # Tailwind configuration
│   └── package.json          # Frontend dependencies
├── .gitignore
└── README.md
```

## 🔧 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/api/todos` | Get all todos |
| GET    | `/api/todos/:id` | Get a specific todo |
| POST   | `/api/todos` | Create a new todo |
| PUT    | `/api/todos/:id` | Update a todo |
| PATCH  | `/api/todos/:id/toggle` | Toggle todo completion |
| DELETE | `/api/todos/:id` | Delete a todo |
| GET    | `/api/health` | Health check |

## 📝 Todo Data Structure

```json
{
  "id": 1,
  "title": "string (required)",
  "description": "string (optional)",
  "completed": false,
  "created_at": "2025-09-29T20:54:18.146Z",
  "updated_at": "2025-09-29T20:54:18.146Z"
}
```

## 🚀 Local Development

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- PostgreSQL database (or Neon account)

### Backend Setup

1. Navigate to backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file with your database credentials:
   ```env
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

3. Start development server:
   ```bash
   npm run dev
   ```

4. Build for production:
   ```bash
   npm run build
   ```

5. Serve production build:
   ```bash
   npm install -g serve
   serve -s dist -l 5000
   ```

## 🗄️ Database Schema

```sql
CREATE TABLE todos (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    description TEXT DEFAULT '',
    completed BOOLEAN DEFAULT FALSE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## 🔒 Environment Variables

### Backend
- `DATABASE_URL` - Neon PostgreSQL connection string
- `PORT` - Server port (default: 3001)

## 🌐 CORS Configuration

The backend is configured to accept requests from any origin, making it easy to develop and deploy the frontend separately.

## 📱 Responsive Design

The application is fully responsive and works seamlessly on:
- Desktop computers
- Tablets
- Mobile phones

## 🎨 UI Features

- Clean, modern interface with gradient background
- Smooth animations and transitions
- Interactive hover states
- Visual feedback for all actions
- Loading states for async operations
- Error handling with user-friendly messages

## 🚢 Deployment

### Backend
- Deployed on Morph cloud infrastructure
- Running on port 3001
- Exposed via HTTPS

### Frontend
- Built with Vite for optimized production bundle
- Served using static file server
- Exposed via HTTPS

### Database
- Hosted on Neon (PostgreSQL)
- Automatic backups and scaling
- SSL/TLS encrypted connections

## 👥 Contributing

Feel free to fork this repository and submit pull requests with improvements!

## 📄 License

MIT License - feel free to use this project for personal or commercial purposes.

## 🙏 Acknowledgments

- Built with modern web development best practices
- Utilizes cloud-native technologies
- Optimized for performance and user experience

---

**Repository**: https://github.com/tkfernlabs/todo-list-fullstack-app

**Created**: September 2025
