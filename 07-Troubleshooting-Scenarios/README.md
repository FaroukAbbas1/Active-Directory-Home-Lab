# 07 - Troubleshooting Scenarios

## Goal
Simulate and document real IT troubleshooting scenarios using the format: Problem → Diagnosis → Fix.

## Scenarios

---

### Scenario 1 - Account Lockout
**Problem:** User Amer Ahmed could not log in after multiple failed attempts.
**Diagnosis:** Checked account in ADUC → Account tab showed "Unlock account" checkbox appeared confirming lockout.
**Fix:** Checked "Unlock account" in ADUC → Account was unlocked and user logged in successfully.
**Screenshot:** 07-02-account-locked.png | 07-03-account-locked-aduc.png

---

### Scenario 2 - Password Reset
**Problem:** User forgot their password and could not log in.
**Diagnosis:** Confirmed user identity, located user in ADUC.
**Fix:** Right clicked user → Reset Password → set new temporary password.
**Screenshot:** 07-04-password-reset.png | 07-05-password-reset-done.png

---

### Scenario 3 - Access Denied to Shared Folder
**Problem:** IT user Ahmed Alaa could not access the IT$ shared folder.
**Diagnosis:** Checked NTFS permissions on C:\Shares\IT → IT-Team had Deny set on Full Control.
**Fix:** Removed Deny permission → confirmed Allow Full Control for IT-Team → access restored.
**Screenshot:** 07-06-permissions-denied.png | 07-07-access-denied.png | 07-08-permissions-fixed.png

---

### Scenario 4 - GPO Not Applying
**Problem:** Password lockout policy was not applying to domain users.
**Diagnosis:** Ran gpresult /r on CLIENT01 → Password Policy GPO was not in applied policies list. Found GPO link was disabled in Group Policy Management.
**Fix:** Re-enabled GPO link → ran gpupdate /force → verified policy applied with gpresult /r.
**Screenshot:** 07-10-gpresult-working.png | 07-11-gpo-unlinked.png | 07-14-gpresult-policy-restored.png

---

### Scenario 5 - DNS Failure
**Problem:** Client could not resolve homelab.local domain name.
**Diagnosis:** Ran nslookup homelab.local → DNS request timed out. Checked network adapter settings → DNS was pointing to wrong IP.
**Fix:** Changed DNS to correct server IP 192.168.56.102 → ran ipconfig /flushdns → nslookup resolved successfully.
**Screenshot:** 07-15-nslookup-fail.png | 07-16-dns-fixed-settings.png | 07-17-nslookup-working.png
