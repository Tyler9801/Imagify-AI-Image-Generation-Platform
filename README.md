🚀 Imagify — AI Image Generation Platform

Imagify is a full-stack AI SaaS-style web application that allows users to generate images using AI prompts, manage usage credits, and track generation history.
The platform is built with a modern React frontend, a secure Node.js/Express backend, and MongoDB for persistent storage.

🌐 Live Application

Frontend (UI)
https://imagify-client-htfa.onrender.com

Backend (API Server)
https://imagify-server-pdqg.onrender.com

The frontend communicates with the backend via REST APIs. Authentication is handled using JWT, and all protected operations require valid authorization.

🧠 Features

🎨 AI Image generation using prompts

🔐 Secure user authentication (JWT based)

💳 Credit-based usage system

📜 Image generation history tracking

👤 User account verification

⚡ Fast modern UI with React + Vite

🌍 Fully deployed production environment

🏗️ System Architecture
Browser
   ↓
React Frontend (Render Static Hosting)
   ↓ REST API Calls
Node.js + Express Backend (Render Web Service)
   ↓
MongoDB Database
   ↓
AI Image Generation Provider

📂 Project Structure
imagify/
├── client/                 # React + Vite frontend
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   └── main.jsx
│
└── server/                 # Node.js + Express backend
    ├── routes/
    ├── controllers/
    ├── models/
    ├── middlewares/
    ├── configs/
    └── server.js

🧰 Tech Stack
Frontend

React 18

Vite

Tailwind CSS

Context API

Backend

Node.js

Express.js

MongoDB (Mongoose)

JWT Authentication

REST API Architecture

🔐 Authentication Flow

User registers/logs in

Server returns JWT token

Client stores token

Protected routes require token in Authorization header

Backend verifies token via middleware

💳 Credit System Logic

Each image generation request:

Checks user credits

Deducts credits

Generates image via AI API

Stores transaction in database

Returns generated image URL

⚙️ Local Setup
Prerequisites

Node.js (v14+)

MongoDB

npm

Backend Setup
cd server
npm install


Create .env:

MONGODB_URI=your_database_uri
JWT_SECRET=your_secret
AI_API_KEY=your_provider_key
CLIENT_URL=http://localhost:5173


Run server:

npm start

Frontend Setup
cd client
npm install


Create .env:

VITE_API_URL=http://localhost:5000


Run:

npm run dev

🌍 Production Configuration

Frontend .env

VITE_API_URL=https://imagify-server-pdqg.onrender.com


Server .env

CLIENT_URL=https://imagify-client-htfa.onrender.com

📡 API Overview
User Routes
POST /api/users/register
POST /api/users/login
GET  /api/users/profile

Image Routes
POST /api/images/generate
GET  /api/images/history
POST /api/images/buy-credits

🧪 Health Check
GET https://imagify-server-pdqg.onrender.com/


Expected response:

Server is running

⚡ Performance Notes

First request may take ~30s (Render cold start)

AI generation latency depends on provider response time

Credit system prevents API misuse

🛠️ Future Improvements

Social login (Google/GitHub OAuth)

Image style presets

Prompt history suggestions

Rate limiting per user tier

Stripe subscription billing

🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss improvements.

📄 License

MIT License

👨‍💻 Author

Developed as a full-stack production project demonstrating authentication, payment logic, API integration, and deployment architecture.
