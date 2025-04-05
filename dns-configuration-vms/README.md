
# 📘 DNS Configuration for VMs Project

This project demonstrates how to configure **DNS** for the public IP addresses of two previously deployed virtual machines (VMs). The objective is to assign DNS names to the public IPs of the VMs for easier access.

## 📝 Tasks Performed
1. Configured **DNS** for the public IP addresses of two deployed VMs.
2. Assigned DNS names to the public IPs, making them easier to remember and access.

## 📂 Files Included
- `dns-configuration-vms.pdf` - Detailed document describing the steps for configuring DNS for the VMs' public IPs.
- `dns-config.sh` - Script to configure DNS for the public IPs of the VMs.
- `vm1-public-ip.txt` - Contains the public IP address for **VM1**.
- `vm2-public-ip.txt` - Contains the public IP address for **VM2**.

## 💻 Commands Used (CLI/PowerShell)
- **Azure CLI** commands for configuring DNS:
    ```bash
    # Create a DNS zone
    az network dns zone create --name yourdomain.com --resource-group yourResourceGroup

    # Create A record for VM1
    az network dns record-set a add-record --zone-name yourdomain.com --resource-group yourResourceGroup --name vm1 --ipv4-address your_vm1_public_ip

    # Create A record for VM2
    az network dns record-set a add-record --zone-name yourdomain.com --resource-group yourResourceGroup --name vm2 --ipv4-address your_vm2_public_ip
    ```

## 👩‍💻 Author
- **Name**: Vaishnavi Golhar  
- **Email**: vaishnavi.golhar@example.com  
- **LinkedIn**: [https://www.linkedin.com/in/vaishnavigolhar/](https://www.linkedin.com/in/vaishnavigolhar/)
