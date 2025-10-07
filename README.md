1. Project Description

Briefly explain what the project is and its purpose.

# DevOps Assessment - Next.js App

A simple Next.js application containerized with Docker, automated with GitHub Actions, pushed to GitHub Container Registry (GHCR), and deployed on Minikube using Kubernetes manifests.

2. Steps to Run Locally

Good as-is, but you can add Node version requirement:

## Steps to Run Locally
Requires Node.js v18+ and npm.

```bash
npm install
npm run dev


Open http://localhost:3000
 in your browser.


---

### **3. Docker Build & Run**
You can mention Docker is required:

```markdown
## Docker Build & Run
Requires Docker installed.

```bash
docker build -t devops-assessment-app .
docker run -p 3000:3000 devops-assessment-app


Visit http://localhost:3000


---

### **4. GitHub Actions**
Add a note about what the workflow does:

```markdown
## GitHub Actions
- On push to `main` branch:
  - Builds Docker image
  - Pushes image to GHCR

5. Kubernetes Deployment (Minikube)

Include the imagePullSecrets info so GHCR image can be pulled:

## Kubernetes Deployment (Minikube)
```bash
minikube start
kubectl create secret docker-registry ghcr-secret \
  --docker-server=ghcr.io \
  --docker-username=teja1329 \
  --docker-password=<YOUR_TOKEN> \
  --docker-email=<YOUR_EMAIL>

kubectl apply -f k8s/
minikube service nextjs-service


---

### **6. GHCR Image & GitHub Repo**
Make it explicit:

```markdown
## GHCR Image
`ghcr.io/teja1329/devops-assessment-app:latest`

## GitHub Repo
[https://github.com/teja1329/devops-assessment-app](https://github.com/teja1329/devops-assessment-app)


If you want, I can write the full ready-to-paste README.md with all this included in one file. It’ll be professional and complete.

Do you want me to do that?

You said:
yes pls
ChatGPT said:

Here’s a complete, ready-to-paste README.md for your project:

# DevOps Assessment - Next.js App

A simple Next.js application containerized with Docker, automated with GitHub Actions, pushed to GitHub Container Registry (GHCR), and deployed on Minikube using Kubernetes manifests.

---

## Table of Contents
- [Project Description](#project-description)
- [Prerequisites](#prerequisites)
- [Steps to Run Locally](#steps-to-run-locally)
- [Docker Build & Run](#docker-build--run)
- [GitHub Actions](#github-actions)
- [Kubernetes Deployment (Minikube)](#kubernetes-deployment-minikube)
- [GHCR Image & GitHub Repo](#ghcr-image--github-repo)

---

## Project Description
This project demonstrates:
- Creating a Next.js app
- Containerizing it using Docker
- Automating Docker image build & push to GHCR with GitHub Actions
- Deploying the containerized app on Kubernetes (Minikube)

---

## Prerequisites
- Node.js v18+ and npm
- Docker
- Minikube
- kubectl
- GitHub account with GHCR access token

---

## Steps to Run Locally
```bash
npm install
npm run dev


Open http://localhost:3000
 in your browser.

Docker Build & Run
docker build -t devops-assessment-app .
docker run -p 3000:3000 devops-assessment-app


Visit http://localhost:3000
.

GitHub Actions

On push to main branch:

Builds Docker image

Pushes image to GHCR: ghcr.io/teja1329/devops-assessment-app:latest

Kubernetes Deployment (Minikube)

Start Minikube:

minikube start


Create GHCR secret for Kubernetes to pull image:

kubectl create secret docker-registry ghcr-secret \
  --docker-server=ghcr.io \
  --docker-username=teja1329 \
  --docker-password=<YOUR_GHCR_TOKEN> \
  --docker-email=<YOUR_EMAIL>


Apply Kubernetes manifests:

kubectl apply -f k8s/


Access the app via Minikube service:

minikube service nextjs-service

