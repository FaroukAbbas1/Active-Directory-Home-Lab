# 01 - Virtual Machine Setup

## Goal
Set up two virtual machines in VirtualBox — one for Windows Server 2022 (Domain Controller) and one for Windows 11 (Client).

## VM 1 - Windows Server 2022

| Setting | Value |
|--------|-------|
| Name | DC01 |
| RAM | 2048 MB minimum |
| Storage | 50 GB |
| Network Adapter 1 | NAT (for internet) |
| Network Adapter 2 | Host-Only (for internal communication) |

## VM 2 - Windows 11

| Setting | Value |
|--------|-------|
| Name | CLIENT01 |
| RAM | 2048 MB minimum |
| Storage | 50 GB |
| Network Adapter | Host-Only (same as server) |

## Steps
1. Download VirtualBox from virtualbox.org
2. Create VM for Windows Server 2022 with settings above
3. Attach Windows Server 2022 ISO
4. Create VM for Windows 11 with settings above
5. Attach Windows 11 ISO

## Screenshots
*(screenshots will be added here)*

## Notes & Issues
*(document any issues you ran into and how you fixed them)*
