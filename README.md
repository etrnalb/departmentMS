# Department Management System

## Overview

A comprehensive web application for managing academic departments, including courses, materials, and user management with different roles (students, lecturers, and admins).

The Department Management System (DMS) is designed to streamline educational operations by providing a platform for course management, student enrollment, learning materials distribution, and administrative tasks. The application features role-based access controls, real-time updates, and a responsive user interface.

## Live Applications

- Frontend: <https://department-ms.vercel.app/>
- API: <https://departmentms-1.onrender.com/>

## Documentation

- [Frontend Documentation](https://github.com/oyerohabib/departmentMS/blob/main/frontend/README.md)
- [Backend Documentation](https://github.com/oyerohabib/departmentMS/blob/main/backend/README.md)

## Core Features

- Authentication & Authorization
- User registration and login
- JWT-based authentication
- Role-based access control (Student, Lecturer, Admin)
- Password hashing with bcrypt

## Course Management

- Create, view, update, and delete courses
- Course enrollment for students
- Course assignment for lecturers
- Course details with enrolled students

## Learning Materials

- Upload and manage course materials
- Download materials
- Organize materials by course
- User Management
- User profiles with role information
- Update user details
- View enrolled/teaching courses

## Technology Stack

### Frontend

- Next.js
- TypeScript
- Tailwind CSS
- Axios for API requests
- React Toastify for notifications

### Backend

- Express.js
- TypeScript
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- CORS for cross-origin requests

## Screenshots

|                                                        |                                                   |
| :----------------------------------------------------: | :-----------------------------------------------: |
|   ![Landing Page](https://i.imgur.com/wdoVJFC.jpeg)    |  ![Login Page](https://i.imgur.com/AKhT6oN.jpeg)  |
|   ![Register Page](https://i.imgur.com/ZOpo4pU.jpeg)   |  ![Dashboard](https://i.imgur.com/d3IZkBU.jpeg)   |
| ![Course Management](https://i.imgur.com/AuH7OyJ.jpeg) | ![User Profile](https://i.imgur.com/lSh6g33.jpeg) |

## Setup and Installation

### 1) Clone the repository
```bash
git clone https://github.com/etrnalb/departmentMS.git
cd departmentMS
```

### 2) Install MongoDB locally (Ubuntu)
```bash
# Import MongoDB public GPG key
curl -fsSL https://pgp.mongodb.com/server-7.0.asc | sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg --dearmor

# Add MongoDB repo
echo "deb [ signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list

# Update & install
sudo apt-get update
sudo apt-get install -y mongodb-org

# Start and enable service
sudo systemctl start mongod
sudo systemctl enable mongod
```

### 3) Backend
```bash
cd backend
npm install
```

Create `.env`:
```bash
cat > .env << 'EOF'
PORT=4000
MONGODB_URI=mongodb://localhost:27017/departmentms
JWT_SECRET=change_me
CORS_ORIGIN=http://localhost:3000
UPLOAD_DIR=uploads
EOF
```

Run:
```bash
npm run dev
```

### 4) Frontend
```bash
cd ../frontend
```

Create `.env`:
```bash
cat > .env << 'EOF'
NEXT_PUBLIC_API_BASE_URL=http://localhost:4000
EOF
```

Run:
```bash
npm run dev
```

Visit:
- http://localhost:3000



## Future Development Roadmap

### Enhanced Admin Controls

- Comprehensive user management system
- Bulk actions for courses and users
- Analytics dashboard for administrators
- User activity monitoring
- System-wide announcements

### Academic Structure

- Integration of academic levels (100L, 200L, etc.)
- Semester/session-based course organization
- Prerequisite course relationships
- Academic calendar integration
- Course credit system

### Technical Improvements

- Improved landing page with feature highlights
- Swagger documentation for the API
- Social authentication (Google, Facebook)
- WebSocket integration for real-time notifications
- Mobile application development
- API rate limiting and caching

### Student Experience

- Class scheduling and timetable generation
- Calendar integration
- Exam and assignment submission portals
- Grade management system
- Student performance analytics
- Discussion forums for courses

### Lecturer Features

- Attendance tracking
- Grading tools
- Automated notification system for upcoming classes
- Integration with video conferencing for virtual classes
- Course material version control
- Assignment creation and management

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the [MIT LICENSE](LICENSE).
