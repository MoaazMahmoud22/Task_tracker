
# ✅ Task Tracker

[![Node.js](https://img.shields.io/badge/Backend-Node.js-green)]()
[![React](https://img.shields.io/badge/Frontend-React-blue)]()
[![Dockerized](https://img.shields.io/badge/Deployment-Docker-informational)]()

> 🎯 A full-stack web application for managing and tracking daily tasks.

---

## 📸 Demo

![Dashboard] ![image](https://github.com/user-attachments/assets/4f5b8af9-e0af-409b-82c7-64707adf5de6)

![Add Task] ![image](https://github.com/user-attachments/assets/83fdc5d5-e286-475b-93c5-1ffbcb829116)

![Task View] ![image](https://github.com/user-attachments/assets/1e36b60c-a605-4b3a-ad8b-dd88e5ad569d)

![Notification] ![image](https://github.com/user-attachments/assets/232a3a8c-237a-4cee-948d-5ba66ffca6ef)

![Profile] ![image](https://github.com/user-attachments/assets/ccddcde0-d15e-4dc0-8ab3-c663a7a9e252)




 <!-- Add a screenshot if available -->

---

## 🚀 Features

- 📝 Add new tasks
- ✏️ Edit and delete tasks
- ✅ Toggle task status (pending/completed)
- 📦 Full REST API (CRUD)
- 🎨 Responsive and modern UI with Tailwind CSS
- 🐳 Dockerized for easy deployment

---

## 🧱 Tech Stack

| Layer     | Technology           |
|-----------|----------------------|
| Frontend  | React, Tailwind CSS  |
| Backend   | Node.js, Express     |
| Database  | MongoDB              |
| DevOps    | Docker, Docker Compose |

---

## 📂 Project Structure

```bash
task-tracker/
├── frontend/               # React application
│   ├── src/
│   ├── public/
│   └── ...
├── backend/                # Express backend
│   ├── src/
│   ├── index.js
│   └── ...
├── docker-compose.yml      # Docker orchestration
└── README.md               # This file
```

---

## ⚙️ Installation & Run Locally

### 🚧 Prerequisites

- Node.js & npm
- Docker (for containerized setup)
- MongoDB (local or cloud)

---

### 🔧 Manual Setup (Without Docker)

#### 1. Clone the repository
```bash
git clone https://github.com/yourusername/task-tracker.git
cd task-tracker
```

#### 2. Backend Setup
```bash
cd backend
npm install
npm run dev
```

#### 3. Frontend Setup
```bash
cd ../frontend
npm install
npm start
```

---

### 🐳 Docker Setup

```bash
docker-compose up --build
```

This will start both backend and frontend containers.

---

## 📬 API Endpoints (Sample)

| Method | Endpoint         | Description        |
|--------|------------------|--------------------|
| GET    | /api/tasks       | Get all tasks      |
| POST   | /api/tasks       | Create a new task  |
| PUT    | /api/tasks/:id   | Update a task      |
| DELETE | /api/tasks/:id   | Delete a task      |

---

## 🙌 Contribution

Pull requests are welcome. For major changes, please open an issue first.

