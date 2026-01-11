# Data Encryption & Secure Communications

##  Project Overview
The objective of this project is to implement **Data Confidentiality** using encryption techniques. I demonstrated how to protect sensitive information across different platforms, even when facing system-specific limitations.

## 🛠 Skills Demonstrated
* **Symmetric Encryption:** Using GPG for file-level protection in Linux.
* **Cryptographic Scripting:** Using PowerShell to transform plain text into encrypted secure strings.
* **Problem Solving:** Identifying OS limitations (Windows Home Edition) and implementing programmatic workarounds to achieve security goals.

##  Implementation Details

### 1. Windows Environment (PowerShell Scripting)
Since the standard `cipher` command (EFS) is restricted in Windows Home Edition, I utilized PowerShell's cryptographic cmdlets to encrypt sensitive data within a file.

**Workflow:**
```powershell
# Encrypt plain text and save it to a file
"Credit Card: 1234-5678" | ConvertTo-SecureString -AsPlainText -Force | ConvertFrom-SecureString | Out-File secret-data.txt

# Verify content (displays encrypted string)
cat secret-data.txt
