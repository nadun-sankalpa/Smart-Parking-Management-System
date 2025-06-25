# 🚕🚓🚗 Smart Parking Management System (SPMS)

![EurekaDashboard](https://github.com/nadun-sankalpa/Smart-Parking-Management-System/blob/3b964de499d528cfd33436d99f16dcbf3711416b/doc/eureka-dashboard.png)

---

## 🧠 Overview

The **Smart Parking Management System (SPMS)** is a modern, **cloud-native microservices** solution designed to revolutionize urban parking management. It offers real-time parking availability, booking, and management, while also streamlining payment processing. By integrating various Spring Cloud components, SPMS helps reduce city congestion and enhances user convenience.

Whether you're a user looking for a parking spot or a space owner managing availability — SPMS is built to serve both ends with scalability, security, and ease.

---

## 🚀 Tech Stack

| Tech                  | Description                                                       |
|-----------------------|-------------------------------------------------------------------|
| 🧰 Spring Boot         | Backend framework for creating production-grade services         |
| 🌐 Spring Cloud Config | Centralized external configuration management                   |
| 📘 Spring Cloud Eureka | Service registry for dynamic microservice discovery             |
| 🚪 Spring Cloud Gateway| API Gateway for intelligent routing                             |
| 🔐 Spring Security + JWT | Secured login with role-based access using JWT tokens         |
| 🗄 MySQL               | Relational database for data persistence                         |
| 📫 Postman             | API testing, automation, and monitoring                          |
| 🛠 Maven               | Dependency management and project build                          |
| ☕ Java 17+            | Language used for backend development                            |

---

## 🛠 Prerequisites

Make sure the following are installed on your machine:

- ☕ Java 17 or above  
- 🐘 Maven  
- 🐬 MySQL Server  
- 📫 Postman  
- 💻 Git  
- 🌍 Internet connection (for downloading dependencies)

---

## 📦 Microservices Overview

| Microservice     | Port            | Description                              |
|------------------|-----------------|------------------------------------------|
| 👤 **User Service**     | `http://localhost:8081` | Manages user registration and authentication |
| 🚗 **Vehicle Service**  | `http://localhost:8082` | Handles vehicle registration and mapping  |
| 🅿 **Parking Service**  | `http://localhost:8084` | Manages parking slots and availability    |
| 💳 **Payment Service**  | `http://localhost:8085` | Handles payment transactions (mock)       |
| 🚪 **API Gateway**      | `http://localhost:8080` | Centralized gateway for routing requests  |
| 🔍 **Eureka Server**    | `http://localhost:8761` | Service discovery dashboard               |
| 🛠 **Config Server**    | `http://localhost:8888` | Centralized configuration service         |

---

## 🚀 How to Run the Project

> Run each component in the following order:

1. **Start Eureka Server**  
   🔗 [http://localhost:8761](http://localhost:8761)

2. **Start Config Server**  
   🔗 [http://localhost:8888](http://localhost:8888)

3. **Run All Microservices**  
   Make sure they’re all up and registered in Eureka:
   - User Service → `http://localhost:8081`
   - Vehicle Service → `http://localhost:8082`
   - Parking Service → `http://localhost:8084`
   - Payment Service → `http://localhost:8085`

4. **Start API Gateway**  
   🔗 [http://localhost:8080](http://localhost:8080)

---

## 🧪 API Testing with Postman

You can test all API endpoints through the API Gateway using Postman.

### 📫 Import Postman Collection

[📥 Download Postman Collection – smart-parking-management-system.postman_collection.json](smart-parking-management-system.postman_collection.json)

Open Postman → `Import` → Upload the collection → Start testing!

---

## 📊 Eureka Dashboard

Track live service registration with **Spring Cloud Eureka**:

![EurekaDashboard](https://github.com/nadun-sankalpa/Smart-Parking-Management-System/blob/3b964de499d528cfd33436d99f16dcbf3711416b/doc/eureka-dashboard.png)

---

## 🧩 Project Architecture (Optional Enhancement)

You could add a system diagram like this if you have one:

```plaintext
[ User ] --> [ API Gateway ] --> [ User / Vehicle / Parking / Payment Services ]
                          ↕
                    [ Eureka Server ]
                          ↕
                 [ Config Server / MySQL DB ]
