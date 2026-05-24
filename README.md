# CodeAlpha_CICD_Azure
CodeAlpha DevOps Task 1

# CodeAlpha DevOps Internship - Task 4

# PakMilk Containerized Deployment Workflow

This repository hosts the automation, configuration scripts, and local deployment artifacts for the **PakMilk** platform. 

# Core DevOps Stack
 **WSL 2 (Ubuntu 26.04 LTS):** Provided an isolated, lightweight native Linux environment on Windows to run production containers.
 **Docker Engine:** Utilized for container runtime execution and managing layered application builds.
 **Nginx:** Configured as the high-performance internal web server to deliver frontend static assets smoothly.
 **GitHub Actions:** Integrated for automated CI/CD builds, tracking main branch updates, and distributing images to Docker Hub (`hmadrana/pakmilk`).

---

### 📋 Architectural Workflow & Verification

1. **Continuous Integration (Task 1):** Code changes automatically trigger an Azure-ready GitHub Actions workflow that builds the Docker image and pushes it to Docker Hub.
2. **Environment Provisioning (Task 4):** Initialized a fresh Ubuntu WSL 2 kernel instance and set up the stable Docker daemon.
3. **Local Deployment:** Ran the production container mapping host traffic to the internal Nginx engine:
   ```bash
   sudo docker run -d -p 8080:80 --name pakmilk_server hmadrana/pakmilk
# Live Deployment Proof
The containerized application is running live and serving traffic successfully at:
 http://localhost:8080
