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


---

## 🐳 Docker Commands Used
- docker build
- docker run
- docker stop
- docker rm

---

## 📦 How to Run Locally

```bash
git clone https://github.com/Abdel-3ziz/CI-CD-Pipeline-with-Jenkins-and-Docker.git
cd CI-CD-Pipeline-with-Jenkins-and-Docker

docker build -t devops-app .
docker run -d -p 5000:5000 devops-app
⚙️ Jenkins Pipeline Script
node {

    stage('Clone') {
        echo "Cloning repository..."

        git branch: "main",
            url: "https://github.com/Abdel-3ziz/CI-CD-Pipeline-with-Jenkins-and-Docker.git"
    }

    stage('Build') {
        echo 'Building Docker Image...'
        sh 'docker build -t devops-app .'
    }

    stage('Run') {
        echo 'Running container...'

        sh '''
            docker stop devops-app-container || true
            docker rm devops-app-container || true
            docker run -d -p 5000:5000 --name devops-app-container devops-app
        '''
    }
}
📸 Pipeline Flow
GitHub Repo
     │
     ▼
   Jenkins
     │
     ├── Clone Stage
     ├── Build Stage
     └── Run Stage
     │
     ▼
Docker Container 🚀
👨‍💻 Author

Abdelaziz - DevOps Enthusiast
