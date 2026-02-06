# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name**: Shan Jiang
**Student ID**: 041179466
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=oQFZIzjSSCc)

---

## Technical Explanations

### Order Service (Node.js)

The Order Service handles customer orders: receiving, processing, and queuing orders. It utilizes Node.js, which offers a non-blocking I/O model ideal for scalable network applications. In the architecture, it functions as the transactional backend service. It receives order details from the Store Front via HTTP requests.


### Product Service (Rust)

The Product Service is responsible for managing and serving product data inventory. It is developed using Rust, because it is a fast, memory-safe language ideal for high-performance APIs. As backend microservice, it handles read-heavy workloads efficiently. It interacts with the Store Front by exposing specific endpoints and responding to HTTP requests with product information.



### Store Front (Vue.js)

The Store Front is the  customer-facing website: the UI that shoppers interact with.It is built with Vue.js, because its lightweight nature and component-based architecture. In the microservices architecture, it serves as the client-side entry point, communicating with the Product Service and Order Service.

