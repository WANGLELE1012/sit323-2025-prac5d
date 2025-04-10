
# SIT323-2025-prac5d — Task 5.2D Documentation

## Project Overview

This project demonstrates the process of building a Docker image for a Node.js microservice, pushing it to Google Container Registry (GCR), and deploying it to Kubernetes using deployment and service configuration files.

---

## Tools Used
| Tool        | Purpose                                          |
|-------------|--------------------------------------------------|
| Git         | Version control                                  |
| VS Code     | Code editor                                      |
| Node.js     | Backend development                              |
| Docker      | Containerization                                 |
| Kubernetes  | Container orchestration platform                 |
| kubectl     | Kubernetes CLI for deployment and management     |
| Google Cloud SDK | Authentication and access to GCR            |

---

## Folder Structure
```
docker_web_app/
│
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── server.js
├── package.json
├── package-lock.json
└── node_modules/
```

---

## Google Cloud Container Registry (GCR) Setup Steps

### 1. Set Project
```bash
gcloud config set project lele-docker-push
```

### 2. Login to Google Cloud
```bash
gcloud auth login
```

### 3. Authenticate Docker with GCR
```bash
gcloud auth configure-docker
```

---

## Docker Image Operations

### 1. Build Docker Image
```bash
docker build -t gcr.io/lele-docker-push/node-web-app .
```

### 2. Push Docker Image to GCR
```bash
docker push gcr.io/lele-docker-push/node-web-app
```

---

## Kubernetes Deployment Steps

### 1. Deploy the Application
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 2. Check Pods
```bash
kubectl get pods
```

### 3. Check Services
```bash
kubectl get services
```

---

## GitHub Repository Operations

### 1. Initialize Git Repository
```bash
git init
git add .
git commit -m "prac5.2D complete"
```

### 2. Add Remote and Push
```bash
git remote remove origin
git remote add origin https://github.com/wangelele1012/sit323-2025-prac5d.git
git branch -M main
git push -u origin main
```

---

## GitHub Repository Link
> https://github.com/wangelele1012/sit323-2025-prac5d

---