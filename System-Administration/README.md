# Service Lifecycle Management (Infrastructure Support)

##  Project Overview
This project demonstrates the ability to manage critical system services in both **Windows** and **Linux**. Understanding how to start, stop, and verify services is a fundamental skill for any System Administrator to troubleshoot application failures and maintain system stability.

## Skills Demonstrated
* **Service Monitoring:** Checking the real-time status of system daemons and services.
* **Control Operations:** Safely stopping and starting services via CLI.
* **Infrastructure Troubleshooting:** Simulating a service reset to resolve potential application hangs.

##  Implementation Details

### 1. Windows Environment (PowerShell)
I managed the **Print Spooler** service, which is a critical component for printing operations.

```powershell
# Check current status
Get-Service Spooler

# Stop the service to simulate maintenance
Stop-Service Spooler

# Restart the service to restore functionality
Start-Service Spooler
