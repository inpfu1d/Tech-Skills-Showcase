# قائمة التحقق لتأمين الخوادم (Server Hardening Checklist)
# Server Hardening & Security Checklist

This document outlines key security measures implemented to reduce the attack surface and secure network infrastructure, based on **Google IT Support Professional Certificate** standards.

## 1. Network Security Principles

###  Implicit Deny Strategy
**Concept:** The firewall should reject all traffic by default unless explicitly allowed.
- [ ] Configure firewall rules to drop all incoming/outgoing traffic at the end of the Access Control List (ACL).
- [ ] Only open essential ports (e.g., 80/443 for Web, 22 for SSH) required for specific business needs.
- [ ] **Why?** This prevents unauthorized access from unknown IP addresses or via unused ports.

## 2. Secure Remote Access

###  Bastion Host Implementation
**Concept:** A special purpose computer on a network specifically designed and configured to withstand attacks.
- [ ] Set up a Bastion Host (Jump Box) in the DMZ (Demilitarized Zone).
- [ ] Force all SSH/RDP connections to internal servers to pass through the Bastion Host first.
- [ ] Enable Multi-Factor Authentication (MFA) on the Bastion Host.
- [ ] **Why?** It acts as a single, hardened entry point, preventing direct exposure of critical internal servers to the public internet.

## 3. Attack Surface Reduction

###  Service Hardening
**Concept:** Disabling unnecessary services to minimize potential vulnerabilities.
- [ ] Audit running services using `systemctl` (Linux) or `Get-Service` (Windows).
- [ ] Stop and disable unused services (e.g., FTP, Telnet, Print Spooler on servers that don't need them).
- [ ] **Why?** Every running service is a potential entry point for hackers. If you don't need it, kill it.

---
*Created by: [Ahmed Abdullah Ba-abbad / inpFu1d]*
*Skills Applied: Network Security, Risk Management, System Hardening.*
