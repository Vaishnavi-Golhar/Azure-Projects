# 📘 VM Deletion Alert -Project

This project demonstrates how to **create an alert** for the **deletion** of a **virtual machine (VM)** in Azure to monitor and notify when a VM is deleted.

## 📝 Tasks Performed
1. **Used the previously deployed VM**.
2. **Created an alert** for the deletion of the VM to track any accidental or unauthorized deletion events.

## 📂 Files Included
- [vm-deletion-alert.pdf](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/vm-deletion-alert/vm-deletion-alert.pdf) - Detailed document explaining how to create an alert for VM deletion in Azure.
- `create-alert.sh` - Script to create an alert for the deletion of the VM.
- `vm-deletion-alert-setup-guide.pdf` - A guide to help set up and configure the alert for VM deletion.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands to create a deletion alert:
    ```bash
    # Create an action group for alert notifications
    az monitor action-group create --resource-group MyResourceGroup --name MyActionGroup --short-name MyAG --email "example@example.com"

    # Create the alert for VM deletion
    az monitor alert rule create --resource-group MyResourceGroup --name "VMDeletionAlert" --scopes "/subscriptions/{subscription-id}/resourceGroups/{resource-group}/providers/Microsoft.Compute/virtualMachines/{vm-name}" --condition "SignalName == 'Delete'" --action "ActionGroup" --action-group "/subscriptions/{subscription-id}/resourceGroups/{resource-group}/providers/Microsoft.Insights/actionGroups/MyActionGroup"
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

