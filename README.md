# Real-Time Collaborative To-Do Board 👥📝
A full-stack MERN Application enabling real-time collaboration on tasks (like Trello) with live sync, smart logic, and conflict resolution.

#Live Demo 🚀
Project-Link : []
Demo-Video : []

This is a real-time collaborative Kanban board built using MERN stack. it allows multiple users to :
- Create and manage tasks across three columns : **To-DO** , **In-Progress** and **Done**
- Assign tasks manually or using Smart Assign logic
- See real-time updates with Socket.io
- Handle editing conflicts using merge/overwrite choice
- View the last 20 activities in a live-updating activity log

# Key Features #
- JWT Authentication
- Drag & Drop task on Kanban board
- Smart task assign
- Conflict resolution
- Live activity log
- responsive design

# Tech Stack #

| Component         | Technology                          |
|------------------ |------------------------------------ |
| **Frontend**      | React (React DnD, Socket.IO Client) |
| **Backend**       | Node.js/Express, Socket.IO          |
| **Database**      | MongoDB (Mongoose ODM)              |
| **Authentication**| JWT, Bcrypt                         |
| **Deployment**    | Vercel (Frontend), Render (Backend) |

# Setup Instructions # ⚙️

## 1. Backend
cd backend
npm install
touch .env

 Run the backend as -
     npm start
     
## 2. Frontend
cd frontend
npm install
npm run dev

🎯 Smart Assign Logic
When "Smart Assign" is clicked , the backend finds the user with the fewest non-completed tasks and assigns the task to them.

# Conflict Resolution System #
# Problem Statement #
Handles simultaneous edits to the same task by multiple users.

# Implemented Logic #
# 1. Version Trackin
- Each task has version field(Integer)
- Incremented on every update

# 2. Conflict Detection
If two or more users try to update the same task simultaneously:
- the backend checks for conflicts using updatedAt timestamps.
- if conflict detected , both versions are returned
- the frontend shows popup to Merge or Overwrite

# Usage Guide #
1. Register / Login
2. Create tasks using the (+) button
3. Use drag-drop to move task across columns.
4. Assign users manually or click smart assign
5. Watch real-time updates as teammates work!
6. View activity logs at bottom of the dashboard
