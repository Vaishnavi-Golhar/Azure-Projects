# 📘 Azure Project: List Resources Using Tags

This project demonstrates how to create multiple Azure Storage Accounts with team-specific tags and how to filter resources based on those tags using **Azure CLI** or **PowerShell**.

---

## 📝 Tasks Performed

1. Created 3 storage accounts tagged with teams: `team1`, `team2`, and `team3`
2. Created an additional storage account for `team2`
3. Listed all resources associated with `team2` using the `Team` tag

---

## 📂 Files Included

- 📄 [`list-resources-using-tags.docx`](./list-resources-using-tags.docx):  
  Contains screenshots and commands demonstrating tagging and listing resources.

---

## 💻 Azure CLI Commands Used

```bash
# Create storage accounts with tags
az storage account create --name team1storage --resource-group rg-tag --location "East US" --sku Standard_LRS --tags Team=team1
az storage account create --name team2storage --resource-group rg-tag --location "East US" --sku Standard_LRS --tags Team=team2
az storage account create --name team3storage --resource-group rg-tag --location "East US" --sku Standard_LRS --tags Team=team3

# Create additional storage account for team2
az storage account create --name team2storageextra --resource-group rg-tag --location "East US" --sku Standard_LRS --tags Team=team2

# List resources with tag Team=team2
az resource list --tag Team=team2
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)
