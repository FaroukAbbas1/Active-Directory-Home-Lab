# 04 - Domain Joining Windows 11

## Goal
Join the Windows 11 client machine to the homelab.local domain and verify login with a domain user.

## Prerequisites
- Windows Server 2022 DC is running
- Both VMs are on the same Host-Only network
- Windows 11 VM DNS is pointed to DC's IP: 192.168.56.102

## Steps
1. On Windows 11 VM set DNS to 192.168.56.102
2. Open Settings → System → About → Domain or workgroup
3. Click Change → Select Domain → type homelab.local
4. Enter domain admin credentials when prompted
5. Restart the machine
6. Log in with a domain user account

## Verification
- Logged in as HOMELAB\Ahmed.Alaa successfully
- CLIENT01 appears in Active Directory Users and Computers under Computers
- Ran nltest /dsgetdc:homelab.local to confirm DC connection

## Screenshots

![Client Network](../screenshots/04-03-client-network.png)
![Client Static IP](../screenshots/04-04-client-static-ip.png)
![Ping Server](../screenshots/04-05-ping-server.png)
![System Properties](../screenshots/04-06-system-properties.png)
![Change Domain](../screenshots/04-07-change-domain.png)
![Domain Credentials](../screenshots/04-08-domain-credentials.png)
![Domain User Desktop](../screenshots/04-09-domain-user-desktop.png)
![Client in ADUC](../screenshots/04-10-client-in-aduc.png)
![Domain Verified](../screenshots/04-11-domain-verified.png)
