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

## Project Structure

restfullApiAssignment/
├── src/
│ ├── main/
│ │ ├── java/
│ │ │ └── auca/ac/rw/restfullApiAssignment/
│ │ │ ├── controller/ # Handles HTTP requests
│ │ │ │ └── ProductController.java
│ │ │ ├── service/ # Business logic
│ │ │ │ └── ProductService.java
│ │ │ ├── repository/ # Data access layer
│ │ │ │ └── ProductRepository.java
│ │ │ ├── modal/ # Entity/model layer
│ │ │ │ └── Product.java
│ │ │ └── RestfullApiAssignmentApplication.java
│ │ └── resources/
│ │ └── application.properties # DB & application configuration
├── Screenshots/ # API test screenshots
├── pom.xml


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

**Example Product JSON**
```json
{
  "id": 1001,
  "name": "Wireless Bluetooth Headphones",
  "description": "Premium noise-cancelling wireless headphones",
  "price": 89.99,
  "category": "Electronics",
  "stockQuantity": 150
}

