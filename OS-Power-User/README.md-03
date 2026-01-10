# User & Permissions Management (Cross-Platform Implementation)

## Project Overview
This project demonstrates the implementation of the **Principle of Least Privilege (PoLP)** across both **Windows** and **Linux** environments.

The goal was to simulate a real-world scenario where a support staff member (`Help-Desk-user`) requires read-only access to sensitive system logs, strictly denying modification or deletion rights.

##  Skills Demonstrated
* **User Management:** Creating users via CLI (`net user` / `useradd`).
* **Access Control (ACLs):** Configuring permissions using `icacls` (Windows) and `chmod` (Linux).
* **Inheritance:** Managing permission propagation (`OI` `CI` / Recursive ownership).
* **Cross-Platform Proficiency:** Executing equivalent administrative tasks on both operating systems.

##  Implementation Details

### 1. Windows Environment (PowerShell)
I executed the following commands to create the restricted environment:

```powershell
# Create user & directory
net user Help-Desk-user Password123 /add
mkdir c:\secure-logs

# Grant Read-Only access with inheritance
icacls "C:\secure-logs" /grant "Help-Desk-user:(OI)(CI)R"

**Verification:**
The screenshot confirms `Help-Desk-user` has `(R)` access with inheritance `(OI)(CI)`.

![Windows Proof](Win.png)

### 2. Linux Environment (Ubuntu via WSL)
I replicated the same security controls on an Ubuntu system using standard Linux administration commands:

```bash
# Create user & directory
sudo useradd Help-Desk-user
sudo mkdir /var/secure-logs

# Set ownership and permissions (750: rwxr-x---)
sudo chown root:Help-Desk-user /var/secure-logs
sudo chmod 750 /var/secure-logs

**Verification:**
The output `drwxr-x---` confirms that the group `Help-Desk-user` has Read/Execute permissions, while others have no access.

![Linux Proof](Lin.png)
