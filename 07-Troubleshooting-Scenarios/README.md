# 07 - Troubleshooting Scenarios

## Goal
Simulate and document real IT troubleshooting scenarios using the format: Problem → Diagnosis → Fix.

## Scenarios

---

### Scenario 1 - User Cannot Log In
**Problem:** Domain user reports they cannot log into their machine.
**Diagnosis:** Checked account in ADUC — account was locked out after failed attempts.
**Fix:** Right clicked user → Properties → Account tab → unlocked the account.

---

### Scenario 2 - Cannot Access Shared Folder
**Problem:** User reports "Access Denied" when trying to open department share.
**Diagnosis:** Checked Security tab on folder — user was not a member of the correct group.
**Fix:** Added user to the correct security group in ADUC. Access restored immediately.

---

### Scenario 3 - Group Policy Not Applying
**Problem:** Desktop restriction policy not applying to HR user.
**Diagnosis:** Ran gpresult /r on client — GPO was not being applied due to wrong OU link.
**Fix:** Moved GPO link to correct OU in Group Policy Management. Ran gpupdate /force.

---

### Scenario 4 - Windows 11 Cannot Join Domain
**Problem:** Client machine returns error when trying to join homelab.local.
**Diagnosis:** Pinged DC from client — no response. Checked DNS settings on client.
**Fix:** Changed DNS on Windows 11 to point to DC's static IP instead of router IP.

---

### Scenario 5 - Password Reset
**Problem:** User forgot password and is locked out.
**Diagnosis:** Confirmed identity via help desk procedure.
**Fix:** Right clicked user in ADUC → Reset Password → set temporary password → checked "User must change password at next logon."

## Screenshots
*(screenshots will be added here)*
