🚀 Imagify — AI Image Generation Platform

Imagify is a full-stack AI SaaS web application that allows users to generate images from prompts, manage usage credits, and track generation history.

Built with a modern React frontend, a secure Node.js/Express backend, and MongoDB for persistent storage.

🌐 Live Demo
Service	URL
Frontend (UI)	https://imagify-client-htfa.onrender.com

Backend (API)	https://imagify-server-pdqg.onrender.com

The frontend communicates with the backend via REST APIs.
Authentication is handled using JWT, and all protected operations require authorization.

🧠 Features

🎨 AI image generation using prompts

🔐 Secure JWT authentication

💳 Credit-based usage system

📜 Image generation history tracking

👤 User account verification

⚡ Fast UI built with React + Vite

🌍 Fully deployed production environment

🏗️ System Architecture
Browser
   ↓
React Frontend (Render Static Hosting)
   ↓ REST API
Node.js + Express Backend (Render Web Service)
   ↓
MongoDB Database
   ↓
AI Image Generation Provider






📂 Project Structure
imagify/
├── client/                  # React + Vite frontend
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   └── main.jsx
│
└── server/                  # Node.js + Express backend
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

User registers or logs in

Server returns a JWT token

Client stores token

Protected routes require token in Authorization header

Backend verifies token via middleware

💳 Credit System Logic

For each image generation request:

Check user credits

Deduct credits

Generate image via AI API

Store transaction in database

Return generated image URL

⚙️ Local Setup
Prerequisites

Node.js (v14+)

MongoDB

npm

Backend Setup
cd server
npm install


Create .env

MONGODB_URI=your_database_uri
JWT_SECRET=your_secret
AI_API_KEY=your_provider_key
CLIENT_URL=http://localhost:5173


Run server:

npm start

Frontend Setup
cd client
npm install


Create .env

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
Method	Endpoint	Description
POST	/api/users/register	Register user
POST	/api/users/login	Login user
GET	/api/users/profile	Get user profile
Image Routes
Method	Endpoint	Description
POST	/api/images/generate	Generate AI image
GET	/api/images/history	Fetch generation history
POST	/api/images/buy-credits	Purchase credits
🧪 Health Check
GET https://imagify-server-pdqg.onrender.com/


Expected response:

Server is running

⚡ Performance Notes

First request may take ~30 seconds (Render cold start)

AI generation latency depends on provider response time

Credit system prevents API misuse

🛠️ Future Improvements

Google / GitHub OAuth login

Image style presets

Prompt suggestions

Tier-based rate limiting

Stripe subscription billing

🤝 Contributing

Pull requests are welcome.
For major changes, please open an issue first to discuss improvements.

📄 License

MIT License

👨‍💻 Author

Full-stack production project demonstrating authentication, billing logic, API integration, and deployment architecture.
