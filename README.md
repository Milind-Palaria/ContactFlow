# ContactFlow

# Overview

**ContactFlow** is a powerful, modern contact management system built using **Spring Boot**. It provides an intuitive interface to store, manage, and organize contacts with smart features, scalability, and an optimized workflow.

---

# Features

- **Contact Management**: Easily add, edit, delete, and view contact information.
- **Search & Filter**: Search for contacts by name, email, or custom filters.
- **Cloud Integration**: Sync contacts with cloud services.
- **User Authentication**: Secure user authentication and authorization using Spring Security.
- **REST API**: Expose a RESTful API for external integrations.
- **Responsive Design**: Built-in responsive design using **TailwindCSS** for optimal experience across devices.
- **Docker Support**: Containerized for seamless deployment with Docker and Docker Compose.
- **Multi-environment Support**: Configured for different environments (development, production, etc.).

---

# Prerequisites

Make sure you have the following installed on your system:

- **Java 11** or higher
- **Maven** (version 3.6.0 or higher)
- **Node.js** (for front-end)
- **Docker** (optional, for containerization)

---

# Dependencies

Key dependencies used in this project:

- **Spring Boot**: Core framework for building the application.
- **Spring Data JPA**: For database interaction.
- **Spring Security**: To handle authentication and authorization.
- **Thymeleaf**: Template engine for rendering front-end views.
- **H2 Database**: In-memory database for development/testing.
- **MySQL/PostgreSQL**: For production environments.
- **TailwindCSS**: Utility-first CSS framework for styling.

Check the `pom.xml` for the full list of dependencies.

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/scm2.0.git
cd scm2.0-main
```

## 2. Set Up Database

For development, SCM uses an H2 in-memory database by default. To configure MySQL/PostgreSQL for production, update the `application.properties` file:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/scm_database
spring.datasource.username=yourUsername
spring.datasource.password=yourPassword
```

## 3. Build the Project

Use Maven to build the project:

```bash
mvn clean install
```

## 4. Run the Application

You can run the application locally by executing:

```bash
mvn spring-boot:run
```

Alternatively, you can run the application using Docker (see below).

---

# Running with Docker

## 1. Build Docker Image

Build the Docker image using the provided Dockerfile:

```bash
docker build -t scm2.0 .
```

## 2. Start with Docker Compose

To start the application with Docker Compose (including databases and other services):

```bash
docker-compose up
```

This will spin up the application along with any dependencies (e.g., MySQL).

---

# Frontend Setup

This project uses **Node.js** for managing front-end dependencies.

## 1. Install Node.js Dependencies

```bash
npm install
```

## 2. Build Frontend Assets

To compile the frontend assets (CSS, JS, etc.) using Tailwind:

```bash
npm run build
```

## 3. Run Development Server (Optional)

If you're developing the frontend, run the following for hot-reloading:

```bash
npm start
```

---

# API Endpoints

Here are some of the key API endpoints exposed by the application:

- `GET /api/contacts` - Fetch all contacts
- `POST /api/contacts` - Add a new contact
- `PUT /api/contacts/{id}` - Update contact details
- `DELETE /api/contacts/{id}` - Delete a contact
- `POST /api/auth/login` - User login

For detailed API documentation, check the Swagger docs at `/swagger-ui.html` after running the application.

---

# Configuration

## Environment Variables

The application uses the following environment variables:

- `DATABASE_URL`: URL for the database connection.
- `SPRING_PROFILES_ACTIVE`: Active Spring profile (e.g., `dev`, `prod`).

You can set these in your environment or use a `.env` file for Docker configurations.

