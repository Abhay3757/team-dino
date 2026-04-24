# 🦕 Team Dino — Student Team Members Management App
Team members-
- Abhay Singh
- Govind H Warrier
---

## 📋 Project Description

A full-stack web application to manage student team members. Built with:
- **Frontend:** React.js + React Router + Axios
- **Backend:** Node.js + Express.js
- **Database:** MongoDB (via Mongoose)
- **File Uploads:** Multer

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v18+)
- MongoDB (running locally or MongoDB Atlas URI)
- npm

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/Team-Dino.git
cd Team-Dino
```

### 2. Setup Backend
```bash
cd backend
npm install
```
Create a `.env` file in the `backend/` folder:
```
MONGO_URI=mongodb://localhost:27017/teamdino
PORT=5000
```
Start the backend:
```bash
npm run dev
# or
npm start
```
Backend runs on: `http://localhost:5000`

### 3. Setup Frontend
```bash
cd ../frontend
npm install
npm start
```
Frontend runs on: `http://localhost:3000`

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/members` | Retrieve all team members |
| `GET` | `/api/members/:id` | Fetch a single member by ID |
| `POST` | `/api/members` | Add a new team member (multipart/form-data) |
| `DELETE` | `/api/members/:id` | Delete a member by ID |

### POST /api/members — Form Fields
| Field | Required | Description |
|-------|----------|-------------|
| name | ✅ | Full name |
| roll | ✅ | Roll number |
| year | ✅ | Batch year |
| degree | ✅ | Degree (e.g. B.Tech CSE) |
| email | ✅ | Email address |
| role | ✅ | Role/designation |
| project | ❌ | Project name |
| hobbies | ❌ | Hobbies |
| certificate | ❌ | Certifications |
| internship | ❌ | Internship details |
| aboutAim | ❌ | About & aims |
| image | ❌ | Profile photo (jpg/png/gif/webp, max 5MB) |

---

## 📁 Project Structure
```
Team-Dino/
├── backend/
│   ├── models/
│   │   └── Member.js
│   ├── routes/
│   │   └── members.js
│   ├── uploads/          ← profile images stored here
│   ├── .env
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Home.js
│   │   │   ├── AddMember.js
│   │   │   ├── ViewMembers.js
│   │   │   └── MemberDetails.js
│   │   ├── App.js
│   │   ├── index.js
│   │   └── index.css
│   └── package.json
├── .gitignore
└── README.md
```

---

## 🌐 Pages
- **`/`** — Home page with team intro and navigation
- **`/add`** — Add a new team member (form with image upload)
- **`/view`** — View all team members in a card grid
- **`/member/:id`** — Full details of a selected member

---

## 📦 Test API in Browser
- All members: `http://localhost:5000/api/members`
- Single member: `http://localhost:5000/api/members/<MEMBER_ID>`
