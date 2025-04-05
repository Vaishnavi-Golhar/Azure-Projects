# 📘 Apache2 VM Load Balancer - Assignment 1

This project involves deploying two virtual machines (VMs) with Ubuntu and Apache2 installed. The task also includes configuring a load balancer to distribute traffic between these two VMs, ensuring high availability and efficient traffic distribution.

## 📝 Tasks Performed
1. Deployed **2 VMs** with **Ubuntu** and **Apache2** installed.
2. Customized the **index.html** files:
    - VM1: Displays "This is VM1".
    - VM2: Displays "This is VM2".
3. Created and configured an **Azure Load Balancer** to balance traffic between the two VMs.

## 📂 Files Included
- `apache2-vm-load-balancer.pdf` - Detailed steps on how to deploy the VMs, modify index.html, and configure the load balancer.
- `deploy-vms.sh` - Script to deploy two VMs with Apache2 installed.
- `load-balancer-config.json` - Configuration file for setting up the Azure Load Balancer.
- `index.html` - Modified index page for both VMs.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating VMs and configuring the load balancer:
    ```bash
    az vm create --resource-group yourResourceGroup --name VM1 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys
    az vm create --resource-group yourResourceGroup --name VM2 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys

    az vm open-port --resource-group yourResourceGroup --name VM1 --port 80
    az vm open-port --resource-group yourResourceGroup --name VM2 --port 80

    # Load Balancer Configuration
    az network lb rule create --resource-group yourResourceGroup --lb-name yourLoadBalancer --name LoadBalancerRule --protocol Tcp --frontend-port 80 --backend-port 80 --frontend-ip-name yourFrontendIP --backend-pool-name yourBackendPool
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

