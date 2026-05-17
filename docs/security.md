# Security Operations

# Overview

Configured Microsoft Defender for Endpoint and enterprise endpoint security controls.

---

# Defender Integration with Intune

Path:

```text
Endpoint Security
→ Microsoft Defender for Endpoint
```

Enabled:

```text
Connect Windows devices version 10 and later to Microsoft Defender for Endpoint
```

---

# Defender Onboarding Policy

Path:

```text
Endpoint Security
→ Endpoint Detection and Response
```

Created onboarding profile.

Assigned to:
- Device Groups

---

# Defender Onboarding Flow

```text
Windows Device
→ Intune Enrollment
→ Compliance Policies
→ Defender Onboarding Policy
→ Defender Sensor Installed
→ Device Appears in Defender Portal
```

---

# Validate Defender Onboarding

Verified:
- Device inventory
- Sensor health
- Risk level
- Security recommendations

---

# EDR Configuration

Configured:
- Endpoint Detection & Response
- Automated investigation
- Device isolation
- Threat remediation

---

# Web Content Filtering

Configured:
- Block malicious sites
- Restrict unsafe categories
- Monitor web activity

---

# Validation

Verified:
- Devices onboarded successfully
- Security recommendations visible
- Risk levels reporting correctly
- EDR active
