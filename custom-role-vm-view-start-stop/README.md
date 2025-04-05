# 📘 Custom Role for Viewing, Starting, and Stopping VMs Project

This project demonstrates how to create a **custom role** in Azure that allows users to **view**, **start**, and **stop** Virtual Machines (VMs), but restricts them from performing any other actions.

## 📝 Tasks Performed
1. Created a **custom role** in Azure with permissions to view, start, and stop VMs.
2. Ensured that the role cannot perform any other actions such as creating, deleting, or modifying VMs.
3. Assigned the custom role to a user or group to test its functionality.

## 📂 Files Included
- `custom-role-vm-view-start-stop.pdf` - Detailed document describing the steps to create the custom role and assign it to a user.
- `create-custom-role.sh` - Script to create the custom role in Azure using **Azure CLI**.
- `custom-role-definition.json` - JSON file containing the custom role definition with the required permissions.
- `role-configuration-guide.pdf` - Guide on configuring and assigning the custom role to a user or group.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands to create the custom role:
    ```bash
    # Create a custom role definition
    az role definition create --role-definition ./custom-role-definition.json

    # Assign the custom role to a user or group
    az role assignment create --assignee <user-email> --role "VM View, Start, Stop Role" --scope /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}

    # Custom role definition (custom-role-definition.json):
    # {
    #   "Name": "VM View, Start, Stop Role",
    #   "Description": "Can view, start, and stop VMs but cannot modify or delete them",
    #   "Actions": [
    #     "Microsoft.Compute/virtualMachines/read",
    #     "Microsoft.Compute/virtualMachines/start/action",
    #     "Microsoft.Compute/virtualMachines/deallocate/action"
    #   ],
    #   "NotActions": [
    #     "Microsoft.Compute/virtualMachines/delete",
    #     "Microsoft.Compute/virtualMachines/write"
    #   ],
    #   "AssignableScopes": ["/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}"]
    # }
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)
