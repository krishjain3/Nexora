# Nexora

A cloud-deployed task and project management platform built with Java Spring Boot and React, featuring secure authentication, role-based access control, project collaboration, and task management.

## Features

- Project and task management
- Role-based access control with OWNER, ADMIN, and MEMBER roles
- Project member management
- Multi-user task assignment
- Task filtering by assignee
- Secure Firebase authentication
- RESTful backend APIs
- Responsive React frontend

## Tech Stack

**Backend**
- Java 17
- Spring Boot
- Spring Security
- Spring Data JPA
- PostgreSQL
- Firebase Admin SDK

**Frontend**
- React
- React Router
- Tailwind CSS
- Firebase Authentication
- Vite

**Deployment**
- Docker
- Vercel
- Render
- Neon PostgreSQL

## Architecture

```text
React Frontend
      │
      ▼
Spring Boot REST API
      │
      ├── Spring Security
      ├── Service Layer
      ├── Repository Layer
      │
      ▼
   PostgreSQL

Firebase Authentication
      │
      ▼
Spring Security
Project Structure
nexora/
├── backend/
│   └── user-service/
│       └── src/
│           ├── controller/
│           ├── service/
│           ├── repository/
│           ├── entity/
│           ├── dto/
│           └── config/
│
├── frontend/
│   └── src/
│       ├── auth/
│       ├── components/
│       ├── pages/
│       └── services/
│
├── docs/
└── docker-compose.yml
Live Demo

Frontend: https://nexora-prod.vercel.app

Backend API: https://cloudtask-backend.onrender.com/api

Running Locally
Backend
cd backend/user-service
mvn clean install
mvn spring-boot:run
Frontend
cd frontend
npm install
npm run dev

Configure PostgreSQL and Firebase credentials as described in docs/SETUP.md.

Testing
cd backend/user-service
mvn test
License

This project is licensed under the MIT License.

Author

Krish Jain