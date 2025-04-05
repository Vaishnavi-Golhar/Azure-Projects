# 📘 Azure Project: Create Multiple Resource Groups using Azure CLI & PowerShell

This project demonstrates how to create multiple Resource Groups in Microsoft Azure using **Azure CLI** and **Azure PowerShell** in the **West US** region.

---

## 📝 Tasks Performed

1. Used **Azure CLI** and **Azure PowerShell** to:
   - Create three resource groups in the **West US** region
   - List all resource groups in the **West US** region

---

## 📂 Files Included

- 📄 [`Create-Multiple-ResourceGroups-AzureCLI-PowerShell.pdf`](./Create-Multiple-ResourceGroups-AzureCLI-PowerShell.pdf):  
  Contains screenshots and commands used for both Azure CLI and PowerShell.

---

## 💻 Azure CLI Commands Used

```bash
az group create --name rg-cli-one --location "West US"
az group create --name rg-cli-two --location "West US"
az group create --name rg-cli-three --location "West US"
az group list --query "[?location=='westus']"
```

---

## 💻 Azure PowerShell Commands Used

```powershell
New-AzResourceGroup -Name "rg-ps-one" -Location "West US"
New-AzResourceGroup -Name "rg-ps-two" -Location "West US"
New-AzResourceGroup -Name "rg-ps-three" -Location "West US"
Get-AzResourceGroup | Where-Object {$_.Location -eq "westus"}
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


