# 📘 Azure Project: Move Storage Account Between Resource Groups

This project demonstrates how to create two resource groups and move a storage account between them using **Azure CLI** and **Azure PowerShell**.

---

## 📝 Tasks Performed

1. Created two resource groups: `rg-1` and `rg-2`
2. Added a **Storage Account** to `rg-1`
3. Moved the **Storage Account** from `rg-1` to `rg-2`

---

## 📂 Files Included

- 📄 [`move-storage-between-resource-groups.docx`](./move-storage-between-resource-groups.docx):  
  Contains screenshots and step-by-step CLI & PowerShell commands used to complete the assignment.

---

## 💻 Azure CLI Commands Used

```bash
az group create --name rg-1 --location "East US"
az group create --name rg-2 --location "East US"
az storage account create --name mystorageacct123 --resource-group rg-1 --location "East US" --sku Standard_LRS
az resource move --destination-group rg-2 --ids $(az storage account show --name mystorageacct123 --resource-group rg-1 --query id -o tsv)
```

---

## 💻 Azure PowerShell Commands Used

```powershell
New-AzResourceGroup -Name "rg-1" -Location "East US"
New-AzResourceGroup -Name "rg-2" -Location "East US"
New-AzStorageAccount -ResourceGroupName "rg-1" -Name "mystorageacct123" -Location "East US" -SkuName "Standard_LRS"
$resource = Get-AzResource -ResourceGroupName "rg-1" -ResourceName "mystorageacct123" -ResourceType "Microsoft.Storage/storageAccounts"
Move-AzResource -DestinationResourceGroupName "rg-2" -ResourceId $resource.ResourceId
```

---

👩‍💼 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


