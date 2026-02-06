# CST8915 Lab 2: Refactor the Algonquin Pet Store application

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## 1.Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=iu4PalPRNQU)

---

## 2.Reflection Questions

### i.What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology? 

 - **Configurations:** I removed hard-coded values like the RabbitMQ connection string and port numbers from the source code, replacing them with environment variables loaded from a .env file. The updated index.js file now uses the dotenv library to load environment variables from a .env file during development only.
- **Backing Services factors:** I updated the Order Service to connect to RabbitMQ via a URL provided in these variables instead of a local instance.

### ii.Why is it important to use environment variables instead of hard-coding configurations in your application?

Because environment variables keep secrets safe on the server, for example,hard-coding passwords in the code is dangerous because secrets will be exposed on GitHub.

### iii.Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

Because separate repositories gives each service independence. This means different teams can work on the Order Service or Product Service at the same time without conflicts. It helps scalability because we can update or fix just one service without redeploying the whole system.

---


## 3.Links to the three service repositories created

- order-service:https://github.com/Shan-AC/order-service
- product-service:https://github.com/Shan-AC/product-service
- store-front:https://github.com/Shan-AC/store-front
