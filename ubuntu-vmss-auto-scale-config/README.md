# 📘 Azure Project: Ubuntu VM Scale Set with Auto-Scaling Configuration

This project demonstrates how to create a **Virtual Machine Scale Set (VMSS)** in Azure using **Ubuntu as the operating system**, with auto-scaling rules configured based on CPU usage.

---

## 📝 Tasks Performed

1. Created a **VM scale set** with **Ubuntu OS**
2. Set the **minimum number of VMs** to `1` and **maximum** to `5`
3. Configured **scale-out** rule:
   - CPU threshold: **75%**
   - Increase by: **1 VM**
4. Configured **scale-in** rule:
   - CPU threshold: **25%**
   - Decrease by: **1 VM**

---

## 📂 Files Included

- 📄 [`ubuntu-vmss-auto-scale-config.pdf`](./ubuntu-vmss-auto-scale-config.pdf):  
  Contains screenshots and steps followed to configure VMSS with auto-scaling rules.

---

## 💻 Azure Portal Configuration Summary

- **OS Image**: Ubuntu
- **Region**: West US
- **Scaling Rules**:
  - **Scale-out**: Triggered at 75% CPU usage, adds 1 VM
  - **Scale-in**: Triggered at 25% CPU usage, removes 1 VM

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


