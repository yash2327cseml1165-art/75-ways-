# Major LMS

Major LMS is an AI-powered Learning Management System built as a full-stack web application with a scalable backend and an interactive frontend.  
The project demonstrates secure authentication, role-based access control, course management, lecture management, media uploads, payment integration, review handling, and modern frontend-backend integration.

## Live Demo

- Repository: https://github.com/ANUSHK-24/Major_lms
- Live Application: https://major-lms-2.onrender.com/

## Overview

This project is designed as a modern LMS platform where users can access educational content through a secure and modular architecture.  
It includes user authentication, protected routes, educator and student roles, course creation and management, lecture handling, payment verification, profile updates, and review functionality.

## Core Functionalities

### Authentication & Security
- User signup and login
- Password hashing using bcryptjs
- JWT-based authentication
- Protected routes using authentication middleware
- Secure cookie-based token handling
- Logout functionality
- OTP-based password reset flow
- Email-based OTP sending and verification
- Google authentication support

### Role-Based Access
- Role-based user model with `student` and `educator` roles
- Authenticated route protection for role-aware platform usage
- Educator-oriented course creation and management flow
- Student-oriented LMS consumption flow

### Course & Lecture Management
- Create courses
- Edit course details
- Delete courses
- Get course by ID
- Fetch published courses
- Fetch creator-specific courses
- Create lectures inside courses
- Edit lecture content
- Delete lectures
- Fetch course lectures
- Creator-specific course access support

### User Features
- Get current logged-in user
- Update user profile
- Upload profile photo
- Personalized user flow with protected APIs

### Reviews
- Add course reviews
- Get course reviews
- Fetch all reviews

### Payments
- Razorpay order creation
- Payment verification flow
- Course purchase/enrollment related backend processing

### Media & File Handling
- Multer-based file upload handling
- Cloudinary integration for media storage
- Thumbnail and video upload support

### AI Integration
- Dedicated AI route/controller support for LMS-related intelligent features

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT
- bcryptjs
- Validator
- Cookie Parser
- CORS
- Nodemailer
- Multer
- Cloudinary
- Razorpay

### Frontend
- React
- Vite
- Redux Toolkit
- React Router DOM
- Axios
- React Toastify
- Recharts
- Tailwind CSS
- Firebase

## Project Structure

```bash
Major_lms/
├── backend/
│   ├── config/
│   ├── controller/
│   ├── middleware/
│   ├── model/
│   ├── route/
│   └── index.js
└── frontend/
```

## Backend Modules

### Configuration
- Database connection
- JWT token generation
- Cloudinary setup
- Email sending utility

### Controllers
- Authentication controller
- Course controller
- Payment controller
- Review controller
- User controller
- AI controller

### Middleware
- Authentication middleware
- Multer upload middleware

### Models
- User model
- Course model
- Lecture model
- Review model

### Routes
- `/api/auth`
- `/api/user`
- `/api/course`
- `/api/payment`
- `/api/review`
- `/api/ai`

## API Highlights

### Auth Routes
- `POST /api/auth/signup`
- `POST /api/auth/login`
- `GET /api/auth/logout`
- `POST /api/auth/sendotp`
- `POST /api/auth/verifyotp`
- `POST /api/auth/resetpassword`
- `POST /api/auth/googleauth`

### User Routes
- `GET /api/user/getcurrentuser`
- `POST /api/user/profile`

### Course Routes
- `POST /api/course/create`
- `GET /api/course/getpublishedcoures`
- `GET /api/course/getcreatorcourses`
- `POST /api/course/editcourse/:courseId`
- `GET /api/course/getcourse/:courseId`
- `DELETE /api/course/removecourse/:courseId`
- `POST /api/course/createlecture/:courseId`
- `GET /api/course/getcourselecture/:courseId`
- `POST /api/course/editlecture/:lectureId`
- `DELETE /api/course/removelecture/:lectureId`
- `POST /api/course/getcreator`

### Payment Routes
- `POST /api/payment/create-order`
- `POST /api/payment/verify-payment`

### Review Routes
- `POST /api/review/givereview`
- `GET /api/review/allReview`

## Security and Validation

This project follows secure backend practices using JWT authentication, bcrypt-based password hashing, protected route middleware, email validation, OTP verification, and secure cookie handling.  
The modular structure improves maintainability and makes the backend easier to extend with new features.

## Frontend Integration

The frontend is built to interact directly with backend APIs and provide a complete LMS experience.  
It includes routing, state management, API communication, notifications, charts, and a production-ready UI architecture using React and Vite.

## Database Design

The backend uses MongoDB with Mongoose models for:
- Users
- Courses
- Lectures
- Reviews

This schema design supports modular LMS growth and clean separation of business logic.

## Deployment

The application is deployed on Render and is publicly accessible.

Live URL: https://major-lms-2.onrender.com/

## Scalability Notes

The project follows a modular backend architecture with separate configuration, controllers, middleware, models, and routes.  
This structure makes it easier to scale the application by introducing caching, microservices, background jobs, API versioning, containerized deployment, and load balancing in future iterations.

## Author

YASH KUMAR   
GitHub: https://github.com/yash2327cseml1165-art
