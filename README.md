# RESTful API - Product Management System

**Student Name:** Moise Benineza  
**Student ID:** 26464  

## Overview
This project is a **RESTful API for a Product Management System** developed using **Spring Boot**. It allows complete CRUD operations (Create, Read, Update, Delete) for managing product inventory in an e-commerce system.  

The API is designed with a **layered architecture** using **Spring Boot**, **Spring Data JPA**, and **PostgreSQL**, and follows REST best practices with proper HTTP methods and status codes.

---

## Technologies Used
- **Java:** JDK 21  
- **Framework:** Spring Boot 4.x  
- **Database:** PostgreSQL 18.x  
- **ORM:** Hibernate (JPA)  
- **Build Tool:** Maven  
- **Server:** Embedded Apache Tomcat  

---

---

## Database Configuration
- **Database Name:** `ecommerce_db`  
- **Host:** `localhost`  
- **Port:** `5432`  
- **Username:** `postgres` (update as needed in `application.properties`)  
- **Hibernate DDL:** Auto-update enabled  

> The `product` table is automatically created in PostgreSQL by Hibernate.

---

## API Endpoints

| Operation                       | Method | URL                                      | Body / Notes                                    |
|---------------------------------|--------|------------------------------------------|------------------------------------------------|
| **Create Product**               | POST   | `/api/products/addProduct`               | JSON body with product details                 |
| **Get All Products**             | GET    | `/api/products/getAllProducts`           | Returns a JSON array of all products          |
| **Update Entire Product**        | PUT    | `/api/products/updateProduct`            | JSON body with full product object            |
| **Partial Update: Stock Only**   | PATCH  | `/api/products/updateProductStock/{id}/{stockQuantity}` | Update only stock quantity of a product       |
| **Delete Product**               | DELETE | `/api/products/deleteProduct/{id}`       | Deletes product by ID                           |

## Screenshots of CRUD Operations

Below are screenshots demonstrating that all CRUD operations are working:

### 1 Create Product (POST)
<img width="1276" height="718" alt="Image" src="https://github.com/user-attachments/assets/99c7de7a-3786-457b-b9a1-2b11043a61b7" />

### 2 Read Products (GET)
<img width="1275" height="719" alt="Image" src="https://github.com/user-attachments/assets/38f5cd1a-57f5-4840-88ed-d1fde799b47e" />

### 3 Update Product (PUT)
<img width="1277" height="723" alt="Image" src="https://github.com/user-attachments/assets/26677ee3-4e0c-4404-a5a7-abbaaa30df05" />

### 4 Partial Update - Stock Only (PATCH)
<img width="1278" height="720" alt="Image" src="https://github.com/user-attachments/assets/ef0a86ac-7fc3-4dc6-a488-c56e3ceb7a3a" />

### 5 Delete Product (DELETE)
<img width="1279" height="720" alt="Image" src="https://github.com/user-attachments/assets/c77e2498-3dd5-41a5-9951-e39e6ddc277c" />
