# Job Portal Application

A full-stack **MERN** (MongoDB, Express.js, React.js, Node.js) Job Portal that allows companies to post openings and candidates to browse, apply, and track applications—all deployed as serverless functions on Vercel.

## 🚀 Features

* **User Authentication & Authorization**  
  * Secure signup/login with JWT and role-based access (candidate vs. recruiter)

* **Company & Job Management**  
  * CRUD operations for companies and job listings  
  * Rich job descriptions, deadlines, and application tracking

* **Search & Filter**  
  * Full-text search by title, skills, or location  
  * Filter by experience level, salary range, and job type

* **Application Workflow**  
  * Candidates can apply with resume upload (PDF)  
  * Recruiters can view, shortlist, or reject applications

* **Real-Time Notifications**  
  * Email alerts for new applications and status updates (using SendGrid)

* **Error Monitoring**  
  * Integrated Sentry to capture and report runtime errors

* **Responsive UI**  
  * Mobile-first design using Tailwind CSS and React Router

## 🧰 Tech Stack

| Layer              | Technology                        |
| ------------------ | --------------------------------- |
| **Frontend**       | React, React Router, Axios        |
| **Backend**        | Node.js, Express.js               |
| **Database**       | MongoDB, Mongoose                 |
| **Authentication** | JSON Web Tokens (JWT)             |
| **Notifications**  | SendGrid                          |
| **Error Tracking** | Sentry                            |
| **Styling**        | Tailwind CSS                      |
| **Deployment**     | Vercel (Serverless Functions)     |

## 📦 Project Structure

job-portal/
├── client/ # React front end
│ ├── public/
│ ├── src/
│ │ ├── components/ # Reusable UI components
│ │ ├── pages/ # Route pages (Home, Jobs, Dashboard, etc.)
│ │ ├── services/ # API client (Axios wrappers)
│ │ ├── hooks/ # Custom React hooks
│ │ ├── styles/ # Tailwind config & globals
│ │ └── App.jsx # Entry point
│ └── package.json
│
├── server/ # Express API server
│ ├── controllers/ # Route handlers
│ ├── models/ # Mongoose schemas
│ ├── routes/ # API endpoints
│ ├── middleware/ # Auth, validation, error handling
│ ├── utils/ # Helpers (email, Sentry)
│ ├── server.js # App entry point (exported for Vercel)
│ └── vercel.json # Build & routing config
│
├── README.md # This documentation
└── package.json # Root scripts & dependencies (if using monorepo)

markdown
Copy code

## 📝 API Endpoints

> All endpoints are prefixed by `/api`

### Auth
* `POST /api/auth/register` – Create a new user (candidate or recruiter)  
* `POST /api/auth/login`    – Login and receive JWT

### Companies
* `GET /api/companies`        – List all companies  
* `POST /api/companies`       – Create a new company profile (recruiter only)  
* `GET /api/companies/:id`    – Get company details  
* `PUT /api/companies/:id`    – Update company info (owner only)  
* `DELETE /api/companies/:id` – Delete company (owner only)

### Jobs
* `GET /api/jobs`             – List all jobs (with filters & pagination)  
* `POST /api/jobs`            – Post a new job (recruiter only)  
* `GET /api/jobs/:id`         – Get job details  
* `PUT /api/jobs/:id`         – Update job (owner only)  
* `DELETE /api/jobs/:id`      – Delete job (owner only)

### Applications
* `POST /api/jobs/:id/apply`         – Candidate applies to a job (upload resume)  
* `GET /api/applications`            – List user’s applications (candidate)  
* `GET /api/jobs/:id/applications`   – Recruiter views applicants  
* `PATCH /api/applications/:id`      – Update application status (shortlist, reject)

## 🎨 Customization

* **Tailwind**: Tweak `client/src/styles/tailwind.config.js` for colors, fonts, themes.  
* **Email Templates**: Edit `server/utils/email.js` to change notification content.  
* **Sentry**: Adjust sampling and release settings in `server/utils/sentry.js`.  
* **Pagination**: Modify default page size and sorting logic in `server/controllers/job.controller.js`.















