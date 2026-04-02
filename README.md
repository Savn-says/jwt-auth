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

<img width="427" height="802" alt="Screenshot 2026-04-02 070245" src="https://github.com/user-attachments/assets/332d7edf-b9db-4196-8561-2da913ff79a0" />

### 🔹 Login API (Postman)

<img width="1743" height="626" alt="Screenshot 2026-04-02 065236" src="https://github.com/user-attachments/assets/de5229fa-4e5c-4516-9ba4-e01ce75f0e89" />

<img width="1750" height="712" alt="Screenshot 2026-04-02 065254" src="https://github.com/user-attachments/assets/129df6e8-1b40-42f3-b4fe-8b717912a80c" />

### 🔹 Invalid Login

 <img width="1769" height="749" alt="Screenshot 2026-04-02 065425" src="https://github.com/user-attachments/assets/1e92bc5a-7335-45ef-ae30-67eb3b9e965c" />

### 🔹 Secured API (JWT Token)

<img width="1714" height="708" alt="Screenshot 2026-04-02 065357" src="https://github.com/user-attachments/assets/e962f119-ae15-47a3-907a-3efbae8f7ebf" />

### 🔹 Database (MySQL)

<img width="504" height="92" alt="Screenshot 2026-04-02 065744" src="https://github.com/user-attachments/assets/80261ec3-cd0a-49c6-945c-d55ac1848f66" />

 


## ▶️ Run Project

```bash
mvn spring-boot:run
```

---

 
