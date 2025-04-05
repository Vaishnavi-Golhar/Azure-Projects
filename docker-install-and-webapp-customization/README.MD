# 📘 Azure Project: Docker Install and WebApp Customization

This project demonstrates how to install Docker on an Azure VM, pull a Docker image from Docker Hub, and customize the application by creating a new file in the container.

---

## 📝 Tasks Performed

1. Created an Azure Virtual Machine.
2. Installed Docker on the VM.
3. Pulled the Docker image `hshar/webapp` from Docker Hub.
4. Created a new file inside the container to customize the application.

---

## 📂 Files Included

- 📄 [`docker-install-and-webapp-customization.pdf`](./docker-install-and-webapp-customization.pdf):  
  Contains screenshots and commands used for Docker installation, pulling the image, and editing the container.

---

## 💻 Commands Used

### Install Docker on VM (Ubuntu)
```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version
```

### Pull Docker Image and Run
```bash
docker pull hshar/webapp
docker run -d -p 80:80 hshar/webapp
```

### Customize WebApp (example command)
```bash
docker exec -it <container_id> /bin/bash
echo "Custom message" > /usr/share/nginx/html/custom.txt
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


