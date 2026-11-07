# Stage 2 — Active Directory Implementation

## 1. Project Overview

The second stage of the A&J Market IT Infrastructure Lab focused on implementing Active Directory Domain Services (AD DS) to establish centralized user and computer management.

A Windows Server 2025 virtual machine was configured as the domain controller. A new Active Directory domain was created, organizational units were established to organize company accounts and computers, and employee accounts were created using PowerShell.

The Windows 11 client computer was then joined to the domain to test centralized authentication.

## 2. Environment Configuration

| Component | Configuration |
|---|---|
| Cloud Platform | Microsoft Azure |
| Domain Controller | `AZ-DC01` |
| Client Computer | `AZ-CLIENT01` |
| Server Operating System | Windows Server 2025 Datacenter |
| Client Operating System | Windows 11 Pro |
| Active Directory Domain | `corp.ajmarket.test` |
| NetBIOS Name | `CORP` |
| Domain Controller IP | `10.0.0.4` |
| Administrator Account | `CORP\john_admin` |
| PowerShell Script | `AJMarket_CreateEmployees.ps1` |

## 3. Technologies & Skills Demonstrated

- Active Directory Domain Services (AD DS)
- Windows Server 2025 administration
- Domain controller configuration
- Active Directory domain creation
- Organizational Unit (OU) management
- User and administrator account management
- Active Directory security groups
- PowerShell scripting
- Bulk employee account creation
- Windows domain joining
- Domain authentication and login testing

## 4. Implementation Stages

1. **Install Active Directory Domain Services:** Added the AD DS server role to Windows Server 2025.
2. **Promote the Server to Domain Controller:** Created the new forest and domain `corp.ajmarket.test`.
3. **Create Organizational Units:** Established `_EMPLOYEES`, `_ADMINS`, and `_CLIENTS` to organize directory objects.
4. **Create an Administrator Account:** Created `john_admin` and assigned the appropriate domain administrator membership.
5. **Create Employee Accounts:** Used a PowerShell script to generate 20 employee accounts within the `_EMPLOYEES` OU.
6. **Join the Client to the Domain:** Joined `AZ-CLIENT01` to `corp.ajmarket.test` and organized its computer object within `_CLIENTS`.
7. **Test Domain Authentication:** Signed in to the Windows 11 client using a domain employee account to verify authentication.

## 5. Project Outcome

Successfully established a centralized Active Directory environment for the simulated A&J Market business.

The completed configuration allows administrators to manage employee accounts and computers from a centralized directory rather than managing each computer independently.

This environment provides the foundation for the next stage, which focuses on account security and Group Policy.

---

