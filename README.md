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

