# CST8915 Lab 3: Deploying the Algonquin Pet Store on Azure

**Student Name**: Shan Jiang

**Student ID**: 041179466

**Course**: CST8915 Full-stack Cloud-native Development

**Semester**: Winter 2026

---

## 1.Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=3ba6AqzK9Es)

 - "Note: Due to the subscription policy violation error on Azure Static Web Apps, the Store-Front was run locally (localhost:8080) as per professor's approval. The environment variables shown in the video are from the local .env file."
---

## 2.Reflection Questions

### i.What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

At the beginning, I created the product-service-python folder inside my main CST8915 repository. This caused a lot of problems because the GitHub Actions workflow could not find the correct path to my code and requirements.txt. The deployment kept failing.I tried to fix the path in the YAML file, but it was very confusing. Finally, I decided to create a brand new repository just for the product-service-python.

### ii.How does deploying microservices on Azure Web App Service differ from running them locally?

Running in locally, I just need to run commands like python app.py or npm run serve, and I can access everything on localhost with a specific port. I can see errors directly in my terminal. But running in Azure Web App Service, first step is to configure the server environment, and I have to use the real, long URL provided by Azure instead of localhost.

### iii.Why is it important to use environment variables for configurations in a cloud environment?

Because there are 2 main reasions: security and flexibility. 

First, we can not write sensitive information, like password, directly in our code. If we push the code to GitHub, everyone can see it. Using environment variables keeps these secrets safe in the Azure settings. 

Second, it makes it easy to change configurations. For example, if my RabbitMQ IP address changes, I only need to update the environment variable in the Azure Portal. I don't need to rewrite my code or redeploy the whole application.

---


## 3.Links to the three service repositories created

- order-service:https://github.com/Shan-AC/order-service
- product-service-python:https://github.com/Shan-AC/product-service-python

---

- store-front:https://github.com/Shan-AC/store-front  

(Due to the subscription policy violation error on Azure Static Web Apps, the Store-Front was run locally )
