# 📘 Azure Project: Copy Blob using AzCopy

This project demonstrates how to use the **AzCopy** utility to transfer data between two Azure Storage Account containers.

---

## 📝 Tasks Performed

1. Used existing storage accounts from a previous assignment
2. Used the **AzCopy** utility to copy blob data from one container to another

---

## 📂 Files Included

- 📄 [`copy-blob-using-azcopy.pdf`](./copy-blob-using-azcopy.pdf):  
  Contains screenshots and commands used to complete the AzCopy data transfer assignment.

---

## 💻 AzCopy Command Used

```bash
azcopy copy "https://<source-storage-account>.blob.core.windows.net/<source-container>/<blob-name>?<SAS-token>" \
            "https://<destination-storage-account>.blob.core.windows.net/<destination-container>/<blob-name>?<SAS-token>" \
            --recursive
```

> Replace `<source-storage-account>`, `<source-container>`, `<destination-storage-account>`, `<destination-container>`, `<blob-name>`, and `<SAS-token>` with actual values.

---

👩‍💻 **Author**  
Vaishnavi Golhar  
📧 Email: vaishnavigolhar05@gmail.com  
🔗 LinkedIn: [linkedin.com/in/vaishnavigolhar](https://www.linkedin.com/in/vaishnavigolhar)


