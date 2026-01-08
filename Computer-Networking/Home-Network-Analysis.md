#  Home Network Diagnostics & Performance Analysis

**Date:** 2026-01-08
**Technician:** Ahmed Ba-abbad
**Device Tested:** Personal Laptop (Wi-Fi Connection)

---

## 1. Network Configuration (Current State)
*Analyzed via command line (`ipconfig /all`)*

* **Private IP Address:** 192.168.1.107
* **Subnet Mask:** 255.255.255.0
* **Default Gateway (Router):** 192.168.1.1
* **Current DNS Servers:** 192.168.1.1

---

## 2. Connectivity & Latency Tests
*Tested connectivity to local gateway and public internet.*

### A. Local Router Test
*Command: `ping 192.168.1.1`*
* **Result:** Successful.
* **Latency:** < Minimum = 2ms, Maximum = 8ms, Average = 5ms.

### B. Internet Connectivity Test
*Command: `ping 8.8.8.8 `*
* **Result:** Successful.
* **Average Latency:** Minimum = 166ms, Maximum = 198ms, Average = 182ms
* **Notes:** High latency observed (Avg 182ms) due to 4G/LTE Wireless Connection.

### C. Path Analysis (Trace Route)
*Command: `tracert google.com`*
* **Hops Count:** 14 hops to reach destination.

---

## 3. Optimization Recommendation
**Observation:** Latency is high due to wireless cellular constraints.

**Action Plan:**

Optimize 4G Router placement to improve Signal-to-Noise Ratio (SINR).

Switch to Google Public DNS (8.8.8.8) to improve web browsing resolution speed, although this will not reduce ICMP latency.

* **Preferred Primary DNS:** 8.8.8.8
* **Preferred Secondary DNS:** 8.8.4.4
