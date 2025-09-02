# ALX Airbnb Database Project - ERD Requirements

## 📘 Project Overview
This project involves designing a relational database system for an Airbnb-like application. The system includes users, properties, bookings, and payments.

---

## 🧱 Entities and Their Attributes

### 🧍 User
- `id` (Primary Key)
- `name`
- `email`
- `phone`
- `created_at`

### 🏠 Property
- `id` (Primary Key)
- `owner_id` (Foreign Key → User.id)
- `name`
- `location`
- `price_per_night`
- `description`
- `created_at`

### 📅 Booking
- `id` (Primary Key)
- `user_id` (Foreign Key → User.id)
- `property_id` (Foreign Key → Property.id)
- `start_date`
- `end_date`
- `status`
- `created_at`

### 💳 Payment
- `id` (Primary Key)
- `booking_id` (Foreign Key → Booking.id)
- `amount`
- `payment_date`
- `payment_method`
- `status`

---

## 🔗 Relationships

| Entity A    | Relationship   | Entity B   | Type         |
|-------------|----------------|------------|--------------|
| User        | owns           | Property   | One-to-Many  |
| User        | makes          | Booking    | One-to-Many  |
| Property    | has            | Booking    | One-to-Many  |
| Booking     | has            | Payment    | One-to-One   |

---



---

## 📁 Files Included
- `airbnb_erd.drawio` (ER diagram source file)
- `airbnb_erd.png` or `.pdf` (image or PDF of the ERD)
- `requirements.md` (this file)
