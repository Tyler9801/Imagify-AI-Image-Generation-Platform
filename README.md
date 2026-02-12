# Imagify - AI Image Generation Platform

Imagify is a full-stack web application that leverages AI to generate, process, and manage images. It features a modern React frontend, a Node.js/Express backend, and MongoDB for data persistence.

## Project Structure

```
imagify/
├── client/                 # Frontend application (React + Vite)
│   ├── src/
│   │   ├── components/     # Reusable React components
│   │   │   ├── Description.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── GenerateBtn.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── Steps.jsx
│   │   │   └── Testimonials.jsx
│   │   ├── pages/          # Page components
│   │   │   ├── Home.jsx    # Landing page
│   │   │   ├── Result.jsx  # Image generation results
│   │   │   ├── BuyCredit.jsx # Credit purchase page
│   │   │   └── Verify.jsx  # User verification page
│   │   ├── context/        # React Context API
│   │   │   └── AppContext.jsx # Global state management
│   │   ├── assets/         # Static assets
│   │   │   └── assets.js
│   │   ├── App.jsx         # Main App component
│   │   ├── main.jsx        # Entry point
│   │   └── index.css       # Global styles
│   ├── public/             # Static files
│   ├── package.json        # Dependencies & scripts
│   ├── vite.config.js      # Vite configuration
│   ├── tailwind.config.js  # Tailwind CSS configuration
│   ├── postcss.config.js   # PostCSS configuration
│   ├── eslint.config.js    # ESLint configuration
│   └── vercel.json         # Deployment configuration
│
└── server/                 # Backend API (Node.js + Express)
    ├── routes/             # API endpoints
    │   ├── imageRoutes.js  # Image generation routes
    │   └── userRoutes.js   # User management routes
    ├── controllers/        # Business logic
    │   ├── imageController.js  # Image generation logic
    │   └── UserController.js   # User management logic
    ├── models/             # MongoDB schemas
    │   ├── userModel.js    # User schema and model
    │   └── transactionModel.js # Transaction history schema
    ├── middlewares/        # Express middleware
    │   └── auth.js         # Authentication middleware
    ├── configs/            # Configuration files
    │   └── mongodb.js      # MongoDB connection
    ├── server.js           # Express server entry point
    ├── package.json        # Dependencies & scripts
    └── vercel.json         # Deployment configuration
```

## Technology Stack

### Frontend

- **React 18+** - UI library
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **React Context API** - State management

### Backend

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **JWT** - Authentication (implied from auth middleware)

## Key Features

- 🎨 **AI Image Generation** - Generate images using AI
- 👤 **User Authentication** - Secure user login and verification
- 💳 **Credit System** - Purchase and manage credits for image generation
- 📊 **Transaction Tracking** - Monitor usage history
- 🎯 **Image Management** - View and manage generated images

## Installation & Setup

### Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

### Backend Setup

```bash
cd server
npm install
```

Create a `.env` file in the `server/` directory with:

```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
# Add other required environment variables
```

Start the server:

```bash
npm start
```

### Frontend Setup

```bash
cd client
npm install
```

Create a `.env` file in the `client/` directory with:

```
VITE_API_URL=http://localhost:5000
# Add other required environment variables
```

Start the development server:

```bash
npm run dev
```

## Available Scripts

### Client

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Server

- `npm start` - Start the server
- `npm run dev` - Start with nodemon (if configured)

## API Routes

### User Routes (`/api/users/`)

- Authentication endpoints
- User profile management
- Verification endpoints

### Image Routes (`/api/images/`)

- Image generation
- Image history
- Credit management

## Authentication

The application uses JWT (JSON Web Tokens) for authentication. The `auth.js` middleware handles:

- Token validation
- User verification
- Protected route access

## Database Models

### User Model

- User credentials and profile information
- Credit balance
- Account verification status

### Transaction Model

- Usage history
- Credit transactions
- Image generation logs

## Deployment

Both the client and server are configured for Vercel deployment:

- Client: `vercel.json` in `/client`
- Server: `vercel.json` in `/server`

Follow Vercel's documentation for deployment setup.

## Contributing

Contributions are welcome! Please ensure:

- Code follows the ESLint configuration
- Components follow React best practices
- Database operations are properly handled

## License

Specify your project license here.

## Support

For issues or questions, please open an issue in the repository.
