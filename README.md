# 🐝 BeeNote: A Rate-Limited MERN Stack Note-Taking Application

<p align="center">
  <img src="https://img.shields.io/badge/Stack-MERN-00FF9D?style=for-the-badge&logo=react&logoColor=black" alt="MERN Stack Badge"/>
  <img src="https://img.shields.io/badge/Frontend-Vite%20%26%20Tailwind-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite & Tailwind Badge"/>
  <img src="https://img.shields.io/badge/Rate%20Limit-Upstash%20Redis-FF6347?style=for-the-badge&logo=redis&logoColor=white" alt="Rate Limit Badge"/>
  <img src="https://img.shields.io/badge/Database-MongoDB%20%26%20Mongoose-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB Badge"/>
</p>

## ✨ Core Features & Tech Highlights

BeeNote is a robust, full-stack application for managing notes. It demonstrates a complete modern MERN architecture.

### 🔑 Robust Backend

* **API Endpoints:** A well-defined RESTful API handles all note operations (CRUD: Create, Read, Update, Delete) via `/api/notes`.
* **Data Persistence:** Uses **MongoDB** for flexible data storage, managed through the **Mongoose** ODM.
* **Security & Stability:** Implements a sliding window **Rate Limiter** powered by **Upstash Redis**, allowing only 100 requests per minute to protect the API.

### 🎨 Modern Frontend

* **Framework:** Built with **React** and bundled by **Vite** for ultra-fast development and Hot Module Replacement (HMR).
* **Styling:** A sleek and responsive design using the **Tailwind CSS** framework, enhanced with the **DaisyUI** component library for a "forest" themed aesthetic.
* **User Feedback:** Integrates `react-hot-toast` for non-blocking notifications on success, failure, and rate-limiting alerts.

## 🛠️ Local Development Setup

### Prerequisites
* Node.js (16+ recommended)
* MongoDB Atlas or a local MongoDB instance.
* Upstash Redis REST URL and Token.

### 1. Environment Configuration

Create a file named `.env` in the `backend/` directory and populate it with your specific connection details:

```bash
# backend/.env example:
MONGO_URI=your_mongodb_connection_string
UPSTASH_REDIS_REST_URL="your_upstash_redis_url"
UPSTASH_REDIS_REST_TOKEN="your_upstash_redis_token"
NODE_ENV=development
PORT=5001
