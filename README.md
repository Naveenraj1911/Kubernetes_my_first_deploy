# Hello from Docker + Kubernetes 👋🐳☸️

This is a beginner-friendly project to **containerize a simple Flask web app using Docker**, and then **deploy it on Kubernetes (Minikube)**.  
Great for learning how Docker and Kubernetes work together!

---

## 🔧 Tech Stack

- **Python 3.9**
- **Flask (Web Framework)**
- **Docker** – to containerize the app
- **Kubernetes (Minikube)** – to orchestrate and run containers
- **kubectl** – Kubernetes CLI

---

## 📁 Project Structure
hello-k8s/
│
├── app.py # Flask app
├── requirements.txt # Python dependencies
├── Dockerfile # Docker build instructions
│
└── k8s/ # Kubernetes deployment configs
├── deployment.yaml
└── service.yaml

## How to run docker and kubernetes

1. Run App Locally with Docker

Step 1: Build Docker Image

docker build -t hello-k8s .

Step 2: Run Container

docker run -d -p 5000:5000 hello-k8s

Step 3: Access the App

http://localhost:5000

 Output:
   Hello from Docker + Kubernetes!

2. Deploy App with Kubernetes 

Step 1: Start Minikube

minikube start

Step 2: Use Minikube Docker Environment

eval $(minikube docker-env)

Step 3: Build the Docker Image (inside Minikube context)

docker build -t hello-k8s .

Step 4: Apply Kubernetes Configs

kubectl apply -f k8s/

Step 5: Access the App via Minikube Service

minikube service hello-service

This command will:

Expose the app on a localhost URL like http://127.0.0.1:42981

Automatically open it in your browser

Sample Output (Browser / curl)

Hello from Docker + Kubernetes!














