
# 🎓 DevOps Graduation Project

<p align="center">
  <img src="static/logos/nti-logo.png" height="80" />
  &nbsp;&nbsp;&nbsp;
  <img src="static/logos/ivolve-logo.png" height="80" />
</p>

<h3 align="center">Final Project for NTI DevOps Program</h3>

<p align="center">
  A complete DevOps workflow demonstrating containerization, orchestration, infrastructure provisioning, configuration management, CI/CD automation, and GitOps-driven deployment—all tied together from code to cloud.
</p>

---

## 🔗 Repository

**GitHub:** https://github.com/onkarlonkar9/iVolveGraduation-Project.git

---

## 🧠 Project Summary

This project shows an end-to-end DevOps pipeline for a Python web app, including:

- **Docker** containerization  
- **Docker Compose** for local orchestration  
- **Kubernetes** deployment (Minikube)  
- **Terraform** provisioning (AWS infrastructure)  
- **Ansible** configuration management  
- **Jenkins** based CI  
- **ArgoCD** for GitOps CD

---

## 🐳 Docker & Docker Compose

The web app is containerized with a multi-stage Dockerfile and configured for local development using Docker Compose.

**Run locally:**
```bash
docker-compose up --build
```
Visit: http://localhost:5000

☸️ Kubernetes Deployment (Minikube)
Build and deploy
```bash
minikube start
eval $(minikube docker-env)
docker build -t ivolve-app:latest .
kubectl apply -f k8s/namespace.yaml
kubectl apply -f k8s/ -n ivolve
```
minikube service ivolve-service -n ivolve
✔ Uses custom namespace
✔ Local image deployment without remote registry

☁️ Infrastructure with Terraform (AWS)
Terraform code provisions:

VPC with public subnet

EC2 instance for Jenkins

Security groups

S3 Terraform backend

CloudWatch monitoring

Deploy:

```bash
terraform init
terraform plan
terraform apply
```
⚙️ Configuration Management (Ansible)
Ansible playbooks install and configure:

Git

Docker

Jenkins

Required tools and packages

Run playbook:

```bash
ansible-playbook -i inventory/static_hosts.ini site.yml
```
Idempotent, role-based, and supports dynamic inventory.

🔄 CI with Jenkins
Jenkins pipeline:

Checks out code

Builds Docker images

Validates artifacts

Prepares them for deployment

Pipeline scripts are included in the repository for automated testing and artifact management.

🚀 CD with ArgoCD (GitOps)
ArgoCD continuously monitors the Git repo for Kubernetes manifests.

Deploy ArgoCD App:

```bash
kubectl apply -f argocd/app-argocd.yaml
```
Benefits:

✔ Automated sync to cluster
✔ Rollback via Git history
✔ Built-in health checks

🛠️ Technologies Used
Docker & Docker Compose

Kubernetes (Minikube)

Terraform

Ansible

Jenkins

ArgoCD

AWS (EC2, VPC, S3, CloudWatch)

📌 How to Run (Quick Start)
Clone repo

Start Docker services

Deploy app via Kubernetes

Provision infra with Terraform

Configure servers with Ansible

Trigger CI with Jenkins

Enable automatic sync via ArgoCD

📄 License
This project is MIT-licensed.

⭐ If this helped your portfolio or interview prep, give it a star!

yaml


---

### Next steps (brutal but honest)
1. **Add badges** (build status, license, coverage) — visuals matter.
2. **Write a Jenkinsfile** with clear stages.
3. **Document CI/CD flow** with sequence diagrams.
4. **Add architecture diagram** (PNG/SVG).

Tell me which piece you want next and I’ll craft it.
::contentReference[oaicite:0]{index=0}






