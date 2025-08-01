# voting app
# 🗳️ Voting App (Kubernetes Microservices Demo)

This is a sample microservices-based voting application. It consists of multiple components, each running in its own Docker container and orchestrated with Kubernetes.

---

## 🧩 Architecture Overview

             [ VOTE WEB UI ]
                    |
         +----------+----------+
         |                     |
     [ Redis ]           [ Worker ]
         |                     |
     [ DB (Postgres) ]   [ Result Web UI ]

---

## 🚀 Features

- Frontend voting app (Python Flask)
- Result viewer (Node.js)
- Redis for vote queuing
- PostgreSQL for storing results
- Background worker to process votes
- Kubernetes deployment manifests
- Services exposed via NodePort

---

## 🛠️ Tech Stack

- Python Flask (Vote UI)
- Node.js + Express (Result UI)
- Redis (In-memory queue)
- PostgreSQL (Data store)
- Docker (Containerization)
- Kubernetes (Orchestration)

---

## 📦 Directory Structure

voting_app/
├── vote/               # Frontend voting app
├── result/             # Result viewing app
├── worker/             # Background vote processor
├── redis-pod.yaml      # Redis pod manifest
├── db-pod.yaml         # Postgres pod manifest
├── *.deployment.yaml   # Deployment manifests
├── *.service.yaml      # Service manifests
└── README.md

---

## 🏗️ Deployment Instructions

1. Clone the repository

   git clone https://github.com/YOUR_USERNAME/voting_app.git
   cd voting_app

2. Start Minikube

   minikube start

3. Apply Kubernetes manifests

   kubectl apply -f .

4. Access the application

   kubectl get svc

   Open in your browser:
   http://localhost:<NodePort>

---

## 🐳 Docker Images Used

- dockersamples/examplevotingapp_vote
- dockersamples/examplevotingapp_result
- dockersamples/examplevotingapp_worker
- postgres:12
- redis:alpine

---

## 🙌 Credits

Inspired by the original Docker Voting App: https://github.com/dockersamples/example-voting-app

---

## 📄 License

MIT License
