# 04 - Domain Joining Windows 11

## Goal
Join the Windows 11 client machine to the homelab.local domain and verify login with a domain user.

## Prerequisites
- Windows Server 2022 DC is running
- Both VMs are on the same Host-Only network
- Windows 11 VM DNS is pointed to the DC's IP address

## Steps
1. On Windows 11 VM, set DNS to the Server's static IP
2. Open Settings → System → About → Domain or workgroup
3. Click Change → Select Domain → type homelab.local
4. Enter domain admin credentials when prompted
5. Restart the machine
6. On login screen, sign in with a domain user account

## Verification
- Logged in as HOMELAB\john.smith successfully
- Machine appears in Active Directory Users and Computers under Computers

## Screenshots
*(screenshots will be added here)*

## Notes & Issues
*(document any issues you ran into and how you fixed them)*
