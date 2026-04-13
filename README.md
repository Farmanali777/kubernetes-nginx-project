# 🚀 Kubernetes Nginx Deployment Project

## 📌 Project Overview

This project demonstrates how to deploy an Nginx application using Kubernetes with:

* Pod
* Service (NodePort)
* Deployment (recommended approach)

Built and tested using **KIND (Kubernetes in Docker)** on AWS EC2.

---

## 🧱 Architecture

* Kubernetes Cluster (KIND)
* Nginx Deployment (2 replicas)
* NodePort Service (external access)

---

## 📁 Project Structure

```
kubernetes-nginx-project/
│
├── pod.yml
├── pod-service.yml
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Apply Pod

```
kubectl apply -f pod.yml
```

### 2️⃣ Apply Service

```
kubectl apply -f pod-service.yml
```

---

## 🌐 Access Application

### Option 1 (Recommended for KIND)

```
kubectl port-forward --address 0.0.0.0 svc/nginx-service 8080:80
```

Then open:

```
http://<EC2-PUBLIC-IP>:8080
```

---

## ⚠️ Important Notes

* NodePort may not work directly in KIND without port mapping
* Port-forward is used for external access
* Deployment is recommended over standalone Pod

---

## 💡 Key Learnings

* Kubernetes Pod vs Deployment
* Service (NodePort) usage
* Port-forwarding in KIND
* AWS EC2 networking basics

---

## 🚀 Future Improvements

* Add Ingress Controller
* Use custom domain (nginx.local)
* Deploy on EKS (AWS Kubernetes)

---

## 👨‍💻 Author

**Farman Ali**
Aspiring DevOps Engineer | AWS | Kubernetes | Docker

