# 🔐 PassOP — Password Manager

A full-stack password manager built with **React, Tailwind CSS, Express.js, and MongoDB**.

PassOP provides a simple interface for storing, editing, deleting, and copying website credentials, with data persisted in MongoDB through a custom Express.js backend.

> ⚠️ **Disclaimer:** This is a learning/portfolio project and is not intended for storing real passwords. The current version does not implement encryption, authentication, or other production-grade security measures.

---

## 🚀 Features

* 🔐 Add website credentials
* ✏️ Edit saved passwords
* 🗑️ Delete passwords
* 👁️ Show/hide password input
* 📋 Copy website, username, and password to clipboard
* 💾 Persistent storage with MongoDB
* 🔄 Load saved passwords when the application starts
* 🔔 Toast notifications
* 📱 Responsive UI
* 🎨 Modern interface using Tailwind CSS
* 🆔 Unique IDs using UUID

---

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* Tailwind CSS
* JavaScript
* React Toastify
* UUID

### Backend

* Node.js
* Express.js
* MongoDB
* MongoDB Node.js Driver
* CORS
* dotenv
* Body Parser

---

## 🏗️ How It Works

```text
              React Frontend
                    │
                    │ fetch()
                    ▼
             Express.js API
                    │
                    │ MongoDB Driver
                    ▼
              MongoDB Database
                    │
                    │
                    ▼
             passwords collection
```

The frontend communicates with the Express backend using HTTP requests.

The backend handles CRUD operations and stores the password documents in MongoDB.

---

## 📂 Project Structure

```text
Password-Manager-App/
│
├── backend/
│   ├── .env
│   ├── package-lock.json
│   ├── package.json
│   └── server.js
│
├── public/
│   ├── icons/
│   │   ├── add.gif
│   │   ├── copy.gif
│   │   ├── delete.gif
│   │   ├── edit.gif
│   │   ├── github.png
│   │   ├── hide.png
│   │   └── show.gif
│   │
│   ├── favicon.png
│   ├── favicon.svg
│   └── icons.svg
│
├── src/
│   ├── assets/
│   │   ├── hero.png
│   │   ├── react.svg
│   │   └── vite.svg
│   │
│   ├── components/
│   │   ├── Footer.jsx
│   │   ├── Manager.jsx
│   │   └── Navbar.jsx
│   │
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
│
├── .gitattributes
├── .gitignore
├── eslint.config.js
├── index.html
├── package-lock.json
├── package.json
├── vite.config.js
└── README.md

```
> 🔒 Important: backend/.env should remain local and should not be committed to GitHub.

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have installed:

* Node.js
* npm
* MongoDB

---

### 1. Clone the repository

```bash
git clone https://github.com/AayushGurung22/Password-Manager-App.git

cd Password-Manager-App
```

---

### 2. Install frontend dependencies

```bash
npm install
```

---

### 3. Install backend dependencies

```bash
cd backend
npm install
```

---

### 4. Configure environment variables

Inside the `backend` folder, create a `.env` file:

```env
MONGO_URI=mongodb://localhost:27017
PORT=3000
```

> Never commit `.env` files or sensitive credentials to GitHub.

---

### 5. Start MongoDB

Make sure your local MongoDB server is running.

The application uses:

```text
Database: passop
Collection: passwords
```

---

### 6. Start the backend

From the `backend` directory:

```bash
node server.js
```

The backend will run on:

```text
http://localhost:3000
```

---

### 7. Start the frontend

Open another terminal and navigate to the project root:

```bash
cd ..
npm run dev
```

Open the local URL provided by Vite.

---

## 🔌 API Endpoints

| Method | Endpoint | Description            |
| ------ | -------- | ---------------------- |
| GET    | `/`      | Retrieve all passwords |
| POST   | `/`      | Save a password        |
| DELETE | `/`      | Delete a password      |

---

## 🧠 What I Learned

Building PassOP helped me understand how different parts of a full-stack application work together.

### React

* Managing forms with `useState`
* Using `useEffect` for fetching data
* Using `useRef` for DOM interactions
* Rendering dynamic data
* Handling CRUD operations
* Managing UI state

### Express.js

* Creating an Express server
* Creating API endpoints
* Handling HTTP requests
* Working with request bodies
* Using middleware
* Enabling CORS

### MongoDB

* Connecting Node.js to MongoDB
* Working with databases and collections
* Inserting documents
* Retrieving documents
* Deleting documents
* Persisting application data

### Full-Stack Integration

One of the biggest takeaways was understanding the complete flow:

```text
User Input
    ↓
React State
    ↓
Fetch API
    ↓
Express Endpoint
    ↓
MongoDB
    ↓
Persistent Data
```

---

## 🔮 Future Improvements

Some features I plan to explore in future versions:

* 🔒 Password encryption
* 👤 User authentication
* 🔑 Master password
* 🛡️ Authorization
* 🎲 Strong password generator
* 🔎 Search and filter
* ☁️ MongoDB Atlas
* 🌐 Deployment
* ⏱️ Session timeout
* 🔐 Better security practices
* 📱 Further mobile optimization

---

## ⚠️ Security Disclaimer

PassOP is currently a **learning/portfolio project**.

The application does not currently provide:

* End-to-end encryption
* Password hashing/encryption
* User authentication
* Authorization
* Production-grade security

**Do not use this application to store real passwords or sensitive credentials.**

---

## 👨‍💻 Author

### Aayush Gurung

Built to practice **React, Express.js, MongoDB, REST APIs, and full-stack web development**.

⭐ If you found the project interesting, consider giving the repository a star.

[GitHub Repository](https://github.com/AayushGurung22/Password-Manager-App)
