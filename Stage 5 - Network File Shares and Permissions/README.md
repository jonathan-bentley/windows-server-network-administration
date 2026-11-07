# Stage 5 — Network File Shares and Permissions

## Project Overview

In this lab, I configured and tested network file shares on a Windows Server 2025 domain controller hosted in Microsoft Azure. I implemented different folder access permissions and used Active Directory security groups to control access to shared resources.

## Lab Environment

- **Cloud Platform:** Microsoft Azure
- **Domain Controller:** AZ-DC01 (Windows Server 2025)
- **Client Computer:** AZ-CLIENT01 (Windows 11 Pro)
- **Active Directory Domain:** corp.ajmarket.test
- **Shared Folders:** read-access, write-access, no-access, accounting
- **Security Group:** ACCOUNTANTS

## Technologies and Tools

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- Windows File Explorer
- SMB Network File Sharing
- Windows Share Permissions
- Active Directory Security Groups

## Lab Objectives

1. Create folders for network file sharing.
2. Configure different levels of shared-folder permissions.
3. Access shared folders from a domain-joined Windows 11 client.
4. Verify read-only, write, and restricted access.
5. Create an Active Directory security group for accounting users.
6. Assign permissions using security group membership.
7. Verify that group membership grants access to the accounting folder.

## Implementation and Testing

Detailed configuration steps and screenshots will be added below.
