# 🚀 Wexa-AI

Next.js app containerized with Docker, deployed via GitHub Actions and Minikube.

## 🧩 Features
- Containerized Next.js app
- CI/CD pipeline using GitHub Actions + GHCR
- Kubernetes deployment for Minikube

## 🐳 Run locally
```bash
npm install
npm run dev
```

## 🧱 Build Docker image
```bash
docker build -t wexa-ai:local .
docker run -p 3000:3000 wexa-ai:local
```

## ⚙️ GitHub Actions
Workflow builds & pushes image to:
```
ghcr.io/sivaprakash-tech/nextjs-wexa-ai:latest
```

## ☸️ Deploy to Minikube
```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
minikube service wexa-ai-service
```

## ✅ Access
http://<minikube-ip>:30080
