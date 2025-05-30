# Job Portal Application

Welcome to the **Job Portal Application**, a full-stack MERN (MongoDB, Express.js, React.js, Node.js) project that connects job seekers and recruiters. It provides user authentication, role-based dashboards, resume uploads, job search & filtering, and email notifications.

---

## 🚀 Features

* **Role-Based Authentication**: Separate signup/login for **Job Seekers** and **Recruiters** using JWT.
* **Job Listings**: Recruiters can create, update, and delete job postings.
* **Job Search & Filtering**: Job seekers can search by title, location, and skills.
* **Resume Upload**: Job seekers can upload resumes (PDF/DOCX) via Multer & Cloudinary.
* **Application Tracking**: Track application status (Applied, Shortlisted, Rejected).
* **Email Notifications**: Automatic emails for application confirmation and status updates using Nodemailer.
* **Responsive UI**: Styled with Tailwind CSS and React Router for smooth navigation.

---

## 🧰 Tech Stack

| Layer              | Technology                        |
| ------------------ | --------------------------------- |
| **Frontend**       | React, React Router, Tailwind CSS |
| **Backend**        | Node.js, Express.js               |
| **Database**       | MongoDB, Mongoose                 |
| **Authentication** | JSON Web Tokens (JWT)             |
| **File Uploads**   | Multer, Cloudinary                |
| **Email Service**  | Nodemailer                        |

---

## 📦 Project Structure

```
job-portal/
├── backend/               # Express API server
│   ├── controllers/       # Route handlers
│   ├── models/            # Mongoose schemas
│   ├── routes/            # API endpoints
│   ├── middleware/        # Auth, error handling
│   ├── utils/             # Helpers (e.g., email, Cloudinary)
│   ├── server.js          # App entry point
│   └── .env.example       # Environment variables template

├── frontend/              # React client
│   ├── public/
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Route pages (Home, Dashboard, Login, etc.)
│   │   ├── hooks/         # Custom React hooks
│   │   ├── services/      # API calls
│   │   ├── styles/        # Tailwind config
│   │   └── App.jsx        # App entry point
│   └── tailwind.config.js

├── README.md              # Project documentation
└── package.json           # Root scripts & dependencies
```

---

## 🔧 Prerequisites

* [Node.js (v14+)](https://nodejs.org/)
* [npm (v6+) or Yarn](https://yarnpkg.com/)
* [MongoDB](https://www.mongodb.com/) (local or Atlas account)
* [Cloudinary account](https://cloudinary.com/) for media storage
* SMTP credentials (e.g., Gmail, SendGrid) for Nodemailer

---

## ⚙️ Installation & Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/job-portal.git
   cd job-portal
   ```

2. **Backend Setup**

   ```bash
   cd backend
   npm install
   ```

   * Copy `.env.example` to `.env` and configure your environment variables:

     ```env
     PORT=5000
     MONGO_URI=your_mongo_connection_string
     JWT_SECRET=your_jwt_secret
     CLOUDINARY_CLOUD_NAME=your_cloud_name
     CLOUDINARY_API_KEY=your_api_key
     CLOUDINARY_API_SECRET=your_api_secret
     SMTP_HOST=smtp.example.com
     SMTP_PORT=587
     SMTP_USER=your_email@example.com
     SMTP_PASS=your_email_password
     ```

3. **Frontend Setup**

   ```bash
   cd ../frontend
   npm install
   ```

   * Create a `.env.local` in `frontend/`:

     ```env
     VITE_API_BASE_URL=http://localhost:5000/api
     ```

4. **Running the Application**

   * **Backend** (in `backend/`):

     ```bash
     npm run dev
     # Server starts on http://localhost:5000
     ```

   * **Frontend** (in `frontend/`):

     ```bash
     npm run dev
     # Client starts on http://localhost:3000
     ```

5. **Access the App**

   Open your browser and navigate to `http://localhost:3000`.

---

## 📝 API Endpoints

* **Auth**

  * `POST /api/auth/register` – Register user (role: seeker or recruiter).
  * `POST /api/auth/login` – Authenticate and receive JWT.

* **Users**

  * `GET /api/users/me` – Get current user profile.

* **Jobs**

  * `POST /api/jobs` – Create new job (recruiter only).
  * `GET /api/jobs` – List all jobs (with filters).
  * `GET /api/jobs/:id` – Get job details.
  * `PUT /api/jobs/:id` – Update job (recruiter only).
  * `DELETE /api/jobs/:id` – Delete job (recruiter only).

* **Applications**

  * `POST /api/jobs/:id/apply` – Apply to a job (resume upload).
  * `GET /api/users/applications` – Get applications for current user.
  * `PATCH /api/applications/:id/status` – Update application status (recruiter only).

---

## 🎨 Customization

* **Styling**: Modify `tailwind.config.js` to update themes, colors, and plugins.
* **Cloudinary**: Adjust upload presets in `utils/cloudinary.js`.
* **Email Templates**: Customize email bodies in `utils/mail.js`.

---

## 📈 Deployment

**Frontend**

1. Build the client:

   ```bash
   cd frontend
   npm run build
   ```
2. Deploy `frontend/dist/` to Netlify, Vercel, or any static host.

**Backend**

1. Ensure your `.env` is configured for production.
2. Deploy `backend/` to Heroku, DigitalOcean, or similar.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/my-feature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/my-feature`.
5. Open a Pull Request.

---

## 📄 License

This project is developed solely by me and is presented here as my personal work. All rights are reserved.

---
