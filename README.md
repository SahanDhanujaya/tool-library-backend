# ⚙️ Tool Library Backend
### ECA Final Project - Microservices Architecture

A robust, scalable backend system built with **Spring Boot** and a microservices-based architecture. This system manages tool inventories, user authentication, and transaction logs using a polyglot persistence approach.

---

## 🏗️ Architecture Overview

This project is designed as a distributed system to ensure high availability and independent scalability of services.

* **Service Framework:** Spring Boot 3.x
* **Architecture Style:** Microservices (RESTful APIs)
* **Security:** Spring Security (JWT & RBAC)
* **Discovery & Config:** [e.g., Spring Cloud Netflix Eureka / Config Server]
* **API Gateway:** [e.g., Spring Cloud Gateway]

---

## 🗄️ Database Strategy

We utilize **Polyglot Persistence** to handle different data requirements:

* **MySQL:** Used for structured, relational data such as User accounts, Tool metadata, and Transaction records.
* **MongoDB:** Used for unstructured or high-volume data such as Tool usage logs, activity history, or extended tool specifications.

---

## 💻 Tech Stack

* **Java Version:** 17+
* **Build Tool:** Maven / Gradle
* **Framework:** Spring Boot
* **Persistence:** Spring Data JPA (MySQL), Spring Data MongoDB
* **Containerization:** Docker & Docker Compose
* **Authentication:** JWT (JSON Web Tokens)

---

## 🚀 Getting Started

### 1. Prerequisites
* JDK 17 or higher
* MySQL Server (Port: 3306)
* MongoDB Server (Port: 27017)
* Maven

### 2. Configuration
Update the `application.yml` or `application.properties` in each microservice with your database credentials:

```
yaml
---
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/tool_library_db
    username: your_username
    password: your_password
  data:
    mongodb:
      uri: mongodb://localhost:27017/tool_logs_db
```

## 3. Installation & RunClone the repository and build the services:Bashgit clone [https://github.com/SahanDhanujaya/tool-library-backend.git](https://github.com/SahanDhanujaya/tool-library-backend.git)

mvn clean install
mvn spring-boot:run

---

## 📁 Project Structure
```
Plaintexttool-library-backend/
---
├── discovery-service/    # Service Registry (Eureka)
├── gateway-service/      # API Gateway
├── auth-service/         # JWT & User Management (MySQL)
├── tool-service/         # Inventory Management (MySQL)
├── log-service/          # Activity & History Tracking (MongoDB)
└── common-library/       # Shared DTOs and Utilities
```
---
## 🛠️ API Endpoints (Core)
