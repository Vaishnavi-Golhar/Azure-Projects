# 📘 Assign Custom Role to a User - project

This project demonstrates how to **create a new user** in Azure and **assign** the previously created custom role (from Module 8: Assignment 1) to that user. The user will be granted permissions to **view**, **start**, and **stop** Virtual Machines (VMs) as per the custom role's configuration.

## 📝 Tasks Performed
1. **Created a new user** in Azure Active Directory.
2. **Assigned** the previously created custom role to the new user.
3. **Tested** the access of the user to ensure they can view, start, and stop VMs, but cannot perform other actions.

## 📂 Files Included
- [assign-custom-role-to-user.pdf](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/assign-custom-role-to-user/assign-custom-role-to-user.pdf) - Detailed document describing how to create a new user and assign the custom role.
- `create-user.sh` - Script for creating a new user in Azure Active Directory.
- `assign-role.sh` - Script to assign the custom role to the newly created user.
- `user-configuration-guide.pdf` - Guide on how to configure the user and verify their permissions.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating a user and assigning the custom role:
    ```bash
    # Create a new user in Azure Active Directory
    az ad user create --display-name "NewUser" --user-principal-name newuser@yourdomain.com --password "YourSecurePassword123" --force-change-password-next-sign-in true

    # Assign the custom role to the new user
    az role assignment create --assignee newuser@yourdomain.com --role "VM View, Start, Stop Role" --scope /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

