# CI/CD Kubernetes Deployment Project

## Overview

This project demonstrates a complete DevOps workflow using GitHub, Jenkins, Docker, Docker Hub, and Kubernetes.

A Flask application is containerized using Docker, pushed to Docker Hub, and deployed on a Kubernetes cluster using Minikube.

## Technologies Used

* Linux
* Git & GitHub
* Docker
* Docker Hub
* Jenkins
* Kubernetes (Minikube)
* Flask (Python)

## Project Architecture

GitHub → Jenkins → Docker Build → Docker Hub → Kubernetes Deployment

## Features

* Flask web application
* Docker containerization
* Docker Hub image repository
* Kubernetes Deployment
* Kubernetes Service exposure
* Jenkins CI/CD pipeline
* Minikube cluster deployment

## Docker Build

```bash
docker build -t gangadharbv/cicd-k8s:v1 .
docker push gangadharbv/cicd-k8s:v1
```

## Kubernetes Deployment

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

## Verify Deployment

```bash
kubectl get pods
kubectl get svc
```

## Application Output

```text
CI/CD Kubernetes Project Running!
```

## Author

Gangadhar BV
