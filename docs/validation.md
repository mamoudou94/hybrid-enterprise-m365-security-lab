# Validation & Testing

# Hybrid Join Validation

Command:

```powershell
dsregcmd /status
```

Verified:

```text
AzureAdJoined = YES
DomainJoined = YES
```

---

# Intune Enrollment Validation

Verified:
- Device appears in Intune
- Compliance status active
- Policies applied successfully

---

# Defender Validation

Verified:
- Device appears in Defender portal
- Sensor active
- Risk score reporting
- Security recommendations available

---

# MFA Validation

Verified:
- MFA challenge during login
- Conditional Access enforcement

---

# Compliance Validation

Verified:
- BitLocker enabled
- Antivirus active
- Firewall enabled
- Device compliance reporting
