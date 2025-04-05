# 📘 Azure Project: Create Resource Group using Azure PowerShell

This project demonstrates how to create a Resource Group in Microsoft Azure using **Azure PowerShell**.

---

## 📝 Tasks Performed

1. Connected to **Azure PowerShell** in Azure Cloud Shell or on a local machine.
2. Created a resource group named `rg-powershell` in the **South Central US** region.

---

## 📂 Files Included

- 📄 [`Resource-Group-AzurePowerShell.pdf`](https://github.com/Vaishnavi-Golhar/Azure-Projects/blob/main/Resource-Group-AzurePowerShell/Resource-Group-AzurePowerShell.pdf):  
  Contains screenshots and PowerShell commands used to complete the assignment.

---

## 💻 Azure PowerShell Command Used

```powershell
New-AzResourceGroup -Name rg-powershell -Location "South Central US"

