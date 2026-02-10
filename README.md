# nodeapp-ecs
# Node.js Application Deployment on AWS ECS 🚀

This project demonstrates how to build, containerize, and deploy a **Node.js application** to **AWS ECS (Elastic Container Service)** using **Docker** and **GitHub Actions CI/CD**.

---

## 📌 Project Overview

- Simple Node.js web application
- Dockerized using a `Dockerfile`
- Deployed to AWS ECS (Fargate / EC2)
- CI/CD pipeline using GitHub Actions
- Image stored in AWS ECR

---

## 🛠️ Tech Stack

- **Node.js**
- **Docker**
- **AWS ECS**
- **AWS ECR**
- **GitHub Actions**
- **Linux (Ubuntu runner)**

---

## 📂 Project Structure
nodeapp-ecs/
├── .github/
│ └── workflows/
│ └── deploy.yml # GitHub Actions workflow
├── app.js # Node.js application
├── package.json # Node dependencies
├── Dockerfile # Docker image build file
├── Task-def-revision1.json # ECS task definition
└── README.md # Project documentation

---

## 🚀 Application Flow
Code Push (GitHub)
↓
GitHub Actions CI/CD
↓
Docker Image Build
↓
Push Image to AWS ECR
↓
Update ECS Task Definition
↓
Deploy to ECS Service

---

## 🐳 Docker Setup

### Build Docker Image
```bash
docker build -t nodeapp-ecs .

# Run Container Locally
docker run -p 8080:8080 nodeapp-ecs
☁️ AWS ECS Requirements

AWS Account

ECS Cluster

ECS Service

ECR Repository

IAM user with ECS & ECR permissions

🔐 GitHub Secrets

Add the following secrets in GitHub:

AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY

🧾 ECS Task Definition

Task definition file:

Task-def-revision1.json


Defines:

Container name

Image

Port mapping

CPU & memory

▶️ Run Application Locally
npm install
node app.js


Access the app:

http://localhost:8080

📈 Future Improvements

Add Application Load Balancer

Enable HTTPS

Add CloudWatch logs

Add staging & production environments

