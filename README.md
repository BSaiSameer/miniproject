🚀 CI/CD Pipeline with GitHub Actions & Docker
📌 Project Overview

This project demonstrates a CI/CD pipeline that builds a Docker image, runs tests, and deploys locally using GitHub Actions, Docker, and Minikube/VM.
The pipeline automates the flow from code commit → build → test → deployment.

🛠️ Tools & Technologies

GitHub Actions – CI/CD automation

Docker – Containerization

Docker Hub – Image repository

Minikube / Local VM – Deployment

docker-compose – Local testing

📂 Project Structure
.
├── .github/
│   └── workflows/
│       └── ci-cd.yml     # GitHub Actions pipeline config
├── Dockerfile            # Docker image build instructions
├── docker-compose.yml    # Local container setup
├── k8s-deployment.yml    # Kubernetes deployment (Minikube/VM)
├── app/                  # Application source code
│   ├── main.py           # Example entry point
│   └── requirements.txt  # Dependencies
└── README.md             # Documentation

⚙️ CI/CD Workflow

Developer pushes code → GitHub repo

GitHub Actions runs pipeline

🛠️ Build Docker image

✅ Run tests

📦 Push image to Docker Hub

🚀 Deploy to Minikube / VM

Local Testing → Run with docker-compose up before deployment

▶️ How to Run
🔹 Local with Docker Compose
docker-compose up --build

🔹 Build & Run Docker Manually
docker build -t your-dockerhub-username/ci-cd-app .
docker run -p 5000:5000 your-dockerhub-username/ci-cd-app

🔹 Deploy to Minikube
kubectl apply -f k8s-deployment.yml
kubectl get pods
