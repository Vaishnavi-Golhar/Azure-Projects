# 📘 VM Without Public IP Address with Bastion Host - Project

This project demonstrates how to create a **virtual machine (VM)** without a public IP address and connect to it using an **Azure Bastion Host**. The goal is to ensure secure, private access to a VM that doesn't have a direct public-facing IP.

## 📝 Tasks Performed
1. Created a **VM** without assigning it a public IP address.
2. Configured an **Azure Bastion Host** to securely connect to the VM without exposing it to the public internet.
3. Established secure access to the VM using the Bastion Host.

## 📂 Files Included
- `vm-without-public-ip-bastion.pdf` - Detailed document describing the process of creating the VM and setting up the Bastion Host.
- `deploy-vm-without-public-ip.sh` - Script to deploy a VM without a public IP.
- `bastion-host-setup.sh` - Script for setting up an **Azure Bastion Host** for secure VM access.
- `vm-configuration-guide.pdf` - Guide on how to configure the VM and access it through Bastion.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for deploying the VM and setting up the Bastion Host:
    ```bash
    # Create VM without public IP
    az vm create --resource-group yourResourceGroup --name YourVMName --image UbuntuLTS --admin-username azureuser --generate-ssh-keys --no-wait

    # Create Virtual Network and Subnet for Bastion
    az network vnet create --resource-group yourResourceGroup --name yourVNet --subnet-name AzureBastionSubnet

    # Create Bastion Host
    az network bastion create --resource-group yourResourceGroup --name YourBastionHost --vnet-name yourVNet --subnet AzureBastionSubnet --public-ip-address YourBastionPublicIP

    # Connect to the VM using Bastion
    az network bastion ssh --resource-group yourResourceGroup --name YourBastionHost --target-resource-id /subscriptions/{subscriptionId}/resourceGroups/yourResourceGroup/providers/Microsoft.Compute/virtualMachines/YourVMName --auth-type ssh --username azureuser
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

