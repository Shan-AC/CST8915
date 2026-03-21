# CST8915 Lab 7: Introduction to Kubernetes Basics

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/8-OYYFa9CkE)

---

## Analysis of the RabbitMQ configuration issues

### Whether RabbitMQ is a stateless or stateful application

RabbitMQ is a Stateful application. Unlike a web frontend which is stateless and can be replaced easily, RabbitMQ needs to store data such as message queues, exchange configurations, and user credentials. 


### The implications of running RabbitMQ without persistent storage

All data is stored in the container's temporary storage. This storage is tied directly to the lifecycle of the specific Pod instance.



### What happens when the RabbitMQ pod is deleted or restarted

Kubernetes creates a completely new Pod. 

All previously created queues, and custom settings are permanently lost. The system returns to its initial empty state.

### Potential solutions to this problem (research-based)

Instead of a Deployment, we should use a StatefulSet controller, which is designed for managing stateful applications.

We need to define a PersistentVolumeClaim (PVC) to request stable storage (like Azure Disk or Azure Files). This storage exists independently of the Pod lifecycle, so when a Pod restarts, it can "re-attach" to its old data.

### Does using Azure Service Bus solve the issues identified with RabbitMQ Configuration in this Lab?

Yes. Switching to Azure Service Bus would solve this issuse: Managed Persistence: Azure handles all data storage and backups. We don't need to manage disks or volumes in our cluster.

### Notes about setup challenges or lessons learned.

One of the biggest challenges was accessing the RabbitMQ UI through the EXTERNAL-IP address. I encountered a "JSON Object Not Found" error, which I learned was caused by Nginx path rewrite issues. I solved this by using kubectl port-forward for the demonstration. This taught me that configuring a Reverse Proxy in a microservice architecture requires very precise path mapping.

