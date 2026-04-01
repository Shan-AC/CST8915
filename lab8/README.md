# CST8915 Lab 8: Deploying and Managing the Algonquin Pet Store (On Steroids)

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## 1.Demo Video

🎥 [Watch Demo Video](https://youtu.be/HMxC-3hPzlg)

---

## 2.Explanation of the solution to Task 2

### i. MongoDB Alternative: Azure Cosmos DB for MongoDB
* **Purpose**: A fully managed, distributed NoSQL database service that supports the MongoDB wire protocol.
* **Why it's a good fit**: 
    * **Automatic Scaling**: It automatically scales throughput and storage based on demand.
    * **High Availability**: Offers built-in high availability with up to 99.999% SLA.
    * **No Infrastructure Management**: It provides automated backups and patching, eliminating the need to manually manage Kubernetes StatefulSets, Persistent Volume Claims (PVCs), or database sharding.

### ii. RabbitMQ Alternative: Azure Service Bus
* **Purpose**: A fully managed enterprise-grade message broker with support for queues and topics.
* **Why it's a good fit**: 
    * **Persistence by Default**: It inherently provides persistent message storage, ensuring no data loss if a consumer goes down.
    * **Enterprise Reliability**: Features built-in high availability, geo-disaster recovery, and security features out-of-the-box.
    * **Serverless Operation**: Completely eliminates the operational overhead and ephemeral data risks associated with managing self-hosted RabbitMQ pods in a cluster.

## 3. Attched file

[aps-all-in-one-Task1.yaml file used for Task 1](aps-all-in-one-Task1.yaml)

[aps-all-in-one-Task2.yaml file used for Task 2](aps-all-in-one-Task2.yaml)