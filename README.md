# Learning Management System (LMS)

## 📌 Project Overview
The **Learning Management System (LMS)** is a full-stack MERN (MongoDB, Express, React, Node.js) web application that allows users to register, purchase courses, track progress, and manage learning content. The backend is built using **Node.js, Express, MongoDB**, and the frontend is developed using **React (Vite)**.

## 🚀 Features
- User Authentication (Login & Signup)
- Course Management (Create, Update, Delete)
- Media Uploads
- Purchase Courses
- Course Progress Tracking
- Secure User Sessions with Cookies
- CORS Configuration for Frontend & Backend Integration

## 🛠 Tech Stack
### **Backend:**
- Node.js
- Express.js
- MongoDB (Mongoose ODM)
- dotenv (Environment Variables)
- cookie-parser
- CORS

### **Frontend:**
- React.js (Vite)
- TailwindCSS
- React Router

## 🏗 Installation Guide
### **1️⃣ Clone the Repository**
```sh
git clone 
cd LMS
```

### **2️⃣ Backend Setup**
```sh
cd backend
npm install
npm start
```

Create a **.env** file in the `backend/` directory with the following:
```
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

### **3️⃣ Frontend Setup**
```sh
cd frontend
npm install
npm run dev
```

## 🖥 Deployment
### **Backend:** Hosted on Render → [Backend URL](https://lms-x6sc.onrender.com)
### **Frontend:** Hosted on Netlify/Vercel → [Frontend URL](https://your-frontend-link.com)

## 🔗 API Endpoints
### **User Routes** (`/api/v1/user`)
- `POST /register` – User registration
- `POST /login` – User login
- `GET /profile` – Get user profile

### **Course Routes** (`/api/v1/course`)
- `GET /` – Get all courses
- `POST /create` – Create a course
- `PUT /update/:id` – Update a course
- `DELETE /delete/:id` – Delete a course

### **Purchase Routes** (`/api/v1/purchase`)
- `POST /buy` – Purchase a course

### **Course Progress Routes** (`/api/v1/progress`)
- `POST /update` – Update user course progress

## ⚠ Troubleshooting
### **1. CORS Issues?**
Check the `server.js` file and ensure CORS is correctly configured:
```js
app.use(cors({
    origin: [
        "http://localhost:5173",
        "https://your-frontend-domain.com"
    ],
    credentials: true
}));
```

### **2. Database Connection Issues?**
Ensure your **MongoDB URI** is correctly set in `.env` and MongoDB is running.

### **3. Deployment Errors?**
- Make sure `.env` variables are correctly set on Render.
- Restart the deployment after making necessary fixes.

## 📜 License
This project is **open-source** and available under the **MIT License**.
