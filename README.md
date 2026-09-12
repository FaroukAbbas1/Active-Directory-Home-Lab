# Active Directory Home Lab

A hands-on home lab project built to demonstrate core Windows Server, Active Directory, networking, and firewall/VPN security skills relevant to Help Desk, SysAdmin, and Network Security roles.

## Environment
- Windows Server 2022 (Domain Controller — DC01)
- Windows Server 2022 (File Server — FILE01)
- Windows 11 (Client Machines — CLIENT01, CLIENT02)
- pfSense CE (Router/Firewall/VPN Gateway)
- VirtualBox (Hypervisor)

## What This Lab Covers
| Step | Topic |
|------|-------|
| 00 | Network Topology Diagram |
| 01 | VirtualBox & ISO Setup |
| 02 | Active Directory DS Install & Domain Controller Promotion |
| 03 | Organizational Units, Users & Groups |
| 04 | Domain Joining Windows 11 |
| 05 | Shared Folders & NTFS Permissions |
| 06 | Group Policy Objects (GPO) |
| 07 | Troubleshooting Scenarios |
| 08 | Dedicated File Server (FILE01) |
| 09 | DHCP Server |
| 10 | Second Domain Client (CLIENT02) |
| 11 | pfSense Firewall (VM Setup) |
| 12 | pfSense Gateway Migration |
| 13 | pfSense Firewall Rules (Default-Deny Policy) |
| 14 | VPN (OpenVPN) — Secure Remote Access |

## Skills Demonstrated
- Windows Server 2022 administration
- Active Directory setup and management (AD DS, DNS, DHCP)
- Group Policy configuration (password policy, restrictions, mapped drives, security hardening)
- User, group, and permission management across multiple departments
- File server deployment and share/NTFS permission design
- Firewall/router deployment and administration (pfSense)
- Default-Deny (whitelist) firewall policy design
- Secure remote access via VPN with least-privilege access control
- Network troubleshooting (DNS, DHCP, connectivity, authentication, domain communication, firewall/routing)
- Documentation of real-world troubleshooting scenarios (Problem → Diagnosis → Fix)
