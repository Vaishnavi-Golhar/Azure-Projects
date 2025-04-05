# 📘 Azure Project: Azure Resource Cleanup using Azure CLI & PowerShell

This project demonstrates how to delete all Resource Groups in the **West US** region using both **Azure CLI** and **Azure PowerShell**.

---

## 📝 Tasks Performed

1. Used **Azure CLI** and **Azure PowerShell** to:
   - Delete all resource groups located in the **West US** region using a single command

---

## 📂 Files Included

- 📄 [`azure-resource-cleanup.pdf`](./azure-resource-cleanup.pdf):  
  Contains screenshots and commands used for both Azure CLI and PowerShell.

---

## 💻 Azure CLI Command Used

```bash
az group list --query "[?location=='westus'].name" -o tsv | xargs -I {} az group delete --name {} --yes --no-wait
```

---

## 💻 Azure PowerShell Command Used

```powershell
Get-AzResourceGroup | Where-Object {$_.Location -eq "westus"} | ForEach-Object { Remove-AzResourceGroup -Name $_.ResourceGroupName -Force }
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


