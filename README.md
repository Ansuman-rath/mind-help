# 🧠 MindHelp – AI-Powered Mental Health Platform

MindHelp is a **cloud-based mental health support platform** built using the MERN stack. It helps users track their mental well-being, monitor sleep and mood patterns, and interact with an **AI-powered therapist chatbot**.


---

## 🚀 Features

* 🔐 **User Authentication**

  * Secure login & signup using JWT
  * Google Authentication (Firebase)

* 😴 **Sleep Tracker**

  * Log daily sleep data
  * View sleep history

* 😊 **Mood Tracker**

  * Record mood entries
  * Analyze emotional patterns over time

* 🧠 **AI Therapist Chatbot**

  * Integrated using n8n workflows
  * Provides conversational mental health support

* 📝 **Community Posts**

  * Create, update, delete posts
  * Like/unlike posts

---

## 🏗️ Tech Stack

### Frontend

* React.js
* Vite
* Tailwind CSS

### Backend

* Node.js
* Express.js

### Database

* MongoDB Atlas

### Authentication

* JWT (JSON Web Tokens)
* Firebase Google Auth

### DevOps & Deployment

* Docker & Docker Compose
* AWS EC2 (Cloud Deployment)
* Nginx (Reverse Proxy)

### AI Integration

* n8n (AI chatbot workflow automation)

---

## 📂 Project Structure

```
mind-help/
│
├── frontend/        # React frontend
├── backend/         # Express backend
├── docker-compose.yml
└── README.md
```

---

## ⚙️ Installation (Local Setup)

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Ansuman-rath/mind-help.git
cd mind-help
```

---

### 2️⃣ Setup Backend

```bash
cd backend
npm install
```

Create a `.env` file:

```
PORT=8080
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
```

Run backend:

```bash
npm run dev
```

---

### 3️⃣ Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

Frontend runs on:

```
http://localhost:5173
```

---

## 🌐 API Endpoints

### User

* `POST /api/v1/user/register`
* `POST /api/v1/user/login`

### Sleep

* `POST /api/v1/sleep`
* `GET /api/v1/sleep/user`

### Mood

* `POST /api/v1/mood`
* `GET /api/v1/mood`

### Posts

* `POST /api/v1/post`
* `GET /api/v1/post`

---

## 🧠 Problem Statement

Mental health support is often inaccessible, stigmatized, or fragmented.
MindHelp provides a **centralized, accessible, and intelligent platform** where users can:

* Track mental health metrics
* Receive AI-based support
* Engage with a supportive community

---

## 🏗️ Architecture (MERN)

* **React** → User Interface
* **Express + Node.js** → Backend API
* **MongoDB** → Data storage
* **n8n AI Chatbot** → Intelligent interaction layer

---

## 🔐 Security Features

* JWT-based authentication
* Protected API routes
* Secure environment variables

---

## ☁️ Deployment

The application is deployed using:

* Docker containers
* AWS EC2 instance
* MongoDB Atlas (cloud database)

---

## 🎯 Future Improvements

* 📊 Data visualization (graphs for mood/sleep)
* 📱 Mobile app version
* 🤖 Advanced AI therapist (context memory)
* 🔔 Notifications & reminders

---

## 👨‍💻 Author

**Ansuman Rath**

* GitHub: https://github.com/Ansuman-rath

---

## ⭐ Show Your Support

If you like this project, please ⭐ the repository!

---
