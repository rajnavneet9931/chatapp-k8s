🚀 Full Stack Chat Application (Kubernetes + DevOps)

A real-time full-stack chat application deployed using Docker and Kubernetes (Kind), showcasing end-to-end DevOps practices including CI/CD, scaling, and secure configuration.

🧰 Tech Stack
Frontend: React + Nginx
Backend: Node.js + Express
Database: MongoDB
Containerization: Docker
Orchestration: Kubernetes (Kind)
CI/CD: Jenkins
Media Storage: Cloudinary
Web Server: NGINX
⚙️ Features
Real-time chat using Socket.IO
User authentication with JWT
Profile image upload (Cloudinary)
Dockerized microservices (frontend, backend, MongoDB)
Kubernetes deployments and services
Persistent storage using PV & PVC
Secrets management for sensitive data
Nginx reverse proxy with fixed CSP
Horizontal Pod Autoscaler (HPA)
Vertical Pod Autoscaler (VPA)
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
🔄 CI/CD Pipeline (Jenkins)

This project includes a Jenkins pipeline that:

Clones the repository
Builds and runs services using Docker Compose
Performs health checks using curl
Automates deployment process
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
PersistentVolume & PersistentVolumeClaim
Secrets
Kind cluster configuration
⚡ DevOps Highlights
Infrastructure as Code (Kubernetes YAML)
Containerized microservices architecture
CI/CD automation using Jenkins
Service discovery and networking
Secure secret management
Real production issue debugging
Scalable system with HPA & VPA
🚀 Future Improvements
Ingress Controller for domain routing
Monitoring (Prometheus + Grafana)
Centralized logging (ELK Stack)
Helm charts for packaging
📜 License

This project is licensed under the MIT License.

👨‍💻 Author

Navneet Chauhan
