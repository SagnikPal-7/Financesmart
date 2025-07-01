# FinanceSmart Backend

FinanceSmart is a financial expense tracking application. This backend is built with Node.js, Express.js, and MongoDB, providing secure RESTful APIs for user authentication, income/expense management, and dashboard analytics.

---

## Features

- **User Authentication**: Secure registration and login using JWT.
- **Profile Management**: Upload and manage user profile images.
- **Income & Expense Tracking**: Add, view, and delete income and expense records.
- **Dashboard Analytics**: Get summaries and recent transactions.
- **Excel Export**: Download income and expense data as Excel files.
- **Role-based Access**: Protected routes for authenticated users.
- **CORS Enabled**: Configured for secure frontend-backend communication.

---

## Tech Stack

- **Node.js** & **Express.js**: Backend server and REST API.
- **MongoDB** & **Mongoose**: Database and ODM.
- **JWT**: Authentication and authorization.
- **Multer**: File uploads for profile images.
- **xlsx**: Excel file generation.
- **dotenv**: Environment variable management.
- **CORS**: Cross-origin resource sharing.

---

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- MongoDB database (local or Atlas)

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/yourusername/financesmart-backend.git
   cd financesmart-backend
   ```

2. **Install dependencies:**

   ```sh
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory:

   ```
   MONGO_URL=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   PORT=8000
   CLIENT_URL=https://your-frontend-url.com
   ```

4. **Run the server:**
   ```sh
   npm start
   ```
   The server will run on `http://localhost:8000` by default.

---

## API Endpoints

### Auth

- `POST /api/v1/auth/register` — Register a new user
- `POST /api/v1/auth/login` — Login user
- `GET /api/v1/auth/getUser` — Get user info (protected)
- `POST /api/v1/auth/upload-image` — Upload profile image

### Income

- `POST /api/v1/income/add` — Add income (protected)
- `GET /api/v1/income/get` — Get all income (protected)
- `GET /api/v1/income/downloadexcel` — Download income as Excel (protected)
- `DELETE /api/v1/income/:id` — Delete income (protected)

### Expense

- `POST /api/v1/expense/add` — Add expense (protected)
- `GET /api/v1/expense/get` — Get all expenses (protected)
- `GET /api/v1/expense/downloadexcel` — Download expenses as Excel (protected)
- `DELETE /api/v1/expense/:id` — Delete expense (protected)

### Dashboard

- `GET /api/v1/dashboard/` — Get dashboard analytics (protected)

---

## Folder Structure

```
backend/
│
├── config/                # Database connection
├── controllers/           # Route controllers
├── middleware/            # Auth and upload middleware
├── models/                # Mongoose models
├── routes/                # API route definitions
├── uploads/               # Uploaded profile images
├── .env                   # Environment variables
├── server.js              # Entry point
└── package.json
```

---

## Deployment

- **Environment variables** must be set on your deployment platform (e.g., Render, Heroku).
- Ensure the `uploads/` directory is writable if using local storage for images.

---

## Security

- Passwords are hashed using bcrypt before storage.
- All protected routes require a valid JWT token.
- CORS is restricted to the frontend domain.

---

## License

This project is licensed under the MIT License.
