# 🚗 Vehicle Rental System - Backend

A scalable and modular RESTful API for a Vehicle Rental System built with **Node.js**, **Express.js**, **TypeScript**, and **PostgreSQL**. The application provides secure authentication, vehicle management, booking management, and role-based access control for administrators and customers.

---

## ✨ Features

- 🔐 Secure user authentication and authorization
- 👥 Role-based access control (Admin & Customer)
- 🚗 Vehicle management (CRUD operations)
- 📅 Vehicle booking management
- ✅ Booking status management
- 🛡️ Authentication middleware
- 📂 Modular project architecture
- ⚡ RESTful API design
- 🌐 Environment-based configuration
- 📝 Centralized logging middleware

---

## 🛠️ Tech Stack

### Backend

- Node.js
- Express.js
- TypeScript

### Database

- PostgreSQL

### Authentication

- JWT (JSON Web Token)

### Tools

- Git
- Postman
- npm

---

## 📁 Project Structure

```text
src/
├── config/
│   ├── db.ts
│   └── index.ts
│
├── middleware/
│   ├── auth.ts
│   └── logger.ts
│
├── modules/
│   ├── auth/
│   ├── bookings/
│   ├── users/
│   └── vehicle/
│
└── server.ts
```

### Folder Description

| Folder | Description |
|----------|-------------|
| config | Database connection and application configuration |
| middleware | Authentication and request logging middleware |
| modules/auth | Authentication related APIs |
| modules/users | User management APIs |
| modules/vehicle | Vehicle management APIs |
| modules/bookings | Booking management APIs |
| server.ts | Application entry point |

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/Jakia123sultana/Vehicle_Rental_System_Backend.git
```

```bash
cd Vehicle_Rental_System_Backend
```

### Install dependencies

```bash
npm install
```

### Configure environment variables

Create a `.env` file in the project root.

Example:

```env
PORT=5000

DB_HOST=localhost
DB_PORT=5432
DB_NAME=vehicle_rental
DB_USER=postgres
DB_PASSWORD=your_password

JWT_SECRET=your_secret_key
```

---

## ▶️ Run the Project

Development

```bash
npm run dev
```

Production

```bash
npm run build
npm start
```

---

## 📌 API Modules

- Authentication
- Users
- Vehicles
- Bookings

---

## 🔒 Authentication

The API uses **JWT (JSON Web Token)** for securing protected routes.

---

## 📬 API Testing

The API can be tested using:

- Postman
- Thunder Client
- Insomnia

---

## 👩‍💻 Author

**Jakia Sultana**

- GitHub: https://github.com/Jakia123sultana
- Email: jakiasultanaania@gmail.com
