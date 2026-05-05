# Active Directory IAM Homelab

## Overview
Built a full enterprise-style Active Directory lab to simulate real-world Identity and Access Management (IAM).

This project demonstrates:
- Domain setup and configuration
- Organizational Unit (OU) design
- Security group-based access control
- File share permissions (NTFS + Share)
- Group Policy (GPO) drive mapping with targeting

---

## Environment
- Proxmox Virtualization
- Windows Server (Domain Controller)
- Windows 11 Client
- Domain: homelab.local

---

## What I Built

### Active Directory
- Created structured OU hierarchy
- Created users and security groups
- Implemented role-based access control

### File Shares
- Created HR, Finance, and IT shares
- Configured both Share and NTFS permissions

### Access Control
- HR users → access HR share
- Non-HR users → denied access

### Group Policy (GPO)
- Automated drive mapping (H:)
- Targeted using security group membership
- Verified successful mapping and restriction behavior

---

## Proof

### HR Access Granted
![HR Access](Enterprise-IAM-Homelab-Screenshots/04-File-Shares/hr-access-success.png)

### Finance Access Denied
![Finance Denied](Enterprise-IAM-Homelab-Screenshots/04-File-Shares/finance-access-denied.png)

### GPO Drive Mapping
![Drive Mapping](Enterprise-IAM-Homelab-Screenshots/05-GPO/drive-auto-mapped.png)

---

## Outcome
Successfully implemented identity-based access control using Active Directory, security groups, and Group Policy.

---

## Skills Demonstrated
- Active Directory Administration
- Identity & Access Management (IAM)
- Group Policy (GPO)
- Windows Server
- Troubleshooting (DNS, domain join, permissions)
- File share permissions (NTFS + SMB)
