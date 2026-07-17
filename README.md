# 🚗 Vehicle Rental System - Database Design & SQL Queries

## 📌 Project Overview

The **Vehicle Rental System** is a relational database project designed to manage vehicle rentals efficiently. It demonstrates database normalization, Entity Relationship Diagram (ERD) design, and SQL querying techniques using **PostgreSQL**.

The system manages three main entities:

- Users
- Vehicles
- Bookings

This project also demonstrates the use of:

- Primary Keys
- Foreign Keys
- One-to-One Relationships
- One-to-Many Relationships
- Many-to-One Relationships
- SQL JOIN
- EXISTS
- WHERE Clause

---

# 🎯 Objectives

This project was created to demonstrate the ability to:

- Design a relational database
- Create an Entity Relationship Diagram (ERD)
- Establish relationships between tables
- Apply Primary Key and Foreign Key constraints
- Write SQL queries using JOIN, EXISTS, WHERE, ORDER BY, GROUP BY, etc.
- Maintain data integrity using constraints

---

# 🗄 Database Schema

The system contains **three tables**:

## 1. Users

Stores customer and administrator information.

| Column | Description |
|---------|-------------|
| id | Primary Key |
| name | User's full name |
| email | Unique email address |
| password | User password |
| phone | Contact number |
| role | Admin / Customer |

### Constraints

- Primary Key
- Unique Email
- NOT NULL fields

---

## 2. Vehicles

Stores vehicle information available for rent.

| Column | Description |
|---------|-------------|
| id | Primary Key |
| name | Vehicle name |
| type | Car / Bike / Truck |
| model | Vehicle model |
| registration_number | Unique registration number |
| rental_price_per_day | Rental price |
| availability_status | Available / Rented / Maintenance |

### Constraints

- Primary Key
- Registration Number Unique

---

## 3. Bookings

Stores rental booking information.

| Column | Description |
|---------|-------------|
| id | Primary Key |
| user_id | Foreign Key → Users |
| vehicle_id | Foreign Key → Vehicles |
| start_date | Rental start date |
| end_date | Rental end date |
| booking_status | Pending / Confirmed / Completed / Cancelled |
| total_cost | Total rental amount |

### Constraints

- Primary Key
- Foreign Key (Users)
- Foreign Key (Vehicles)

---

# 🔗 Database Relationships

## One-to-Many

### Users → Bookings

- One user can create multiple bookings.
- Each booking belongs to only one user.

```
Users (1) --------< Bookings (Many)
```

---

## One-to-Many

### Vehicles → Bookings

- One vehicle can have multiple bookings over time.
- Each booking belongs to only one vehicle.

```
Vehicles (1) --------< Bookings (Many)
```

---

# 📊 Entity Relationship Diagram (ERD)

```
+-------------+
|    Users    |
+-------------+
| id (PK)     |
| name        |
| email       |
| password    |
| phone       |
| role        |
+-------------+
       |
       | 1
       |
       | *
+----------------+
|    Bookings    |
+----------------+
| id (PK)        |
| user_id (FK)   |
| vehicle_id(FK) |
| start_date     |
| end_date       |
| booking_status |
| total_cost     |
+----------------+
       *
       |
       | 1
+------------------+
|     Vehicles     |
+------------------+
| id (PK)          |
| name             |
| type             |
| model            |
| registration_no  |
| price_per_day    |
| availability     |
+------------------+
```

---

# 💼 Business Logic

## Users

- Store Admin and Customer accounts
- Unique email for each user
- Store password securely
- Store contact information

---

## Vehicles

- Each vehicle has a unique registration number
- Vehicle types include:
  - Car
  - Bike
  - Truck
- Track availability status:
  - Available
  - Rented
  - Maintenance

---

## Bookings

Each booking records:

- Customer information
- Vehicle information
- Rental start date
- Rental end date
- Booking status
- Total rental cost

Booking status values:

- Pending
- Confirmed
- Completed
- Cancelled

---

# 🛠 Technologies Used

- PostgreSQL
- SQL
- pgAdmin
- ER Diagram

---

# 📚 SQL Concepts Used

- CREATE TABLE
- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- NOT NULL
- INSERT
- UPDATE
- DELETE
- SELECT
- WHERE
- ORDER BY
- GROUP BY
- INNER JOIN
- LEFT JOIN
- EXISTS
- Aggregate Functions

---

# 📂 Project Structure

```
Vehicle-Rental-System
│
├── schema.sql
├── insert_data.sql
├── queries.sql
├── erd.png
└── README.md
```

---

# 🚀 Learning Outcomes

After completing this project, you will understand:

- Relational database design
- ERD creation
- Database normalization
- SQL querying
- Table relationships
- Data integrity using constraints
- Real-world booking system implementation

---

# 👩‍💻 Author

**Jakia Sultana**

- GitHub: https://github.com/Jakia123sultana
- Email: jakiasultanaania@gmail.com
