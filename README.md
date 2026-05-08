# 🚀 CI/CD Pipeline using Jenkins & Docker

![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-blue)
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![DevOps](https://img.shields.io/badge/DevOps-Automation-green)
![Flask](https://img.shields.io/badge/Flask-Python-lightgrey)

---

## 📌 Overview

This project demonstrates a CI/CD pipeline using Jenkins and Docker to automate deployment of a Flask application.

It automates:
- Pulling code from GitHub  
- Building Docker image  
- Running container  
- Replacing old version automatically  

---

## 🧰 Tech Stack

- Jenkins  
- Docker  
- GitHub  
- Python (Flask)  
- Linux  

---

## ⚙️ Pipeline Stages

### 1️⃣ Clone
Get latest code from GitHub

### 2️⃣ Build
Build Docker image using Dockerfile

### 3️⃣ Run
Stop old container and run new one

---

## 🔁 CI/CD Flow

GitHub → Jenkins → Build Image → Run Container → Flask App 🚀

---

## 🐳 Docker Commands

docker build -t devops-app .

docker run -d -p 5000:5000 devops-app

docker stop devops-app-container

docker rm devops-app-container

---

## 📦 How to Run Locally

Clone repo:
git clone https://github.com/Abdel-3ziz/CI-CD-Pipeline-with-Jenkins-and-Docker.git  
cd CI-CD-Pipeline-with-Jenkins-and-Docker  

Build image:
docker build -t devops-app .

Run container:
docker run -d -p 5000:5000 devops-app  

Open:
http://localhost:5000  

---

## ⚙️ Jenkins Pipeline (Jenkinsfile)

node {

    stage('Clone') {
        git branch: "main",
            url: "https://github.com/Abdel-3ziz/CI-CD-Pipeline-with-Jenkins-and-Docker.git"
    }

    stage('Build') {
        sh 'docker build -t devops-app .'
    }

    stage('Run') {
        sh '''
            docker stop devops-app-container || true
            docker rm devops-app-container || true
            docker run -d -p 5000:5000 --name devops-app-container devops-app
        '''
    }
}

---

## 🧹 Improvements

- Add testing stage  
- Use Docker Compose  
- Push image to DockerHub  
- Use Jenkins credentials  
- Add webhook trigger  
- Add rollback strategy  

---

## 📸 Architecture

GitHub → Jenkins → Docker → Container → App Running

---

## 👨‍💻 Author

Abdelaziz — DevOps Enthusiast 🚀
