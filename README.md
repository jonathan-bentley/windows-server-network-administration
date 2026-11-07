# Windows Server & Network Administration
## A&J Market — IT Infrastructure Lab

### Project Overview

This project demonstrates the deployment, configuration, and administration of a small business IT infrastructure using Microsoft Azure and Windows Server 2025.

The lab simulates the IT environment of A&J Market, a fictional retail business. The goal was to build a centralized network environment, manage employee accounts, implement security policies, configure DNS, and establish secure network file sharing.

### Project Environment

| Component | Configuration |
|---|---|
| Cloud Platform | Microsoft Azure |
| Resource Group | `rg-ad-infrastructure` |
| Region | East US 2 |
| Domain Controller | `AZ-DC01` |
| Client Computer | `AZ-CLIENT01` |
| Server Operating System | Windows Server 2025 Datacenter |
| Client Operating System | Windows 11 Pro |
| Active Directory Domain | `corp.ajmarket.test` |
| Domain Controller IP | `10.0.0.4` |
| PowerShell | Used for employee account creation and administration |

### Technologies & Skills Demonstrated

- Microsoft Azure virtual machine deployment
- Windows Server administration
- Active Directory Domain Services (AD DS)
- Organizational Units (OUs) and user account management
- Group Policy and account lockout policies
- DNS records (A and CNAME)
- DNS caching and troubleshooting
- SMB network file sharing
- NTFS and share permissions
- Active Directory security groups
- PowerShell scripting
- Windows Event Viewer and security auditing

### Project Stages

1. **[Stage 1 — Azure Infrastructure](./Stage%201%20-%20Azure%20Infrastructure/README.md):** Deployed the domain controller and Windows 11 client virtual machines and configured network connectivity.
2. **[Stage 2 — Active Directory](./Stage%202%20-%20Active%20Directory/README.md):** Installed AD DS, created a domain, configured organizational units, and created employee accounts using PowerShell.
3. **[Stage 3 — Account Security](./Stage%203%20-%20Account%20Security/README.md):** Configured account lockout policies, tested account disabling and re-enabling, and reviewed Windows security events.
4. **[Stage 4 — DNS Configuration](./Stage%204%20-%20DNS%20Configuration/README.md):** Created and tested A and CNAME records, investigated DNS caching, and verified name resolution.
5. **[Stage 5 — Network File Shares and Permissions](./Stage%205%20-%20Network%20File%20Shares%20and%20Permissions/README.md):** Configured shared folders, access permissions, and security groups; tested access using a standard employee account.


### Project Objectives

- Build a functional Windows Server domain environment.
- Centralize employee account management through Active Directory.
- Apply security policies to protect user accounts.
- Configure and troubleshoot internal DNS.
- Control access to shared business resources.
- Demonstrate practical Windows administration and troubleshooting skills.

---

