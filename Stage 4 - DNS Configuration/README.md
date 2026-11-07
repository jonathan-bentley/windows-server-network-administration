# Stage 4 — DNS Configuration and Troubleshooting

## 1. Project Overview

This stage focuses on configuring and troubleshooting Domain Name System (DNS) services in the A&J Market Active Directory environment.

Using Windows Server 2025 and Windows 11, I created DNS records, tested hostname resolution, examined local DNS caching, and verified DNS changes using networking commands.

The objective was to gain hands-on experience with DNS administration and troubleshooting in a Windows domain environment.

## 2. Environment Configuration

- **Cloud Platform:** Microsoft Azure
- **Domain Controller / DNS Server:** AZ-DC01 (Windows Server 2025)
- **Client Computer:** AZ-CLIENT01 (Windows 11 Pro)
- **Active Directory Domain:** corp.ajmarket.test
- **DNS Server Private IP:** 10.0.0.4
- **Client Private IP:** 10.0.0.5

## 3. Technologies and Tools

- Windows Server DNS Manager
- Active Directory Domain Services
- DNS A Records
- DNS CNAME Records
- Windows DNS Resolver Cache
- Command Prompt
- PowerShell
- `ping`
- `nslookup`
- `ipconfig /displaydns`
- `ipconfig /flushdns`

## 4. Implementation Stages

1. Test hostname resolution before creating a DNS record.
2. Create a DNS A record for `fileserver` pointing to `10.0.0.4`.
3. Verify hostname resolution from the Windows 11 client.
4. Change the A record to `8.8.8.8` and examine the locally cached DNS result.
5. Flush the DNS resolver cache and verify the updated record.
6. Create a DNS CNAME record named `search` pointing to `www.google.com`.
7. Test the CNAME record using `ping` and `nslookup`.
8. Restore the `fileserver` A record to `10.0.0.4` and verify name resolution.

## 5. Project Outcome

Successfully configured and tested DNS records within the A&J Market domain.

Demonstrated how DNS A records map hostnames to IPv4 addresses, how CNAME records provide aliases for existing hostnames, and how locally cached DNS information can affect name resolution after a record changes.

Used `ping`, `nslookup`, and Windows DNS cache commands to investigate and verify DNS behavior.

Restored the original `fileserver` record after completing the troubleshooting exercises.
