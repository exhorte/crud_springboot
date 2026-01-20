# CRUD Spring Boot REST API

## 📌 Description

This project is a **CRUD REST API** developed with **Spring Boot** as part of my **L3 Full-Stack Developer** training.
It exposes RESTful endpoints to manage a `Person` resource and connects to a **MySQL** database using **Spring Data JPA (Hibernate)**.

The API is designed following good backend practices: layered architecture, proper HTTP status codes, and clean request/response handling. It is intended to be tested and consumed using tools like **Postman** or integrated into a frontend application.

---

## 🚀 Technologies Used

* **Java 25**
* **Spring Boot 4.x**
* **Spring Data JPA (Hibernate)**
* **MySQL**
* **Maven**
* **Tomcat (Embedded)**
* **Postman** (API testing)

---

## 📂 Project Structure

```
src/main/java
└── com.example.crud_springboot
    ├── CrudSpringbootApplication.java
    ├── controller
    │   └── PersonController.java
    ├── model
    │   └── Person.java
    └── repository
        └── PersonRepository.java

src/main/resources
└── application.properties
```

---

## 🔧 Configuration

### Database Configuration (`application.properties`)

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/crud_springboot
spring.datasource.username=root
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.open-in-view=false
```

Make sure that:

* MySQL is running
* The database `crud_springboot` exists
* MySQL version is **8.0 or higher** (recommended)

---

## 🔗 API Endpoints

Base URL:

```
http://localhost:8080/api/persons
```

### ➤ Get all persons

```
GET /api/persons
```

### ➤ Get a person by ID

```
GET /api/persons/{id}
```

### ➤ Create a new person

```
POST /api/persons
```

**Request Body (JSON):**

```json
{
  "name": "John Doe",
  "city": "Dakar",
  "phoneNumber": "771234567"
}
```

### ➤ Update a person

```
PUT /api/persons/{id}
```

### ➤ Delete a person

```
DELETE /api/persons/{id}
```

---

## 🧪 Testing with Postman

* All endpoints were tested using **Postman**
* HTTP status codes are properly handled (`200`, `201`, `404`)
* JSON request and response formats are respected

---

## ✅ Features

* Full CRUD operations
* RESTful architecture
* Clean controller logic
* Database persistence with JPA
* Ready to be consumed by any frontend (React, Angular, etc.)

---

## 👨‍💻 Author

**Exhorte Mboumba**
L3 Full-Stack Developer
Backend: Java | Spring Boot | MySQL

---

## 📄 License

This project is for educational purposes and personal learning.
