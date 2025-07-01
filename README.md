# FinanceSmart

FinanceSmart is a full-stack financial expense tracking application designed to help users manage their income and expenses efficiently. The project leverages the MERN stack (MongoDB, Express.js, React.js, Node.js) and modern development tools to deliver a secure, scalable, and user-friendly experience.

---

## Live Demo

- **Frontend**: [https://financesmart-bc8j.vercel.app](https://financesmart-bc8j.vercel.app)
- **Backend**: [https://financesmart.onrender.com](https://financesmart.onrender.com)

---

## Features

- **User Authentication**: Secure registration and login using JWT.
- **Profile Management**: Upload and manage user profile images.
- **Income & Expense Tracking**: Add, view, and delete income and expense records.
- **Dashboard Analytics**: Visualize financial data with charts and summaries.
- **Excel Export**: Download income and expense data as Excel files.
- **Responsive Design**: Optimized for all devices using Tailwind CSS.
- **Notifications**: Real-time feedback for user actions.

---

## Tech Stack

### Frontend

- **React.js**: UI library for building interactive interfaces.
- **Tailwind CSS**: Utility-first CSS framework for rapid styling.
- **Vite**: Fast build tool and development server.
- **Axios**: HTTP client for API requests.
- **React Router**: Client-side routing.
- **Context API**: Global state management.
- **Recharts**: Data visualization.
- **React Hot Toast**: User notifications.

### Backend

- **Node.js** & **Express.js**: Backend server and REST API.
- **MongoDB** & **Mongoose**: Database and ODM.
- **JWT**: Authentication and authorization.
- **Multer**: File uploads for profile images.
- **xlsx**: Excel file generation.
- **dotenv**: Environment variable management.
- **CORS**: Cross-origin resource sharing.

### Deployment

- **Frontend**: Vercel
- **Backend**: Render

---

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- MongoDB database (local or Atlas)

### Backend Setup

1. **Navigate to the backend directory:**
   ```sh
   cd backend
   ```

2. **Install dependencies:**
   ```sh
   npm install
   ```

3. **Configure environment variables:**
   Create a `.env` file in the backend root:
   ```
   MONGO_URL=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=8000
   CLIENT_URL=https://your-frontend-url.com
   ```

4. **Run the backend server:**
   ```sh
   npm start
   ```

### Frontend Setup

1. **Navigate to the frontend directory:**
   ```sh
   cd frontend/expense-tracker
   ```

2. **Install dependencies:**
   ```sh
   npm install
   ```

3. **Configure environment variables (optional):**
   Create a `.env` file in the frontend root:
   ```
   VITE_API_BASE_URL=https://your-backend-url.com
   ```

4. **Run the frontend development server:**
   ```sh
   npm run dev
   ```

---

## Folder Structure

```
Financesmart/
│
├── backend/                # Express.js backend API
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── uploads/
│   ├── .env
│   └── server.js
│
└── frontend/
    └── expense-tracker/    # React.js frontend
        ├── public/
        ├── src/
        ├── .env
        ├── package.json
        └── vite.config.js
```

---

## API Documentation

See the [backend README](./backend/README.md) for detailed API endpoints and usage.

---

## License

This project is licensed under the MIT License.
