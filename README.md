This project contains a Dockerized Node.js app deployed to a local Kubernetes cluster.

## Features
- Dockerfile for building Node.js app
- Kubernetes Deployment and Service (YAML)
- kubectl usage examples

## To run:
1. Build image: docker build -t node-web-app .
2. Apply Kubernetes files:
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml
3. View pod & service:
   kubectl get pods
   kubectl get services