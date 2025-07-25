# Hospital Management System

A modern, full-stack hospital management system for seamless hospital operations, built with React, Tailwind CSS, Zustand, Lucide React, Node.js, Express, and MS SQL Server.

---

## 🚀 Project Overview

This is a role-based hospital management platform designed to streamline hospital workflows for administrators, doctors, and patients. It provides real-time dashboards, management tools, and a beautiful, responsive UI for all user types.

---

## 🛠️ Tech Stack

- **Frontend:** React, Tailwind CSS, Zustand, Lucide React, React Router
- **Backend:** Node.js, Express, mssql (MS SQL Server)
- **Database:** MS SQL Server

---

## ✨ Features

### Authentication & Role-Based Access
- Secure login for Admin, Doctor, and Patient roles
- Role-based dashboards and navigation

### Admin Dashboard
- Overview widgets: doctors, patients, appointments, billing, pharmacy, labs, etc.
- Management pages for:
  - Users
  - Doctors
  - Patients
  - Appointments
  - Pharmacy (medicines)
  - Labs (lab tests)
  - Billing
  - Ambulances
  - Feedback
- CRUD operations for all entities

### Doctor Dashboard
- Overview: today's appointments, total patients, pending labs, critical patients
- Appointments management
- Patient list and details
- Lab test management
- Pharmacy (prescribe/view medicines)
- Responsive, real-time data

### Patient Dashboard
- Overview: upcoming appointments, lab results, billing, etc.
- Book/view appointments
- View available doctors
- View all available medicines
- View lab reports
- Request ambulance
- Submit/view feedback

---

## 📦 Project Structure

```
hospital-system/
├── back_end/           # Node.js/Express backend
│   ├── config/         # Database config
│   ├── controller/     # Route controllers
│   ├── routes/         # API routes
│   └── server.js       # Entry point
├── front_end/          # React frontend
│   ├── src/
│   │   ├── components/ # UI and layout components
│   │   ├── pages/      # Page components (dashboards, management)
│   │   ├── store/      # Zustand stores
│   │   └── App.jsx     # Main app
│   └── ...
├── README.md           # This file
└── ...
```

---

## ⚡ Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- npm
- MS SQL Server (local or remote)

### 1. Clone the Repository
```bash
git clone <repo-url>
cd hospital-system
```

### 2. Backend Setup
```bash
cd back_end
npm install
# Configure your .env file with DB credentials (see config/db.js)
npm start
```

### 3. Frontend Setup
```bash
cd ../front_end
npm install
npm run dev
```

### 4. Access the App
- Open [http://localhost:5173](http://localhost:5173) in your browser.
- Login as Admin, Doctor, or Patient (see your Users table for credentials).

---

## 📝 Usage Notes
- **Role-based routing:** Users are redirected to their dashboard after login.
- **Admin:** Full access to all management features.
- **Doctor:** Can view/manage their appointments, patients, labs, and more.
- **Patient:** Can view appointments, doctors, medicines, labs, and request ambulance.
- **Medicines:** All patients see all available medicines (no patient-specific filtering yet).
- **API Proxy:** The frontend uses a Vite proxy to connect to the backend (`/api/*` routes).

---

## 📚 Customization & Extending
- To add patient-specific medicines, implement a patient-medicine relationship in the backend and expose an endpoint like `/api/pharmacy/patient/:id`.
- To add more granular permissions, implement route protection using a PrivateRoute/ProtectedRoute component.
- Easily extend dashboards with more widgets, analytics, or management features.




