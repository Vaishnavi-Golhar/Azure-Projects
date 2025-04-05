# 📘 Azure Project: ACR, Docker, and VM App Service Deployment

This project demonstrates how to create an Azure Container Registry (ACR), connect it to Docker running on a Virtual Machine (VM), and upload a Docker image to ACR. It also showcases how to deploy the image using Azure App Service.

---

## 📝 Tasks Performed

1. Created an Azure Container Registry (ACR).
2. Connected Docker running on an Azure VM to the ACR.
3. Pushed a Docker image from the VM to the ACR.
4. Created an Azure App Service to deploy the Docker image.

---

## 📂 Files Included

- 📄 [`acr-docker-vm-appservice-deployment.pdf`](./acr-docker-vm-appservice-deployment.pdf):  
  Contains screenshots and commands used to complete the assignment.

---

## 💻 Commands Used

### Install Docker on VM (Ubuntu)
```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version

