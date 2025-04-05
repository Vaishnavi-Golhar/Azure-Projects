# 📘 Azure Project: Mount Azure File Share on Windows & Linux

This project demonstrates how to create an **Azure File Share** in a Storage Account and mount it on both **Windows** and **Linux** systems.

---

## 📝 Tasks Performed

1. Created a file share in Azure Storage
2. Mounted the file share on:
   - A Windows machine
   - A Linux machine

---

## 📂 Files Included

- 📄 [`mount-azure-file-share.docx`](./mount-azure-file-share.docx):  
  Contains screenshots and detailed steps to create and mount the Azure file share.

---

## 💻 Azure CLI & Mount Commands Used

### Windows PowerShell (Mount):
```powershell
# Example mount command for Windows (modify with actual credentials)
net use Z: \\<storage-account-name>.file.core.windows.net\<file-share-name> <storage-key> /user:Azure\<storage-account-name>
```

### Linux (Mount):
```bash
# Example mount command for Linux (modify with actual credentials)
sudo mount -t cifs //<storage-account-name>.file.core.windows.net/<file-share-name> /mnt/<mount-dir> -o vers=3.0,username=<storage-account-name>,password=<storage-key>,dir_mode=0777,file_mode=0777,serverino
```

---

👩‍💻 Author  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


