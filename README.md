# DevOps Assessment - Next.js App

## Steps to Run Locally
```bash
npm install
npm run dev
```

## Docker Build & Run
```bash
docker build -t devops-assessment-app .
docker run -p 3000:3000 devops-assessment-app
```

## GitHub Actions
- Builds Docker image on push to `main`
- Pushes image to GHCR: `ghcr.io/teja1329/devops-assessment-app:latest`

## Kubernetes Deployment (Minikube)
```bash
minikube start
kubectl apply -f k8s/
minikube service nextjs-service
```

Access the app via Minikube service URL.
