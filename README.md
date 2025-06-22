# -airbnb-clone-project.

## 📌 Overview
This project is a clone of the Airbnb platform, aiming to replicate its core functionality including user registration, property listing, booking, and reviews. It serves as a full-stack software engineering challenge using modern development practices.

---

## 👥 Team Roles

- **Frontend Developer**: Designs and implements the user interface using HTML, CSS, and JavaScript frameworks.
- **Backend Developer**: Builds the server-side logic using Django and RESTful APIs.
- **Database Administrator (DBA)**: Designs, manages, and optimizes the PostgreSQL database.
- **DevOps Engineer**: Sets up CI/CD pipelines, Docker, and manages deployment environments.
- **QA Engineer**: Tests features, handles bug tracking, and ensures software quality.

---

## 🧰 Technology Stack

- **Django**: Web framework used to build the backend logic and REST APIs.
- **PostgreSQL**: Relational database for storing users, properties, bookings, etc.
- **GraphQL**: Alternative API layer for efficient data querying.
- **HTML/CSS/JavaScript**: Frontend technologies for UI/UX.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **GitHub Actions**: CI/CD pipeline tool to automate testing and deployment.

---

## 🗃️ Database Design

### Key Entities:

1. **User**
   - id (PK)
   - name
   - email
   - password
   - is_host (boolean)

2. **Property**
   - id (PK)
   - user_id (FK to User)
   - title
   - description
   - location
   - price

3. **Booking**
   - id (PK)
   - user_id (FK to User)
   - property_id (FK to Property)
   - start_date
   - end_date

4. **Review**
   - id (PK)
   - user_id (FK to User)
   - property_id (FK to Property)
   - rating
   - comment

5. **Payment**
   - id (PK)
   - booking_id (FK to Booking)
   - amount
   - payment_date
   - status

### Relationships:
- A user can own multiple properties.
- A property can have many bookings.
- A booking can have one payment.
- A property can have multiple reviews.

---

## ⚙️ Feature Breakdown

- **User Management**: Users can sign up, log in, update profiles, and switch between guest/host roles.
- **Property Management**: Hosts can list properties, upload images, and set availability.
- **Booking System**: Guests can book properties by date, view availability, and manage their bookings.
- **Review System**: Guests can leave ratings and comments after a stay.
- **Payment Integration**: Secure checkout flow for booking payments with tracking and confirmation.

---

## 🔐 API Security

- **Authentication**: Only logged-in users can book properties or leave reviews.
- **Authorization**: Only hosts can edit or delete their properties.
- **Rate Limiting**: Prevents abuse by limiting the number of API requests.
- **Data Encryption**: Ensures user data and payments are protected.
- **Input Validation**: Prevents SQL injection and XSS attacks.

---

## 🚀 CI/CD Pipeline

- **CI (Continuous Integration)**: Automatically tests new changes using GitHub Actions before merging.
- **CD (Continuous Delivery)**: Deploys to staging/production using Docker and GitHub Actions.
- **Tools**:
  - GitHub Actions for automation
  - Docker for containerized environments
  - Heroku/AWS/DigitalOcean for deployment (optional)

---

