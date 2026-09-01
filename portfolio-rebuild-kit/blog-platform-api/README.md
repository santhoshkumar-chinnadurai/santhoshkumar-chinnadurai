# Blog Platform & Comments REST API

A full-stack blog publishing and discussion platform featuring user authentication, post authoring, and nested comments built with **Node.js**, **Express.js**, and **JWT**.

---

## 📌 Overview

The Blog Platform enables registered authors to create, edit, and publish rich articles while allowing the community to participate through threaded discussion comments. All write operations are protected using stateless JSON Web Tokens (JWT) and Bcrypt password hashing.

---

## ✨ Features

- **User Authentication**: Secure signup and login with hashed passwords via Bcrypt and JWT token issuance.
- **Article Authoring & Publishing**: Full CRUD lifecycle for blog posts.
- **Threaded Comment System**: Nested comments associated with specific blog posts.
- **RESTful API Routes**: Clean, decoupled API endpoints for posts, comments, and authentication.
- **Responsive UI**: Fast, modern frontend interface with vanilla JavaScript and CSS3.

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Security**: JSON Web Token (`jsonwebtoken`), Bcrypt (`bcryptjs`)
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)

---

## 💻 Installation & Setup

### 1. Clone & Install
```bash
git clone https://github.com/santhoshkumar-chinnadurai/blog-platform-api.git
cd blog-platform-api
npm install
```

### 2. Run the Server
```bash
npm start
```
The server starts on port `3000`.

---

## 🔐 Environment Variables (.env.example)

Create `.env` in the root directory:
```env
PORT=3000
JWT_SECRET=your_jwt_secret_key_here
```

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Santhoshkumar Chinnadurai**  
- **GitHub**: [@santhoshkumar-chinnadurai](https://github.com/santhoshkumar-chinnadurai)  
- **LinkedIn**: [santhoshkumar-chinnadurai](https://www.linkedin.com/in/santhoshkumar-chinnadurai-4b8034344)
