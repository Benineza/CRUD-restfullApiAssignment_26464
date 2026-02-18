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

### 1️⃣ Create Product (POST)
<img width="1276" height="718" alt="Image" src="https://github.com/user-attachments/assets/99c7de7a-3786-457b-b9a1-2b11043a61b7" />

### 2️⃣ Read Products (GET)
![Read Products](Screenshots/2_Read_GET_Products.png)

### 3️⃣ Update Product (PUT)
![Update Product](Screenshots/3_Update_PUT_a_Product.png)

### 4️⃣ Partial Update - Stock Only (PATCH)
![Partial Update](Screenshots/Partial_Update_PATCH_Update_only_stock_quantity.png)

### 5️⃣ Delete Product (DELETE)
![Delete Product](Screenshots/4_Delete_DELETE_deleting_a_Product.png)
