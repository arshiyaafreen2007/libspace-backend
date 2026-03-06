# LibSpace Backend API

LibSpace is a backend API built using **Node.js, Express.js, and MongoDB**.  
It provides authentication using **JWT** and allows users to perform **CRUD operations on books**.

---

## Features

- User Registration
- User Login with JWT Authentication
- Add Books
- Get All Books
- Get Book by ID
- Update Book
- Delete Book
- Protected Routes using Token Verification

---

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- JSON Web Token (JWT)
- bcrypt.js

---

## Installation

```
git clone https://github.com/arishyaafreen2007/libspace-backend.git
cd libspace-backend
npm install
```

---

## Environment Variables

Create a `.env` file in the root directory and add the following variables:

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
SECRET_KEY=your_secret_key
```

Example `.env` structure is available in:

```
.env.example
```

---

## Run the Server

```
npm start
```

Server runs at:

```
http://localhost:5000
```

---

## API Endpoints

### Authentication

Register User

```
POST /api/authuser/register
```

Login User

```
POST /api/authuser/login
```

---

### Books

Add Book

```
POST /api/book/addbook
```

Get All Books

```
GET /api/book/getBooks
```

Get Book by ID

```
GET /api/book/:bookId
```

Update Book

```
PUT /api/book/:bookId
```

Delete Book

```
DELETE /api/book/deleteBook/:bookId
```

---

## Authorization

Protected routes require a **Bearer Token** in the request header.

Example header:

```
Authorization: Bearer <your_token>
```

---

## Project Structure

```
libspace-backend
│
├── Config
│   └── db.js
│
├── controller
│   ├── authController.js
│   └── bookController.js
│
├── middlewares
│   └── verify_token.js
│
├── models
│   ├── user.model.js
│   ├── book.model.js
│   └── blackListerToken.js
│
├── routes
│   ├── user.route.js
│   └── book.route.js
│
├── .env.example
├── .gitignore
├── index.js
├── package.json
└── README.md
```

---

## Author

Arishya Afreen

GitHub  
https://github.com/arishyaafreen2007