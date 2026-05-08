# 🚀 CI/CD Pipeline using Jenkins & Docker

![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-blue)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![DevOps](https://img.shields.io/badge/DevOps-Automation-green)

---

## 📌 Overview
This project demonstrates a simple CI/CD pipeline using **Jenkins** and **Docker** to automate building and deploying a containerized Flask application.

The pipeline automates the process of:
- Cloning the source code from GitHub
- Building a Docker image
- Running the application inside a Docker container

---

## 🧰 Tech Stack
- Jenkins
- Docker
- GitHub
- Python (Flask)

---

## ⚙️ Pipeline Stages

### 1️⃣ Clone Stage
Pulls the latest code from the GitHub repository.

### 2️⃣ Build Stage
Builds a Docker image using the Dockerfile.

### 3️⃣ Run Stage
Stops any existing container and runs a new instance of the application.

---

## 🔁 CI/CD Flow
