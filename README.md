# Java Spring Boot CRUD API with PostgreSQL

This project demonstrates a simple CRUD (Create, Read, Update, Delete) API using Java Spring Boot with PostgreSQL as the database.

---

## Prerequisites

Before running the project, ensure you have the following installed:

- **Java Development Kit (JDK)** (version 11 or later)
- **Maven** (version 3.6 or later)
- **Docker** (for run PostgreSQL container)
- **IDE** (e.g., IntelliJ IDEA)

---

## Installation Steps

### 1. Clone the Repository
Clone this project to your local machine
### 2. Run PostgresSQL via docker-compose.yaml file that already prepare using the following command: 
```bash
docker compose up
```
### 3. Install Dependencies
Run the following command to install project dependencies:
```bash
mvn clean install
```

---

## Running the Project

### 1. Start the Application
Run the application using the following command:
```bash
mvn spring-boot:run
```

### 2. Verify the API
Once the application is running, use tools like **Postman** or **cURL** to test the API. The base URL is:
```
http://localhost:8080
```

---

## API Endpoints

### **1. Create Product**
**POST** `/products`
- Request Body (JSON):
  ```json
  {
      "name": "Laptop",
      "description": "High-performance laptop",
      "price": 1200.00
  }
  ```
- Response: 201 Created

### **2. Get All Products**
**GET** `/products`
- Response: 200 OK

### **3. Get Product by ID**
**GET** `/products/{id}`
- Response: 200 OK / 404 Not Found

### **4. Update Product**
**PUT** `/products/{id}`
- Request Body (JSON):
  ```json
  {
      "name": "Updated Laptop",
      "description": "Updated description",
      "price": 1300.00
  }
  ```
- Response: 200 OK / 404 Not Found

### **5. Delete Product**
**DELETE** `/products/{id}`
- Response: 204 No Content / 404 Not Found

---

## Folder Structure
```
my-spring-boot-project/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.example.demo/
│   │   │       ├── controller/  # API Controllers
│   │   │       ├── model/       # Entity Classes
│   │   │       └── repository/  # JPA Repositories
│   │   ├── resources/
│   │       ├── application.properties  # Configuration File
```

## License
This project is licensed under the [MIT License](LICENSE).

---

## Author
Developed by pongsakorn-m.
