# 🚀 Jenkins Automation with Docker

![Jenkins](https://img.shields.io/badge/Jenkins-Automation-red?logo=jenkins)
![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)
![CI/CD](https://img.shields.io/badge/CI/CD-Pipeline-success)
![Status](https://img.shields.io/badge/Status-Working-brightgreen)

> 🔥 **Automating Docker Image Build and Container Execution using Jenkins Pipeline**

---

## 📌 Project Overview

This project demonstrates **CI/CD automation** using **Jenkins and Docker**.  
The Jenkins pipeline automatically builds a Docker image and runs a container whenever the job is triggered.

---

## 🛠️ Tech Stack

- 🧩 Jenkins  
- 🐳 Docker  
- 🐍 Python (Flask)  
- 🌐 GitHub  
- 💻 WSL (Ubuntu)  

---

## 📂 Project Structure

Jenkin_Automation_Docker/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
└── README.md
---

## ⚙️ CI/CD Workflow

---

## 🧪 COMPLETE PROCEDURE TO RUN THE PROJECT

### 🔹 Step 1: Install Required Software

Ensure the following are installed:

- Docker Desktop (with WSL integration enabled)
- Git
- WSL (Ubuntu)
- Jenkins running inside Docker

---

### 🔹 Step 2: Clone the Repository

```bash
git clone https://github.com/SrikanthRaj007/Jenkin_Automation_Docker.git
cd Jenkin_Automation_Docker
bash```


### 🔹 Step 3: Run Jenkins Using Docker

If Jenkins already exists:

docker start jenkins

If Jenkins is not created:

docker run -d \
  --name jenkins \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --restart unless-stopped \
  jenkins/jenkins:lts

###🔹 Step 4: Open Jenkins Dashboard

Open browser and go to:

http://localhost:8080


Login using Jenkins credentials.




