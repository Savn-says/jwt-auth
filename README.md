# 🔐 Spring Boot JWT Authentication API

## 📌 Project Description

This project is a **Spring Boot REST API** that implements **JWT (JSON Web Token) based authentication**. It allows users to log in and receive a token, which can be used to access secured endpoints.

---

## 🚀 Features

* User login authentication
* JWT token generation
* Secure API endpoints
* RESTful API design

---

## 🛠 Technologies Used

* Java
* Spring Boot
* Spring Security
* Spring Data JPA
* MySQL
* Maven
* JWT (JJWT)

---

## 📂 Project Structure

```
com.JWTExample.JWT_Demo
│
├── config
│   └── SecurityConfig.java
│
├── controller
│   └── AuthController.java
│
├── entity
│   └── User.java
│
├── repository
│   └── UserRepository.java
│
├── filter
│   └── Jwtfilter.java
│
└── service
    └── jwtservice.java
```

---

## ⚙️ How It Works

1. User sends login request (`/api/login`)
2. Backend checks username & password from database
3. If valid → JWT token is generated
4. Token is used to access secured APIs

---

## 🔑 API Endpoints

### 🔹 Login

**POST** `/api/login`

**Params:**

```
username=your_username
password=your_password
```

**Response:**

```
JWT Token (if valid)
OR
Invalid Credentials
```

---

### 🔹 Test Endpoint

**GET** `/api/hello`

**Response:**

```
Hello! JWT Authentication Successful
```

---

## 🧩 Dependencies

Add in `pom.xml`:

```xml
<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-impl</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>

<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt-jackson</artifactId>
    <version>0.11.5</version>
    <scope>runtime</scope>
</dependency>
```

---

## 🔒 Security Config

* CSRF disabled
* CORS disabled
* Form login disabled
* JWT-based authentication

---

## 🗄️ Database

**Table:** `users`

| Column   | Type   |
| -------- | ------ |
| id       | Long   |
| username | String |
| password | String |

---

## 📸 Screenshots

### 🔹 Project Structure

 


### 🔹 Login API (Postman)

 


### 🔹 Invalid Login
 

### 🔹 Secured API (JWT Token)
 


### 🔹 Database (MySQL)

 

---



## ▶️ Run Project

```bash
mvn spring-boot:run
```

---

 
