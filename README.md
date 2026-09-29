# CST8915-Lab1
CST8915 Lab 1 -Azure VM Pet Store Deployment
**Student Name**: Justin
**Student ID**: [041290562]
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

## Demo Video

**YouTube Video:** [Video link will be added here]

## Technical Explanations

### Order Service (Node.js)

The Order Service is responsible for receiving customer orders from the Store Front. It runs on port 3000 and provides a REST API that accepts order requests. It is built with Node.js, a JavaScript runtime that can be used to build scalable backend services.

In the microservices architecture, the Order Service handles the order part of the application. When a customer places an order from the Store Front, the request is sent to the Order Service. The Order Service then sends the order message to RabbitMQ, where it is stored in a durable queue for processing.

### Product Service (Rust)

The Product Service is responsible for providing the product catalog, including product IDs, names, and prices. It is written in Rust, a fast and memory-safe programming language that is suitable for high-performance APIs. The service provides REST API endpoints and runs on port 3030.

In the microservices architecture, the Product Service manages the product information independently from the other services. The Store Front communicates with the Product Service through its REST API to retrieve the products and display them to the customer.

### Store Front (Vue.js)

The Store Front is the customer-facing web application of the Algonquin Pet Store. It is built with Vue.js, a JavaScript framework used to create interactive web applications. It runs on port 8080 and allows customers to view products, select a product, enter a quantity, see the total price, and place an order.

In the microservices architecture, the Store Front acts as the user interface and communicates with the backend services. It retrieves product information from the Product Service on port 3030 and sends customer orders to the Order Service on port 3000. This allows the user interface, product catalog, and order processing to work as separate services while communicating with each other.
