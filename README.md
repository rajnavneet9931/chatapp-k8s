🚀 Full Stack Chat Application (Kubernetes + DevOps)
A real-time full-stack chat application deployed using Docker and Kubernetes (Kind), demonstrating production-like DevOps practices.

🧰 Tech Stack


Frontend: React + Nginx


Backend: Node.js + Express


Database: MongoDB


Containerization: Docker


Orchestration: Kubernetes (Kind)


Media Storage: Cloudinary


Web Server: NGINX



⚙️ Features


Real-time chat using Socket.IO


User authentication with JWT


Profile image upload (Cloudinary)


Dockerized services (frontend, backend, MongoDB)


Kubernetes deployments and services


Persistent storage using PV & PVC


Secrets management for sensitive data


Nginx reverse proxy


Fixed CSP for external image loading


Horizontal Pod Autoscaler (HPA)


Vertical Pod Autoscaler (VPA)


Debugged real-world issues (CrashLoopBackOff, CSP, env errors, Mongo auth)



🐳 Docker Setup
Build Images
docker build -t chatapp-backend ./backenddocker build -t chatapp-frontend ./frontend
Run with Docker Compose
docker-compose up --build
Access
Frontend → http://localhost:3000  Backend → http://localhost:5001  MongoDB → localhost:27017  

☸️ Kubernetes Setup (Kind)
Create Cluster
kind create cluster --config kind-config.yaml
Deploy Application
kubectl apply -f k8s/
Access Application
http://localhost:8081

🔐 Environment Variables
Backend requires:
MONGODB_URIPORTNODE_ENVJWT_SECRETCLOUDINARY_CLOUD_NAMECLOUDINARY_API_KEYCLOUDINARY_API_SECRET

📦 Kubernetes Components


Deployments (Frontend, Backend, MongoDB)


Services (ClusterIP / NodePort)


PersistentVolume & PersistentVolumeClaim


Secrets


Kind cluster config



⚡ DevOps Highlights


Infrastructure as Code (YAML)


Containerized microservices


Service discovery and networking


Secure secret handling


Real production debugging scenarios


Scalable architecture with HPA & VPA



🚀 Future Improvements


Ingress Controller


CI/CD (GitHub Actions / Jenkins)


Monitoring (Prometheus + Grafana)


Logging (ELK Stack)



📜 License
This project is licensed under the MIT License.

👨‍💻 Author
Navneet Chauhan
