# 📋 Task Management System

> **CSC456 – Advanced Web Programming**
> **Project 3 – Full-Stack Web Application Development with Authentication and Cloud Deployment**

![Node.js](https://img.shields.io/badge/Node.js-Express-green)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-success)
![Mongoose](https://img.shields.io/badge/ODM-Mongoose-red)
![EJS](https://img.shields.io/badge/View-EJS-orange)
![JWT](https://img.shields.io/badge/Auth-JWT-blue)
![bcrypt](https://img.shields.io/badge/Security-bcrypt-yellow)

---

# 📖 Project Overview

The **Task Management System** is a full-stack web application developed using **Node.js**, **Express.js**, **MongoDB**, **Mongoose**, and the **EJS templating engine** following the **Model–View–Controller (MVC)** architecture.

The application provides a secure web dashboard where authenticated users can manage projects, tasks, and users while enforcing role-based authorization. Passwords are securely encrypted using **bcrypt**, and authentication is handled through **JSON Web Tokens (JWT)**.

The application is designed to demonstrate the complete backend development workflow, including authentication, authorization, database modeling, server-side rendering, deployment, and CI/CD integration.

---

# 🚀 Features

* Full-stack MVC architecture
* User Authentication
* User Registration
* Secure Login & Logout
* Password Hashing using bcrypt
* JWT Authentication
* Role-Based Authorization
* CRUD Operations
* MongoDB Database Integration
* Mongoose Data Validation
* Responsive EJS Dashboard
* Server-side Rendering
* Cloud Deployment Ready
* Render Deployment Configuration
* Environment Variable Support
* GitHub CI/CD Ready

---

# 🛠️ Tech Stack

| Technology    | Purpose                 |
| ------------- | ----------------------- |
| Node.js       | Runtime Environment     |
| Express.js    | Backend Framework       |
| MongoDB Atlas | NoSQL Database          |
| Mongoose      | MongoDB ODM             |
| EJS           | Server-side Rendering   |
| JWT           | Authentication          |
| bcrypt        | Password Encryption     |
| dotenv        | Environment Variables   |
| Render        | Cloud Deployment        |
| GitHub        | Version Control & CI/CD |

---

# 🏗️ Project Architecture

The project follows the **MVC (Model–View–Controller)** architecture.

```text
Client
   │
   ▼
Routes
   │
   ▼
Controllers
   │
   ▼
Models (Mongoose)
   │
   ▼
MongoDB
```

---

# 📂 Project Structure

```text
Task-Management-System/
│
├── config/
│
├── controllers/
│   ├── authController.js
│   ├── projectController.js
│   ├── taskController.js
│   └── userController.js
│
├── middleware/
│   └── auth.js
│
├── models/
│   ├── User.js
│   ├── Project.js
│   └── Task.js
│
├── public/
│   ├── css/
│   └── js/
│
├── routes/
│   ├── auth.js
│   ├── users.js
│   ├── projects.js
│   └── tasks.js
│
├── tests/
│   └── requirements.test.js
│
├── views/
│   ├── auth/
│   ├── users/
│   ├── projects/
│   ├── tasks/
│   ├── layouts/
│   └── partials/
│
├── app.js
├── render.yaml
├── package.json
├── .env.example
└── README.md
```

---

# 🗄️ Database Design

## User

Stores application users.

Attributes include:

* Name
* Email
* Password
* Role

---

## Project

Stores project information.

Typical fields include:

* Project Name
* Description
* Assigned Users

---

## Task

Stores individual tasks.

Typical fields include:

* Title
* Description
* Status
* Due Date
* Assigned User
* Related Project

---

# 🔗 Relationships

## One-to-Many

```text
Project
   │
   ├── Task
   ├── Task
   ├── Task
```

One project contains multiple tasks.

---

## Many-to-Many

```text
Users
   ▲
   │
Projects
```

Users may participate in multiple projects.

Projects may include multiple users.

---

# 🔐 Authentication & Authorization

The application implements a complete authentication system.

### Authentication

* User Registration
* User Login
* User Logout
* JWT Authentication
* Protected Routes

### Security

* Password Hashing using bcrypt
* Environment Variables
* JWT Verification Middleware

### Authorization

Role-based access control is implemented.

Supported roles include:

* Admin
* User

Protected routes are only accessible to authenticated users with the appropriate permissions.

---

# 📋 CRUD Operations

The application supports complete CRUD functionality for:

### Users

* Create User
* View Users
* Edit User
* Delete User

---

### Projects

* Create Project
* View Projects
* Edit Project
* Delete Project

---

### Tasks

* Create Task
* View Tasks
* Edit Task
* Delete Task

---

# 🎨 User Interface

The frontend is built using **EJS** server-side templates.

Features include:

* Login Page
* Registration Page
* Dashboard
* Project Management
* Task Management
* User Management
* Shared Layouts
* Reusable Partials

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/tatianabazouni/task-management-system.git
```

Navigate into the project

```bash
cd task-management-system
```

Install dependencies

```bash
npm install
```

Create a `.env` file

```env
MONGODB_URI=your_connection_string
JWT_SECRET=your_secret_key
PORT=3000
```

Run the application

```bash
npm start
```

For development

```bash
npm run dev
```

---

# ☁️ Deployment

The project is configured for cloud deployment.

### MongoDB

* MongoDB Atlas

### Backend

* Render

Environment variables are securely managed using `.env`.

Deployment configuration is included through:

```
render.yaml
```

---

# 🔄 CI/CD Pipeline

The deployment workflow follows these steps:

```
VS Code
     │
Git Commit
     │
Git Push
     │
GitHub Repository
     │
Automatic Deployment
     │
Render
```

Every push to the GitHub repository automatically triggers a new deployment on Render.

---

# 🧪 Testing

A testing folder is included:

```
tests/
```

It contains automated checks to verify the required project functionality.

---

# 📚 Learning Outcomes

This project demonstrates:

* Full-stack web development
* MVC Architecture
* Express.js Routing
* MongoDB Data Modeling
* Mongoose Validation
* Authentication & Authorization
* JWT Security
* Password Encryption
* Server-side Rendering with EJS
* CRUD Operations
* Protected Routes
* Cloud Deployment
* CI/CD Integration
* Clean Project Architecture

