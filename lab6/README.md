# CST8915 Lab 6: Deploy Algonquin Pet Store to Azure Kubernetes Service (AKS)

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## 1.Demo Video

🎥 [Watch Demo Video](https://youtu.be/SsAEpJ-0g5Y)

---

## 2.Reflection Question

### Why  can we access different services using the same IP address?

Because the store-front container uses Nginx as a Reverse Proxy, the nginx.conf file defines routing rules. When I go to the /products path, Nginx automatically forwards my request to the internal product-service. So, we only need to expose one public IP to the internet.