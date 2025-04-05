# 📘 Apache2 VM DNS Configuration - Project

This project demonstrates the configuration of Apache2 on a virtual machine (VM) with a custom domain using Azure DNS. The assignment involves linking a free domain to the VM’s IP address, ensuring the domain resolves correctly to the Apache2 server hosted on Azure.

## 📝 Tasks Performed
1. Used an existing Apache2 VM from previous configurations.
2. Obtained a free domain name from **freenom.com**.
3. Configured **Azure DNS** to point the free domain to the VM’s public IP address.

## 📂 Files Included
- `apache2-vm-dns-configuration.pdf` - A detailed document describing the steps to configure the Apache2 VM and link it to the free domain.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for creating and managing the DNS zone:
    ```bash
    az network dns zone create --name yourdomain.com --resource-group yourResourceGroup
    az network dns record-set a add-record --zone-name yourdomain.com --resource-group yourResourceGroup --name www --ipv4-address your_vm_ip_address
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)

