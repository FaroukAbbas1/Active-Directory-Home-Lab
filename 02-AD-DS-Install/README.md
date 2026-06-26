# 02 - Active Directory DS Install & Domain Controller Promotion

## Goal
Install the Active Directory Domain Services role on Windows Server 2022 and promote it to a Domain Controller.

## Steps
1. Open Server Manager → Add Roles and Features
2. Select Active Directory Domain Services
3. Complete installation
4. Click the notification flag → Promote this server to a Domain Controller
5. Select "Add a new forest" and set domain name: homelab.local
6. Set DSRM password
7. Complete wizard and let server restart
8. Verify AD DS is running after reboot
9. Verify DNS is configured correctly

## Verification
- Logged in with HOMELAB\Administrator
- Active Directory Users and Computers opens successfully
- DNS Manager shows homelab.local zone

## Screenshots

![Add Roles](../screenshots/02-01-add-roles.png)
![Server Roles](../screenshots/02-02-server-roles.png)
![Confirmation](../screenshots/02-03-confirmation.png)
![Installing](../screenshots/02-04-installing.png)
![Installation Complete](../screenshots/02-05-installation-complete.png)
![Deployment Config](../screenshots/02-06-deployment-config.png)
![DC Options](../screenshots/02-07-dc-options.png)
![NetBIOS](../screenshots/02-08-netbios.png)
![Review Options](../screenshots/02-09-review-options.png)
![Login Screen](../screenshots/02-11-login-screen.png)
![Server Manager After DC](../screenshots/02-12-server-manager-after-dc.png)
![ADUC Open](../screenshots/02-13-aduc-open.png)
![DNS Manager](../screenshots/02-14-dns-manager.png)
