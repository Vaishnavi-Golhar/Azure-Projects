# 📘 Assign Role to User Group Project

This project demonstrates how to **create a user group** in Azure, **attach the custom role** (created in Module 8: Assignment 1) to the group, and **add users** to the group to verify whether the permissions are correctly assigned.

## 📝 Tasks Performed
1. **Created a user group** in Azure Active Directory.
2. **Assigned** the custom role (created in Assignment 1) to the user group.
3. **Added users** to the group and validated whether the permissions for viewing, starting, and stopping VMs are applied to the users.

## 📂 Files Included
- [assign-role-to-user-group.pdf](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/assign-role-to-user-group/assign-role-to-user-group.pdf) - Detailed document describing how to create the user group, assign the role, and add users.
- `create-user-group.sh` - Script to create a user group in Azure Active Directory.
- `assign-role-to-group.sh` - Script to assign the custom role to the newly created user group.
- `add-users-to-group.sh` - Script to add users to the group and check if the role is assigned correctly.
- `group-configuration-guide.pdf` - Guide on how to configure the user group and verify the permissions.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating the user group, assigning the role, and adding users:
    ```bash
    # Create a new user group in Azure Active Directory
    az ad group create --display-name "VM-Role-Group" --mail-nickname "VMRoleGroup"

    # Assign the custom role to the user group
    az role assignment create --assignee "VM-Role-Group" --role "VM View, Start, Stop Role" --scope /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}

    # Add a new user to the group
    az ad group member add --group "VM-Role-Group" --member-id {user-object-id}
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

