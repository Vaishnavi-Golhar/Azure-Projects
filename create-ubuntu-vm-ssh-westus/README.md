# 📘 Azure Project: Create Ubuntu VM with SSH in West US

This project demonstrates how to create a **Linux VM (Ubuntu)** in Microsoft Azure, open the SSH port, and connect to the VM using the terminal.

---

## 📝 Tasks Performed

1. Created a **Virtual Machine** in the **West US** region
2. Selected the **Ubuntu** image
3. Opened **SSH port (22)**
4. Connected to the **Linux VM** using terminal via SSH

---

## 📂 Files Included

- 📄 [`create-ubuntu-vm-ssh-westus.pdf`](./create-ubuntu-vm-ssh-westus.pdf):  
  Contains screenshots and commands used during the assignment.

---

## 💻 Azure CLI Command Used

```bash
az vm create \
  --resource-group <YourResourceGroupName> \
  --name <YourVMName> \
  --image UbuntuLTS \
  --admin-username <YourUsername> \
  --generate-ssh-keys \
  --location "West US"

az vm open-port \
  --port 22 \
  --resource-group <YourResourceGroupName> \
  --name <YourVMName>
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


