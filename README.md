# 💬 Real Time Chat Web application

<div align="center">

![Real Time Chat Web application](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Node](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg)
![MongoDB](https://img.shields.io/badge/database-MongoDB-green.svg)

**A full-stack, real-time chat platform powered by the MERN stack, with seamless messaging and robust JWT-based authentication.**

[🚀 Live Demo](https://smart-health-assistant-one.vercel.app) 

</div>

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Environment Variables](#-environment-variables)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Deployment](#-deployment)
- [Known Issues](#-known-issues)


## ✨ Features

### Authentication & Security
- 🔐 Secure JWT-based authentication
- 🔒 Password hashing with bcrypt
- 🍪 HTTP-only cookie storage for tokens
- 🛡️ Protected routes and middleware

### Messaging & Communication
- 💬 Real-time messaging with Socket.IO
- 👥 One-on-one private conversations
- 📷 Image and video sharing via Cloudinary
- 🟢 Online/offline user status indicators
- 📜 Message history persistence

### AI Health Assistant
- 🤖 AI-powered health chatbot


### User Experience
- 📱 Fully responsive design
- 🎨 Modern UI with Tailwind CSS
- 🔔 Real-time notifications
- 👤 Customizable user profiles
- 🖼️ Avatar upload support

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React 18 | UI Library |
| Redux Toolkit | State Management |
| React Router v6 | Routing |
| Tailwind CSS | Styling |
| Socket.IO Client | Real-time Communication |
| Axios | HTTP Client |
| Lucide React | Icons |
| React Toastify | Notifications |

### Backend
| Technology | Purpose |
|------------|---------|
| Node.js | Runtime Environment |
| Express.js | Web Framework |
| MongoDB | Database |
| Mongoose | ODM |
| Socket.IO | Real-time Communication |
| JWT | Authentication |
| Cloudinary | Media Storage |
| bcrypt | Password Hashing |

## 📁 Project Structure

```

├── frontend_SmartHealthAssistant/
│   ├── public/
│   │   └── avatar-holder.avif
│   ├── src/
│   │   ├── components/
│   │   │   ├── ChatBot/
│   │   │   │   ├── ChatbotButton.jsx
│   │   │   │   └── ChatbotWindow.jsx
│   │   │   ├── skeletons/
│   │   │   │   ├── MessageSkeleton.jsx
│   │   │   │   └── SidebarSkeleton.jsx
│   │   │   ├── ChatContainer.jsx
│   │   │   ├── ChatHeader.jsx
│   │   │   ├── MessageInput.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── NoChatSelected.jsx
│   │   │   └── Sidebar.jsx
│   │   ├── lib/
│   │   │   ├── axios.js
│   │   │   └── socket.js
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Profile.jsx
│   │   │   └── Register.jsx
│   │   ├── store/
│   │   │   ├── slices/
│   │   │   │   ├── authSlice.js
│   │   │   │   └── chatSlice.js
│   │   │   └── store.js
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── .env
│   ├── package.json
│   ├── tailwind.config.js
│   └── vite.config.js
│
├── backend_SmartHealthAssistant/
│   ├── config/
│   │   └── config.env
│   ├── controllers/
│   │   ├── messageController.js
│   │   └── userController.js
│   ├── database/
│   │   └── db.js
│   ├── lib/
│   │   └── socket.js
│   ├── middlewares/
│   │   ├── authMiddelware.js
│   │   └── catchAsyncError.js
│   ├── models/
│   │   ├── messageModel.js
│   │   └── userModel.js
│   ├── routes/
│   │   ├── messageRoute.js
│   │   └── userRoute.js
│   ├── utils/
│   │   └── jwtToken.js
│   ├── app.js
│   ├── server.js
│   └── package.json
│
└── README.md
```

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (v18.0.0 or higher)
- **npm** (v9.0.0 or higher) or **yarn**
- **MongoDB** (local installation or MongoDB Atlas account)
- **Cloudinary** account (for media storage)
- **Git** (for cloning the repository)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/SmartHealthAssistant.git
cd SmartHealthAssistant
```

### 2. Install Backend Dependencies

```bash
cd backend_SmartHealthAssistant
npm install
```

### 3. Install Frontend Dependencies

```bash
cd ../frontend_SmartHealthAssistant
npm install
```

## ⚙️ Environment Variables

### Backend Configuration

Create a `config.env` file in `backend_SmartHealthAssistant/config/`:

```env
# Server Configuration
PORT=4000
NODE_ENV=development

# Frontend URL
FRONTEND_URI=http://localhost:5173

# MongoDB Database
MONGO_URI=mongodb+srv://your_username:your_password@cluster.mongodb.net/smart_health_assistant

# JWT Authentication
JWT_SECRET_KEY=your_super_secret_jwt_key_here
JWT_EXPIRES=7d
COOKIE_EXPIRE=7

# Cloudinary Configuration
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# N8N Webhook (for AI Chatbot)
N8N_URL=your_n8n_webhook_url
```

### Frontend Configuration

Create a `.env` file in `frontend_SmartHealthAssistant/`:

```env
VITE_N8N_URL=your_n8n_webhook_url
```

## 🏃‍♂️ Running the Application

### Development Mode

**Terminal 1 - Start Backend:**
```bash
cd backend_SmartHealthAssistant
npm run dev
```

**Terminal 2 - Start Frontend:**
```bash
cd frontend_SmartHealthAssistant
npm run dev
```

### Production Mode

**Backend:**
```bash
cd backend_SmartHealthAssistant
npm start
```

**Frontend:**
```bash
cd frontend_SmartHealthAssistant
npm run build
npm run preview
```

### Access the Application

- **Frontend:** http://localhost:5173
- **Backend API:** http://localhost:4000


## 📚 API Documentation

### Authentication Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/user/sign-up` | Register a new user |
| POST | `/api/v1/user/sign-in` | Login user |
| GET | `/api/v1/user/sign-out` | Logout user |
| GET | `/api/v1/user/me` | Get current user |
| PUT | `/api/v1/user/update-profile` | Update user profile |

### Message Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/message/users` | Get all users for chat |
| GET | `/api/v1/message/:id` | Get messages with a user |
| POST | `/api/v1/message/send/:id` | Send a message |

### Request & Response Examples

#### Register User
```bash
POST /api/v1/user/sign-up
Content-Type: multipart/form-data

{
  "fullName": "John Doe",
  "email": "john@example.com",
  "password": "securepassword123",
  "avatar": <file>
}
```

#### Login User
```bash
POST /api/v1/user/sign-in
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securepassword123"
}
```

#### Send Message
```bash
POST /api/v1/message/send/:receiverId
Content-Type: multipart/form-data
Authorization: Bearer <token>

{
  "text": "Hello, how are you?",
  "media": <file> (optional)
}
```

## 🔌 Socket.IO Events

### Client Events (Emit)
| Event | Description |
|-------|-------------|
| `connection` | Connect to socket server |
| `disconnect` | Disconnect from socket server |

### Server Events (Listen)
| Event | Description |
|-------|-------------|
| `getOnlineUsers` | Get list of online user IDs |
| `newMessage` | Receive new message notification |


## ☁️ Deployment

### Deploy to Vercel

#### Backend Deployment

1. Push code to GitHub
2. Import project in [Vercel](https://vercel.com/)
3. Set root directory to `backend_SmartHealthAssistant`
4. Add environment variables in Vercel dashboard
5. Deploy!

#### Frontend Deployment

1. Update API URL in `frontend_SmartHealthAssistant/src/lib/axios.js`
2. Update the socket URL in `frontend_SmartHealthAssistant/src/lib/socket.js`
3. Import project in [Vercel](https://vercel.com/)
3. Set root directory to `frontend_SmartHealthAssistant`
4. Add environment variables: ``` VITE_N8N_URL=your_n8n_webhook_url ```
5. Deploy!

#### Post-Deployment Steps

1. Update `FRONTEND_URI` in backend environment variables with the deployed frontend URL
2. Test all functionality:
   - ✅ User registration and login
   - ✅ Real-time messaging
   - ✅ File uploads
   - ✅ AI chatbot
   - ✅ Online status indicators


## 🐛 Known Issues

- Large file uploads may take longer on slower connections
- Mobile keyboard may overlap chat input on some devices
- Socket.IO connections may require WebSocket fallback on some hosting platforms






