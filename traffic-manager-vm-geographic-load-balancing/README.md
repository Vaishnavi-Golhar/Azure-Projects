# 📘 Traffic Manager with VM Geographic Load Balancing - project

This project demonstrates how to deploy two virtual machines (VMs) in different regions in Azure and configure **Azure Traffic Manager** to balance the traffic geographically. The goal is to ensure that traffic is routed to the closest VM based on the user's geographical location.

## 📝 Tasks Performed
1. Deployed **2 VMs** in **different Azure regions**.
2. Configured **Azure Traffic Manager** for **geographical load balancing**.
3. Set up routing policies to direct traffic to the nearest VM based on the user's region.

## 📂 Files Included
- `traffic-manager-vm-geographic-load-balancing.pdf` - Detailed document describing how to deploy the VMs, configure Traffic Manager, and test geographical load balancing.
- `traffic-manager-config.json` - Configuration file for setting up **Azure Traffic Manager**.
- `deploy-vms.sh` - Script for deploying VMs in different regions.
- `vm1-region1-config.pdf` - Configuration details for **VM1** in **Region 1**.
- `vm2-region2-config.pdf` - Configuration details for **VM2** in **Region 2**.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating VMs and configuring **Azure Traffic Manager**:
    ```bash
    # Create VM in Region 1
    az vm create --resource-group yourResourceGroup --name VM1 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys --location eastus

    # Create VM in Region 2
    az vm create --resource-group yourResourceGroup --name VM2 --image UbuntuLTS --admin-username azureuser --generate-ssh-keys --location westus

    # Create Traffic Manager Profile for Geographic Routing
    az network traffic-manager profile create --name yourTrafficManagerProfile --resource-group yourResourceGroup --routing-method Geographic --unique-dns-name yourdnsname

    # Create Traffic Manager Endpoint for VM1
    az network traffic-manager endpoint create --profile-name yourTrafficManagerProfile --resource-group yourResourceGroup --name VM1Endpoint --type azureEndpoints --target-resource-id /subscriptions/{subscriptionId}/resourceGroups/yourResourceGroup/providers/Microsoft.Compute/virtualMachines/VM1 --endpoint-location "East US"

    # Create Traffic Manager Endpoint for VM2
    az network traffic-manager endpoint create --profile-name yourTrafficManagerProfile --resource-group yourResourceGroup --name VM2Endpoint --type azureEndpoints --target-resource-id /subscriptions/{subscriptionId}/resourceGroups/yourResourceGroup/providers/Microsoft.Compute/virtualMachines/VM2 --endpoint-location "West US"
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

