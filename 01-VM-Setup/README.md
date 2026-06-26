# 01 - Virtual Machine Setup

## Goal
Set up two virtual machines in VirtualBox — one for Windows Server 2022 (Domain Controller) and one for Windows 11 (Client).

## VM 1 - Windows Server 2022

| Setting | Value |
|--------|-------|
| Name | DC01 |
| RAM | 2048 MB |
| Storage | 50 GB |
| Network Adapter 1 | NAT (for internet) |
| Network Adapter 2 | Host-Only (for internal communication) |

## VM 2 - Windows 11

| Setting | Value |
|--------|-------|
| Name | CLIENT01 |
| RAM | 4096 MB |
| Storage | 60 GB |
| Network Adapter 1 | NAT |
| Network Adapter 2 | Host-Only (same as server) |

## Steps
1. Create Host-Only network in VirtualBox Network Manager
2. Create DC01 VM with settings above and attach Windows Server 2022 ISO
3. Create CLIENT01 VM with settings above and attach Windows 11 ISO
4. Install Windows Server 2022 on DC01
5. Install Windows 11 on CLIENT01

## Screenshots

![VirtualBox Start](../screenshots/01-01-virtualbox-start.png)
![VM Name ISO](../screenshots/01-02-vm-name-iso.png)
![RAM Settings](../screenshots/01-03-ram-settings.png)
![Storage Settings](../screenshots/01-04-storage-settings.png)
![Host Only Network](../screenshots/01-05-host-only-network.png)
![Network Settings](../screenshots/01-06-network-settings.png)
![Windows Setup Language](../screenshots/01-07-windows-setup-language.png)
![OS Selection](../screenshots/01-08-os-selection.png)
![Custom Install](../screenshots/01-09-custom-install.png)
![Installing](../screenshots/01-10-installing.png)
![Set Password](../screenshots/01-11-set-password.png)
![Server Manager](../screenshots/01-12-server-manager.png)
![Win11 VM Name](../screenshots/01-14-win11-vm-name.png)
![Win11 Language](../screenshots/01-18-win11-language.png)
![Win11 Edition](../screenshots/01-20-win11-edition.png)
![Win11 Installing](../screenshots/01-21-win11-installing.png)
![Win11 Desktop](../screenshots/01-24-win11-desktop.png)
