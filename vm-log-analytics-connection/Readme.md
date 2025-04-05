# 📘 VM Log Analytics Connection - Project

This project demonstrates how to **connect Log Analytics** to a previously deployed **VM** in Azure for monitoring and log management.

## 📝 Tasks Performed
1. **Used previously connected VMs**.
2. **Connected Log Analytics** workspace to the virtual machine for monitoring and log collection.

## 📂 Files Included
- [vm-log-analytics-connection.pdf](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/vm-log-analytics-connection/vm-log-analytics-connection.pdf) - Detailed document explaining how to connect Log Analytics to the VM.
- `connect-log-analytics.sh` - Script to connect the VM to Log Analytics workspace.
- `configure-vm-for-log-analytics.sh` - Script to configure the VM for integration with Log Analytics.
- `log-analytics-setup-guide.pdf` - Guide on how to set up Log Analytics and monitor the VM.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for configuring Log Analytics:
    ```bash
    # Create a Log Analytics workspace
    az monitor log-analytics workspace create --resource-group MyResourceGroup --workspace-name MyLogAnalyticsWorkspace --location eastus

    # Connect the VM to the Log Analytics workspace
    az vm extension set --resource-group MyResourceGroup --vm-name MyVM --name OmsAgentForLinux --publisher Microsoft.EnterpriseCloud --protected-settings '{"workspaceKey": "{workspace-key}"}' --settings '{"workspaceId": "{workspace-id}"}'
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

