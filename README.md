# 🛡️ Cybersecurity Internship – Week 1  
## User Management System Security Assessment

---

## 👤 Intern Information
- **Name:** Muhammad Talha  
- **Program:** Cybersecurity Internship  
- **Task:** Week 1 – Security Assessment  

---

## 📌 Project Overview

This project is a simple User Management System built using Node.js, Express, and MongoDB. It provides user registration, login, and profile management using JWT authentication.

The goal of this task is to perform a basic security assessment and identify common web application vulnerabilities.

---

## ⚙️ Tech Stack

- Node.js  
- Express.js  
- MongoDB Atlas  
- JWT Authentication  
- bcrypt Password Hashing  
- Postman for API Testing  

---

## 🚀 How to Run

### 1. Install dependencies
```bash
npm install
```

---
## 2. Setup environment variables

Create .env file:

MONGODB_URI=your_mongodb_uri
PORT=3000
JWT_SECRET=your_secret

---

## 3. Start server
npm start

Server runs at:

http://localhost:3000


## 🔗 API Endpoints

# User Routes

POST /api/v1/users/register
POST /api/v1/users/login
GET /api/v1/users/account

# Admin Routes

GET /api/v1/admin/users
DELETE /api/v1/admin/user


---

## 🔍 Security Testing

# 🟠 XSS Test

Input:

<script>alert('XSS')</script>

Result:
Stored in database but not executed.

# 🔵 SQL Injection Test

Input:

admin' OR '1'='1

Result:
Login failed – system is secure against basic SQL injection.


---

## 🟢 Authentication Test
JWT token generated successfully
Protected routes require valid token


## ⚠️ Security Issues Found

Input sanitization missing (XSS risk)
No rate limiting implemented
Basic security headers not enabled


## 🛠️ Recommendations
Add input validation and sanitization
Use Helmet.js for security headers
Implement rate limiting
Improve password policies
Add logging system



---


## 📊 Conclusion

This project demonstrates a basic secure backend system with JWT authentication and MongoDB. Minor security improvements are recommended for production use.

## 📦 Deliverables
Source Code
Security Report
Video Explanation



---

## 👨‍💻 Author

Muhammad Talha
Cybersecurity Intern
