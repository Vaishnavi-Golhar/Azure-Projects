# 📘 Linux VM with Apache2 and Backup - Project

This project demonstrates how to **create a Linux VM**, install **Apache2** on it, create a **Recovery Services vault**, and take a **backup** of the deployed VM using Azure's backup services.

## 📝 Tasks Performed
1. **Created a Linux Virtual Machine** on Azure.
2. **Installed Apache2** web server on the Linux VM.
3. **Created a Recovery Services vault** to store the backup.
4. **Took a backup** of the deployed Linux VM using Azure Recovery Services.

## 📂 Files Included
- [linux-vm-apache2-backup.pdf](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/linux-vm-apache2-backup/linux-vm-apache2-backup.pdf) - Detailed document describing how to create a Linux VM, install Apache2, create the Recovery Services vault, and back up the VM.
- `create-linux-vm.sh` - Script to create a Linux VM on Azure.
- `install-apache2.sh` - Script to install Apache2 web server on the Linux VM.
- `create-recovery-vault.sh` - Script to create a Recovery Services vault.
- `backup-vm-guide.pdf` - Guide on how to back up the VM and manage backups using Azure Recovery Services.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating the VM, installing Apache2, and taking backups:
    ```bash
    # Create a Linux VM in Azure
    az vm create --resource-group MyResourceGroup --name MyLinuxVM --image UbuntuLTS --admin-username azureuser --generate-ssh-keys

    # Install Apache2 on the Linux VM
    az vm run-command invoke --resource-group MyResourceGroup --name MyLinuxVM --command-id RunShellScript --scripts "sudo apt-get update && sudo apt-get install apache2 -y"

    # Create a Recovery Services vault
    az backup vault create --resource-group MyResourceGroup --vault-name MyRecoveryVault --location eastus

    # Take a backup of the VM
    az backup protection enable-for-vm --resource-group MyResourceGroup --vault-name MyRecoveryVault --vm MyLinuxVM --policy-name DefaultPolicy
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

