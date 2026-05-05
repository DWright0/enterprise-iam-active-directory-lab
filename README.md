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
![HR Access](Enterprise-IAM-Homelab-Screenshots/04-file-shares/05-access-validation-01-hr-access-success.png)

### Finance Access Denied
![Finance Denied](Enterprise-IAM-Homelab-Screenshots/04-file-shares/05-access-validation-02-finance-access-denied.png)

### File Share Permissions Config
![NTFS Permissions](Enterprise-IAM-Homelab-Screenshots/04-file-shares/04-file-shares-03-hr-ntfs-permissions.png)

---

## Troubleshooting (Real-World Issues Solved)

This lab required troubleshooting across multiple layers, including:

### DNS Issues
- Domain join initially failed due to DNS resolution problems
- Verified DNS server configuration using:
  - `ipconfig /all`
  - `nslookup homelab.local`
- Fixed by ensuring client pointed to Domain Controller for DNS

### Domain Join Failures
- Encountered "Domain Controller could not be contacted"
- Resolved by:
  - Verifying network connectivity (`ping`)
  - Fixing DNS configuration
  - Ensuring correct domain name usage

### File Share Access Issues
- Share worked but permissions failed initially
- Identified mismatch between:
  - Share permissions
  - NTFS permissions
- Fixed by aligning both permission layers

### GPO Not Applying
- Drive mapping did not appear initially
- Troubleshot using:
  - `gpupdate /force`
  - `gpresult /r`
- Confirmed:
  - Correct OU targeting
  - Security group membership
  - Item-level targeting configuration

---

## Outcome
Successfully implemented identity-based access control using Active Directory, security groups, file shares, and Group Policy.

---

## Skills Demonstrated
- Active Directory Administration
- Identity & Access Management (IAM)
- Group Policy (GPO)
- Windows Server
- DNS Troubleshooting
- Domain Join Debugging
- File Share Permissions (NTFS + SMB)
- Access Control Design
