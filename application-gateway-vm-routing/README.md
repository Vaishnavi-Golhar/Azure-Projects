# 📘 Application Gateway with VM Routing - Module 7: Assignment 2

This project involves configuring an **Azure Application Gateway** to route traffic to two virtual machines (VMs) based on the URL path. The task requires setting up routing rules so that:
- `/vm1` directs to **VM1**.
- `/vm2` directs to **VM2**.

## 📝 Tasks Performed
1. Created an **Application Gateway** in Azure.
2. Configured routing rules to route traffic based on the path:
    - `/vm1` routes to **VM1**.
    - `/vm2` routes to **VM2**.
3. Deployed and configured **VM1** and **VM2** to serve content on specific paths.

## 📂 Files Included
- `application-gateway-vm-routing.pdf` - Detailed document outlining the setup and configuration of the Application Gateway and VMs.
- `app-gateway-config.json` - Configuration file for creating the Application Gateway with routing rules.
- `deploy-vms.sh` - Script to deploy the VMs.
- `vm1-index.html` - Custom index page for **VM1**.
- `vm2-index.html` - Custom index page for **VM2**.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating VMs and configuring the Application Gateway:
    ```bash
    # Create VM1
    az vm create --resource-group yourResourceGroup --name VM1 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys

    # Create VM2
    az vm create --resource-group yourResourceGroup --name VM2 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys

    # Create Application Gateway
    az network application-gateway create --name yourAppGateway --resource-group yourResourceGroup --location eastus --sku Standard_v2 --capacity 2 --frontend-port 80 --backend-pool-name yourBackendPool

    # Create routing rules for /vm1 and /vm2
    az network application-gateway url-path-map rule create --gateway-name yourAppGateway --resource-group yourResourceGroup --name Vm1Route --paths "/vm1" --address "http://VM1_IP"
    az network application-gateway url-path-map rule create --gateway-name yourAppGateway --resource-group yourResourceGroup --name Vm2Route --paths "/vm2" --address "http://VM2_IP"
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

