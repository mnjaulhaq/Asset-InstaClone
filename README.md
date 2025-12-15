# InstaClone - Social Media Photo Sharing (MVP)

InstaClone adalah aplikasi web berbagi foto yang terinspirasi dari Instagram, dibangun sebagai proyek pembelajaran end-to-end untuk memahami proses pengembangan aplikasi web modern, mulai dari backend, frontend, hingga deployment.

Proyek ini dirancang sebagai Minimum Viable Product (MVP) dan akan dikembangkan secara bertahap :
## Features (MVP)
- User Authentication (Register & Login)
- User Profile
- Upload Photo
- Feed (Timeline)
- Like Post
- Comment Post

Catatan: Fitur seperti chat, story, dan reels belum termasuk dalam versi MVP.
## 🛠️ Tech Stack
#### Backend
- Node.js
- Express.js
- PostgreSQL
- Prisma ORM
- JWT Authentication
- Cloudinary (Image Upload)

#### Frontend
- React.js
- Tailwind CSS
- Axios

#### Tools & Services
- Git & GitHub
- Postman
- Vercel (Frontend Deployment)
- Railway / Render (Backend & Database)

#### 📂 Project Structure
```
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

```
## 🗄️ Database Design (Simplified)
#### User
- id
- username
- email
- password
- avatar
- created_at

#### Post
- id
- user_id
- image_url
- caption
- created_at

#### Like
- id
- user_id
- post_id

#### Comment
- id
- user_id
- post_id
- content
- created_at

## 🔗 API Endpoints (Core)
#### Auth
```sh
POST /api/auth/registe
POST /api/auth/login
```
#### User
```sh
GET /api/users/:id
```
#### Post
```sh
POST /api/posts
GET /api/posts
GET /api/posts/:id
```
#### Like
```sh
POST /api/posts/:id/like
```
#### Comment
```sh
POST /api/posts/:id/comments
GET /api/posts/:id/comments
```
## ⚙️ Environment Variables

Buat file .env di folder backend:
```sh
PORT=5000
DATABASE_URL=postgresql://user:password@localhost:5432/instaclone
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=Jaulhak
CLOUDINARY_API_KEY=22441
CLOUDINARY_API_SECRET=120094
```
## ▶️ How to Run Locally

#### Backend
```sh
cd backend
npm install
npx prisma migrate dev
npm run dev
```

#### Frontend
```sh
cd frontend
npm install
npm run dev
```
Akses aplikasi di:
- Frontend: http://localhost:5173
- Backend: http://localhost:5000

#### 🧪 Testing
- API testing menggunakan Postman
- Manual testing untuk UI & flow user

#### 📌 Roadmap
```sh
- Authentication
- Upload Photo
- Feed
- Like & Comment
- Follow User
- Notification
- Story Feature
```

#### 💻 Author

**Jaulhak**
Backend Developer

Proyek ini dibuat sebagai bagian dari proses pembelajaran dan persiapan untuk pengembangan proyek tim di masa depan.

#### 📄 License
This project is licensed under the MIT License.

>Notes:
Proyek ini akan digunakan sebagai:
Portofolio pribadi
Referensi untuk proyek tim
>Media pembelajaran backend & system design
