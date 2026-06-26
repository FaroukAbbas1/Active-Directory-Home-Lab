# 07 - Troubleshooting Scenarios

## Goal
Simulate and document real IT troubleshooting scenarios using the format: Problem → Diagnosis → Fix.

## Scenarios

---

### Scenario 1 - Account Lockout
**Problem:** User Amer Ahmed could not log in after multiple failed attempts.
**Diagnosis:** Checked account in ADUC → Account tab showed "Unlock account" checkbox confirming lockout.
**Fix:** Checked "Unlock account" in ADUC → user logged in successfully.

![Login Screen](../screenshots/07-01-login-screen.png)
![Account Locked](../screenshots/07-02-account-locked.png)
![Account Locked ADUC](../screenshots/07-03-account-locked-aduc.png)

---

### Scenario 2 - Password Reset
**Problem:** User forgot their password and could not log in.
**Diagnosis:** Confirmed user identity, located user in ADUC.
**Fix:** Right clicked user → Reset Password → set new temporary password.

![Password Reset](../screenshots/07-04-password-reset.png)
![Password Reset Done](../screenshots/07-05-password-reset-done.png)

---

### Scenario 3 - Access Denied to Shared Folder
**Problem:** IT user Ahmed Alaa could not access the IT$ shared folder.
**Diagnosis:** Checked NTFS permissions on C:\Shares\IT → IT-Team had Deny set on Full Control.
**Fix:** Removed Deny permission → confirmed Allow Full Control for IT-Team → access restored.

![Permissions Denied](../screenshots/07-06-permissions-denied.png)
![Access Denied](../screenshots/07-07-access-denied.png)
![Permissions Fixed](../screenshots/07-08-permissions-fixed.png)
![Access Restored](../screenshots/07-09-access-restored.png)

---

### Scenario 4 - GPO Not Applying
**Problem:** Password lockout policy was not applying to domain users.
**Diagnosis:** Ran gpresult /r on CLIENT01 → Password Policy GPO was missing from applied policies. GPO link was disabled.
**Fix:** Re-enabled GPO link → ran gpupdate /force → verified with gpresult /r.

![GPResult Working](../screenshots/07-10-gpresult-working.png)
![GPO Unlinked](../screenshots/07-11-gpo-unlinked.png)
![GPO Relinked](../screenshots/07-13-gpo-relinked.png)
![GPResult Restored](../screenshots/07-14-gpresult-policy-restored.png)

---

### Scenario 5 - DNS Failure
**Problem:** Client could not resolve homelab.local domain name.
**Diagnosis:** Ran nslookup homelab.local → timed out. DNS was pointing to wrong IP.
**Fix:** Changed DNS to 192.168.56.102 → ran ipconfig /flushdns → nslookup resolved successfully.

![NsLookup Fail](../screenshots/07-15-nslookup-fail.png)
![DNS Fixed](../screenshots/07-16-dns-fixed-settings.png)
![NsLookup Working](../screenshots/07-17-nslookup-working.png)
