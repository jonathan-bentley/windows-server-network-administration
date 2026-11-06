# Stage 1 — Azure Infrastructure Deployment

## 1. Project Overview

The first stage of the A&J Market IT Infrastructure Lab involved building the foundation of a small business network using Microsoft Azure.

Two virtual machines were deployed in Azure: a Windows Server 2025 domain controller and a Windows 11 client computer. Both machines were connected to the same virtual network to establish communication between the server and client.

## 2. Environment Configuration

| Component | Configuration |
|---|---|
| Cloud Platform | Microsoft Azure |
| Resource Group | `rg-ad-infrastructure` |
| Azure Region | East US 2 |
| Virtual Network | `net-corp-network` |
| Network Address Space | `10.0.0.0/16` |
| Subnet | `default` |
| Subnet Address Range | `10.0.0.0/24` |
| Domain Controller | `AZ-DC01` |
| Domain Controller OS | Windows Server 2025 Datacenter |
| Domain Controller Private IP | `10.0.0.4` |
| Client Computer | `AZ-CLIENT01` |
| Client OS | Windows 11 Pro |
| Client Private IP | `10.0.0.5` |
| Client DNS Server | `10.0.0.4` |

## 3. Step-by-Step Implementation

### Step 1: Create the Azure Resource Group

1. Sign in to the Microsoft Azure Portal.
2. Search for **Resource groups** using the portal search bar.
3. Select **Create**.
4. Select the appropriate Azure subscription.
5. Enter `rg-ad-infrastructure` as the resource group name.
6. Select **East US 2** as the region.
7. Review the configuration and select **Review + create**.
8. Select **Create** to deploy the resource group.

**Expected Result:** The resource group `rg-ad-infrastructure` appears in the Azure Resource Groups list and provides a location for the lab's virtual machines and networking resources.

### Step 2: Create the Virtual Network

1. In the Azure Portal, search for **Virtual networks**.
2. Select **Create**.
3. Choose the resource group `rg-ad-infrastructure`.
4. Enter `net-corp-network` as the virtual network name.
5. Select **East US 2** as the region.
6. Configure the IPv4 address space as `10.0.0.0/16`.
7. Create a subnet named `default`.
8. Configure the subnet address range as `10.0.0.0/24`.
9. Review the configuration and select **Create**.

**Expected Result:** The virtual network and its default subnet are deployed successfully.

### Step 3: Deploy the Windows Server Domain Controller

1. In the Azure Portal, search for **Virtual machines**.
2. Select **Create** and then **Azure virtual machine**.
3. Select the resource group `rg-ad-infrastructure`.
4. Enter `AZ-DC01` as the virtual machine name.
5. Select **East US 2** as the region.
6. Choose **Windows Server 2025 Datacenter, Gen 2** as the operating system image.
7. Select an available virtual machine size.
8. Configure the administrator account using the username `labadmin`.
9. On the Networking tab, select the virtual network `net-corp-network`.
10. Select the `default` subnet.
11. Review the remaining settings and deploy the virtual machine.

**Expected Result:** Azure successfully deploys `AZ-DC01`, which serves as the Windows Server machine for the lab.

The server's private IP address was `10.0.0.4`.

### Step 4: Deploy the Windows 11 Client

1. Return to **Virtual machines** in the Azure Portal.
2. Select **Create** and then **Azure virtual machine**.
3. Select the resource group `rg-ad-infrastructure`.
4. Enter `AZ-CLIENT01` as the virtual machine name.
5. Select **East US 2** as the region.
6. Choose **Windows 11 Pro** as the operating system image.
7. Select an available virtual machine size.
8. Configure the local administrator account.
9. On the Networking tab, select `net-corp-network`.
10. Select the `default` subnet.
11. Review the configuration and deploy the virtual machine.

**Expected Result:** Azure successfully deploys `AZ-CLIENT01` within the same virtual network as the domain controller.

The client received the private IP address `10.0.0.5`.

### Step 5: Configure the Client's DNS Server

The client computer must use the domain controller as its DNS server so it can locate Active Directory services during the domain-joining process.

1. In the Azure Portal, open the `AZ-CLIENT01` virtual machine.
2. Navigate to its **Networking** settings.
3. Open the network interface associated with the client.
4. Locate **DNS servers** in the network interface settings.
5. Select the custom DNS server option.
6. Enter `10.0.0.4` as the DNS server address.
7. Save the configuration.

**Expected Result:** The client is configured to use `AZ-DC01` at `10.0.0.4` for DNS resolution.

The client's own private IP remains `10.0.0.5`.

### Step 6: Configure Network Connectivity

To test communication between the two virtual machines, ICMP traffic was enabled on the domain controller.

1. Connect to `AZ-DC01` through Remote Desktop.
2. Open PowerShell as an administrator.
3. Run the following command:

```powershell
Enable-NetFirewallRule -DisplayName "File and Printer Sharing (Echo Request - ICMPv4-In)"
```

4. Allow the command to complete.
5. Connect to `AZ-CLIENT01`.
6. Open Command Prompt or PowerShell.
7. Run the following command:

```powershell
ping 10.0.0.4
```

**Expected Result:** The client successfully receives replies from `10.0.0.4`, confirming network communication with the domain controller.

The connectivity test returned four successful replies.

## 4. Final Results

The first stage successfully established the Azure infrastructure needed for the remaining lab activities.

Completed tasks included:

- Created the Azure resource group.
- Deployed the virtual network and subnet.
- Deployed the Windows Server 2025 domain controller.
- Deployed the Windows 11 client computer.
- Configured the client to use the domain controller for DNS.
- Enabled ICMP traffic for connectivity testing.
- Successfully tested communication between both virtual machines.

This infrastructure provided the foundation for Stage 2, where Active Directory Domain Services was installed and configured.

## 5. Technologies Used

- Microsoft Azure
- Windows Server 2025 Datacenter
- Windows 11 Pro
- Azure Virtual Machines
- Azure Virtual Networks
- PowerShell
- Remote Desktop
- ICMP / Network Connectivity Testing
