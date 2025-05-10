# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

  - **Output**
  ![alt text](output/user_health.png)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

  - **Output**
  ![alt text](output/product_health.png)

---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

  - **Output**
  ![alt text](output/order_health.png)

---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Output Health For gateway**
  ![alt text](output/gateway_health.png)
  
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Output**
    ![alt text](output/api_users.png)

  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
    **Output**
    ![alt text](output/api_products.png)

  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```
    **Output - Order List**
    ![alt text](output/api_orders.png)

    **Output - Order Create Via Postman Post method**
    ![alt text](output/api_create_order.png)


---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
2. Once the services are running, use the above endpoints to verify the functionality.

Happy testing!

--- 
