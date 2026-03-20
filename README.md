# Real-Time Collaborative Task Manager

A full-stack task management application that allows users to create, manage, and assign tasks in real time. Built with modern web technologies, it features secure Google authentication, responsive UI, and collaborative task sharing.


## ✨ Features

* 🔐 Google Authentication (secure login)
* ✅ Personal To-Do List (CRUD operations)
* 👥 Task Assignment via Email
* 🔄 Real-time Updates (if implemented)
* 📱 Fully Responsive Design
* ⚡ Loading states, toasts, and error handling


## 🧱 Tech Stack

**Frontend**

* Next.js (React)
* Tailwind CSS
* Shadcn/UI

**Backend**

* Node.js (API Routes)
* TypeScript

**Database**

* PostgreSQL (Prisma ORM)

**Authentication**

* NextAuth (Google OAuth)

**Deployment**

* Vercel (Frontend + Backend)
* Railway / Supabase (Database)


## 🧠 Architectural Decisions

* Used Prisma ORM for type-safe database access.
* Implemented email-based task assignment with fallback:

  * If user exists → linked via userId
  * If not → stored email and linked upon signup
* Separated concerns between UI, API, and database layers.
* Used server-side authentication to protect API routes.


## 🗄️ Database Schema

### User

* id
* name
* email
* image

### Task

* id
* title
* description
* status
* createdBy
* assignedTo
* assignedEmail
* createdAt
