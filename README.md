# Doctor Appointment System

A comprehensive full-stack web application for managing doctor appointments with separate interfaces for patients, doctors, and administrators. Built with modern web technologies including React, Node.js, and MongoDB.

## 🏥 Overview

The Doctor Appointment System is designed to streamline the process of booking, managing, and tracking medical appointments. It provides a seamless experience for patients to find and book appointments with healthcare providers while giving administrators and doctors powerful tools to manage their practice.

## 🚀 Features

### Patient Portal (Frontend)
- **User Registration & Authentication**: Secure login and signup functionality
- **Doctor Discovery**: Browse and search for doctors by specialty
- **Appointment Booking**: Schedule appointments with available doctors
- **Appointment Management**: View, reschedule, or cancel existing appointments
- **Profile Management**: Update personal information and preferences
- **Payment Integration**: Secure payment processing with Stripe and Razorpay
- **Responsive Design**: Mobile-friendly interface built with Tailwind CSS

### Admin Panel
- **Dashboard**: Overview of system statistics and key metrics
- **Doctor Management**: Add, edit, and manage doctor profiles
- **Appointment Oversight**: Monitor and manage all appointments
- **User Management**: Oversee patient registrations and accounts
- **Analytics**: Track system usage and performance metrics

### Backend API
- **RESTful API**: Well-structured API endpoints for all operations
- **Authentication & Authorization**: JWT-based secure authentication
- **Database Management**: MongoDB integration with Mongoose ODM
- **File Upload**: Image handling with Cloudinary integration
- **Payment Processing**: Integration with multiple payment gateways
- **Email Verification**: Account verification system

## 🛠️ Technology Stack

### Frontend & Admin Panel
- **React 18**: Modern React with hooks and functional components
- **Vite**: Fast build tool and development server
- **React Router DOM**: Client-side routing
- **Axios**: HTTP client for API communications
- **React Toastify**: User notifications and alerts
- **Tailwind CSS**: Utility-first CSS framework
- **ESLint**: Code linting and quality assurance

### Backend
- **Node.js**: JavaScript runtime environment
- **Express.js**: Web application framework
- **MongoDB**: NoSQL database
- **Mongoose**: MongoDB object modeling
- **JWT**: JSON Web Tokens for authentication
- **Bcrypt**: Password hashing
- **Multer**: File upload handling
- **Cloudinary**: Cloud-based image management
- **CORS**: Cross-origin resource sharing
- **Nodemon**: Development server with auto-restart

### Payment Integration
- **Stripe**: International payment processing
- **Razorpay**: Indian payment gateway

## 📁 Project Structure

```
Doctor_Appointment_System/
├── frontend/                 # Patient-facing React application
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   │   ├── Banner.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Header.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── RelatedDoctors.jsx
│   │   │   ├── SpecialityMenu.jsx
│   │   │   └── TopDoctors.jsx
│   │   ├── pages/           # Application pages
│   │   │   ├── About.jsx
│   │   │   ├── Appointment.jsx
│   │   │   ├── Contact.jsx
│   │   │   ├── Doctors.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── MyAppointments.jsx
│   │   │   ├── MyProfile.jsx
│   │   │   └── Verify.jsx
│   │   ├── context/         # React context for state management
│   │   ├── assets/          # Static assets
│   │   ├── App.jsx          # Main application component
│   │   └── main.jsx         # Application entry point
│   ├── package.json
│   └── vite.config.js
│
├── admin/                    # Admin panel React application
│   ├── src/
│   │   ├── components/      # Admin UI components
│   │   │   ├── Navbar.jsx
│   │   │   └── Sidebar.jsx
│   │   ├── pages/           # Admin pages
│   │   │   ├── Admin/
│   │   │   ├── Doctor/
│   │   │   └── Login.jsx
│   │   ├── context/         # Admin context management
│   │   ├── assets/          # Admin assets
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
│
└── backend/                  # Node.js Express API
    ├── config/              # Database and service configurations
    ├── controllers/         # Business logic controllers
    ├── middleware/          # Custom middleware functions
    ├── models/              # Database models
    │   ├── appointmentModel.js
    │   ├── doctorModel.js
    │   └── userModel.js
    ├── routes/              # API route definitions
    ├── server.js            # Main server file
    └── package.json
```

## 🚦 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB database
- Cloudinary account (for image storage)
- Stripe account (for payments)
- Razorpay account (for Indian payments)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Gauravdub-git/Doctor_Appointment_System.git
   cd Doctor_Appointment_System
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   ```
   
   Create a `.env` file in the backend directory:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   STRIPE_SECRET_KEY=your_stripe_secret_key
   RAZORPAY_KEY_ID=your_razorpay_key_id
   RAZORPAY_KEY_SECRET=your_razorpay_key_secret
   ```

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   ```
   
   Create a `.env` file in the frontend directory:
   ```env
   VITE_BACKEND_URL=http://localhost:5000
   ```

4. **Admin Panel Setup**
   ```bash
   cd ../admin
   npm install
   ```
   
   Create a `.env` file in the admin directory:
   ```env
   VITE_BACKEND_URL=http://localhost:5000
   ```

### Running the Application

1. **Start the Backend Server**
   ```bash
   cd backend
   npm run server  # For development with nodemon
   # or
   npm start      # For production
   ```

2. **Start the Frontend Application**
   ```bash
   cd frontend
   npm run dev
   ```

3. **Start the Admin Panel**
   ```bash
   cd admin
   npm run dev
   ```

The applications will be available at:
- Frontend: `http://localhost:5173`
- Admin Panel: `http://localhost:5174`
- Backend API: `http://localhost:5000`

## 📱 Usage

### For Patients
1. Register or log in to your account
2. Browse available doctors by specialty
3. Select a doctor and available time slot
4. Complete the booking with secure payment
5. Manage your appointments from the dashboard

### For Administrators
1. Access the admin panel with admin credentials
2. Manage doctor profiles and availability
3. Monitor appointment bookings and cancellations
4. Handle user accounts and system settings
5. View analytics and system reports

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/verify` - Email verification

### Appointments
- `GET /api/appointments` - Get user appointments
- `POST /api/appointments/book` - Book new appointment
- `PUT /api/appointments/:id` - Update appointment
- `DELETE /api/appointments/:id` - Cancel appointment

### Doctors
- `GET /api/doctors` - Get all doctors
- `GET /api/doctors/:id` - Get doctor details
- `POST /api/doctors` - Add new doctor (admin only)

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

**Gaurav** - [Gauravdub-git](https://github.com/Gauravdub-git)

## 🙏 Acknowledgments

- React and Vite communities for excellent development tools
- MongoDB for reliable database solutions
- Tailwind CSS for beautiful, responsive designs
- All contributors and users of this system

## 📞 Support

If you encounter any issues or have questions, please:
1. Check the existing issues on GitHub
2. Create a new issue with detailed information
3. Contact the maintainers

---

**Note**: Make sure to configure all environment variables properly before running the application. Refer to the `.env.example` files in each directory for required variables.
