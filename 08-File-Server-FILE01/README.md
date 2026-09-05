# 08 - File Server (FILE01)

## Goal
Move file sharing responsibilities off the Domain Controller (DC01) onto a dedicated File Server (FILE01), following the principle of not overloading a DC with non-essential roles.

## VM Specs

| Setting | Value |
|--------|-------|
| Name | FILE01 |
| OS | Windows Server 2022 Standard (Desktop Experience) |
| RAM | 2048 MB |
| Storage | 40 GB |
| CPUs | 2 |
| Network Adapter 1 | NAT |
| Network Adapter 2 | Host-Only (same network as DC01/CLIENT01) |
| Static IP | 192.168.56.103 |
| DNS | 192.168.56.102 (DC01) |

## Steps
1. Create FILE01 VM in VirtualBox with the specs above
2. Install Windows Server 2022 (manual install, Desktop Experience edition)
3. Configure static IP and DNS pointing to DC01
4. Rename computer to FILE01
5. Join FILE01 to the homelab.local domain
6. Verify FILE01 appears in Active Directory Users and Computers under Computers
7. Recreate shared folders (IT, HR, Finance, Management) on FILE01
8. Reapply NTFS + Share permissions matching each department's security group
9. Update the Mapped Drives GPO to point to \\FILE01\ instead of \\DC01\
10. Remove the shares from DC01 to keep the DC clean

## Verification
- (to be filled in after testing)

## Screenshots

<!-- add screenshots here, e.g.
![FILE01 VM Creation](../screenshots/08-01-file01-vm-creation.png)
![FILE01 Domain Joined](../screenshots/08-02-file01-domain-joined.png)
-->
