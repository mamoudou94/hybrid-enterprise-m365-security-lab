# Endpoint Management

# Overview

Configured Microsoft Intune for enterprise endpoint management, compliance enforcement, and device security.

---

# Configure Intune

Configured Microsoft Intune as MDM authority.

---

# Automatic Enrollment Configuration

Path:

```text
Devices
→ Enroll Devices
→ Automatic Enrollment
```

Configured:

| Setting | Value |
|---|---|
| MDM User Scope | All |
| MAM User Scope | None |

---

# Hybrid Enrollment Flow

```text
1. Device joins Active Directory
2. Device syncs to Entra ID
3. Device becomes Hybrid Azure AD Joined
4. MDM auto-enrollment policy applies
5. Device enrolls into Intune
6. Compliance policies apply
7. Defender onboarding policy applies
8. Device onboarded to Defender
```

---

# Validate Intune Enrollment

Command:

```powershell
dsregcmd /status
```

Verified:
- MDMUrl
- TenantId
- DeviceId

---

# Compliance Policies

Configured:
- BitLocker required
- Firewall enabled
- Antivirus required
- TPM required
- Secure Boot required
- Password policy enforcement

---

# Configuration Profiles

Configured:
- Device restrictions
- Endpoint protection
- Browser restrictions
- Security hardening

---

# Security Baselines

Configured:
- Windows Security Baseline
- Defender Security Baseline
- Edge Security Baseline

---

# Windows LAPS

Configured:
- Automatic password rotation
- Password backup to Entra ID
- Local admin account management

---

# Windows Autopilot

## Export Hardware Hash

```powershell
Get-WindowsAutopilotInfo.ps1
```

Uploaded hardware hash CSV into Intune.

Configured:
- User-driven deployment
- Entra ID Join
- Automatic enrollment

---

# Validation

Verified:
- Device appears in Intune
- Compliance policies applied
- Configuration profiles assigned
- Security baselines deployed
