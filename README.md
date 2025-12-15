# Asset-InstaClone
InstaClone adalah aplikasi web berbagi foto yang terinspirasi dari Instagram, dibangun sebagai proyek pembelajaran end-to-end untuk memahami proses pengembangan aplikasi web modern, mulai dari backend, frontend, hingga deployment.

Proyek ini dirancang sebagai Minimum Viable Product (MVP) dan akan dikembangkan secara bertahap.
🚀 Features (MVP)
🔐 User Authentication (Register & Login)
👤 User Profile
🖼️ Upload Photo
📰 Feed (Timeline)
❤️ Like Post
💬 Comment Post

Catatan: Fitur seperti chat, story, dan reels belum termasuk dalam versi MVP.

🛠️ Tech Stack
Backend
-Node.js
-Express.js
-PostgreSQL
-Prisma ORM
-JWT Authentication
-Cloudinary (Image Upload)

Frontend
-React.js
-Tailwind CSS
-Axios

Tools & Services
-Git & GitHub
-Postman
-Vercel (Frontend Deployment)
-Railway / Render (Backend & Database)

📂 Project Structure
instaclone/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── routes/
│   │   ├── middlewares/
│   │   ├── services/
│   │   ├── prisma/
│   │   └── app.js
│   ├── .env
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── App.jsx
│   └── package.json
│
└── README.md

🗄️ Database Design (Simplified)
-User
-id
-username
-email
-password
-avatar
-created_at

Post
-id
-user_id
-image_url
-caption
-created_at

Like
-id
-user_id
-post_id

Comment
-id
-user_id
-post_id
-content
-created_at

🔗 API Endpoints (Core)
Auth
-POST /api/auth/register
-POST /api/auth/login

User
-GET /api/users/:id

Post
-POST /api/posts
-GET /api/posts
-GET /api/posts/:id

Like
-POST /api/posts/:id/like

Comment
-POST /api/posts/:id/comments
-GET /api/posts/:id/comments
