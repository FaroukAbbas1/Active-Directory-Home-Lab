# 06 - Group Policy Objects (GPO)

## Goal
Create and apply Group Policy Objects to enforce security settings and desktop restrictions across the domain.

## GPOs Created
| GPO Name | Linked To | Purpose |
|----------|-----------|---------|
| Password Policy | homelab.local | Enforce strong passwords |
| Login Banner | homelab.local | Display warning message at login |
| Disable Control Panel | HR OU | Restrict HR users from Control Panel |
| Mapped Drives | IT OU | Auto map IT share drive |

## Steps
1. Open Group Policy Management
2. Right click domain or OU → Create a GPO and link it here
3. Right click GPO → Edit
4. Configure the required settings
5. Run gpupdate /force on client machine
6. Verify policy applied with gpresult /r

## Key Settings
- Minimum password length: 10 characters
- Password history: 5 passwords remembered
- Account lockout threshold: 5 attempts
- Login banner text: "Authorized users only. All activity is monitored."

## Screenshots

![GPO Management](../screenshots/06-01-gpo-management.png)
![GPO Editor](../screenshots/06-03-gpo-editor.png)
![Password Policy Before](../screenshots/06-04-password-policy-before.png)
![Password Policy Configured](../screenshots/06-05-password-policy-configured.png)
![Lockout Policy](../screenshots/06-06-lockout-policy.png)
![Login Banner GPO](../screenshots/06-07-login-banner-gpo.png)
![Login Banner Settings](../screenshots/06-08-login-banner-settings.png)
![Disable Control Panel](../screenshots/06-09-disable-control-panel.png)
![Mapped Drive](../screenshots/06-10-mapped-drive.png)
![Login Banner](../screenshots/06-11-login-banner.png)
![Mapped Drive Z](../screenshots/06-12-mapped-drive-z.png)
![Control Panel Blocked](../screenshots/06-13-control-panel-blocked.png)
