# Stage 3 — Account Security and Group Policy

## 1. Project Overview

This stage focuses on implementing and testing account security controls in the A&J Market Active Directory environment.

Using Windows Server 2025 and Windows 11, I configured account lockout policies through Group Policy, performed user account administration, and examined Windows Security Event Logs to monitor authentication activity.

The objective was to demonstrate practical skills in securing domain user accounts, troubleshooting authentication issues, and monitoring security events.

## 2. Environment Configuration

- **Cloud Platform:** Microsoft Azure
- **Domain Controller:** AZ-DC01 (Windows Server 2025)
- **Client Computer:** AZ-CLIENT01 (Windows 11 Pro)
- **Active Directory Domain:** corp.ajmarket.test
- **Domain Administrator:** CORP\john_admin
- **Test Employee Account:** CORP\qip.tese

## 3. Technologies and Tools

- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Active Directory Users and Computers (ADUC)
- Windows Local Security Policy
- Windows Event Viewer
- Remote Desktop Protocol (RDP)
- Windows PowerShell

## 4. Implementation Stages

1. Configure an account lockout policy using Group Policy.
2. Apply and verify the updated Group Policy settings.
3. Test account lockout using unsuccessful login attempts.
4. Unlock a locked employee account and reset its password.
5. Disable and re-enable an employee account to test access restrictions.
6. Enable successful and failed logon auditing on the Windows 11 client.
7. Review Windows Security Event Logs for authentication activity.

## 5. Project Outcome

Successfully implemented and tested account security controls within the A&J Market domain.

Configured an account lockout threshold of five failed sign-in attempts, with a 15-minute lockout duration and a 15-minute reset interval.

Demonstrated account unlocking, password resets, account disabling and re-enabling, and security event monitoring using Windows Event Viewer.

Verified authentication activity using Windows Security Event IDs 4624 (successful logon) and 4625 (failed logon).
