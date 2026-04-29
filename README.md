🚀 Full Stack Chat Application (Kubernetes + DevOps)

A real-time full-stack chat application deployed using Docker and Kubernetes (Kind), showcasing production-level DevOps practices including CI/CD, autoscaling, and secure configuration.

🧰 Tech Stack
Frontend: React + Nginx
Backend: Node.js + Express
Database: MongoDB
Containerization: Docker
Orchestration: Kubernetes (Kind)
CI/CD: Jenkins
Media Storage: Cloudinary
Web Server / Ingress: NGINX
⚙️ Features
Real-time chat using Socket.IO
User authentication with JWT
Profile image upload (Cloudinary)
Dockerized microservices (frontend, backend, MongoDB)
Kubernetes deployments and services
Persistent storage using PV & PVC
Secrets management for sensitive data
Nginx reverse proxy with fixed CSP
Ingress for routing and single entry point
Horizontal Pod Autoscaler (HPA) for frontend & backend
Vertical Pod Autoscaler (VPA) for MongoDB
CI/CD pipeline using Jenkins
Real-world debugging & troubleshooting
🐳 Docker Setup
Build Images
docker build -t chatapp-backend ./backend
docker build -t chatapp-frontend ./frontend
Run with Docker Compose
docker-compose up -d --build
Access
Frontend → http://localhost:3000  
Backend → http://localhost:5001  
MongoDB → localhost:27017  
☸️ Kubernetes Setup (Kind)
Create Cluster
kind create cluster --config kind-config.yaml
Deploy Application
kubectl apply -f k8s/
Access Application
http://localhost:8081
🌐 Ingress
Single entry point for application
Routes traffic to frontend (which proxies backend APIs)
Production-style routing setup
🔄 CI/CD Pipeline (Jenkins)

Pipeline performs:

Code checkout from GitHub
Build & run using Docker Compose
Health checks using curl
Automated deployment
📈 Autoscaling
HPA (Horizontal Pod Autoscaler)
Backend → auto scales based on CPU
Frontend → auto scales based on CPU
VPA (Vertical Pod Autoscaler)
MongoDB → auto adjusts CPU & memory
🔐 Environment Variables

Backend requires:

MONGODB_URI
PORT
NODE_ENV
JWT_SECRET
CLOUDINARY_CLOUD_NAME
CLOUDINARY_API_KEY
CLOUDINARY_API_SECRET
📦 Kubernetes Components
Deployments (Frontend, Backend, MongoDB)
Services (ClusterIP / NodePort)
Ingress
PersistentVolume & PersistentVolumeClaim
Secrets
Kind cluster configuration
⚡ DevOps Highlights
Infrastructure as Code (Kubernetes YAML)
Containerized microservices architecture
CI/CD automation using Jenkins
Ingress-based routing
Autoscaling with HPA & VPA
Secure secret management
Real production debugging scenarios
🚀 Future Improvements
Monitoring (Prometheus + Grafana)
Centralized logging (ELK / Loki)
Helm charts
GitHub Actions pipeline
📜 License

This project is licensed under the MIT License.

👨‍💻 Author

Navneet Chauhan
