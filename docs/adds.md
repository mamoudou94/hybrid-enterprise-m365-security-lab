# Active Directory Domain Services (AD DS)

# Overview

Configured an enterprise-style on-premises Active Directory environment using Windows Server 2025 to support:

- Hybrid identity
- Device management
- Group policy administration
- Hybrid Azure AD Join
- Intune enrollment

---

# AD DS Deployment

## Install Active Directory Domain Services

1. Open Server Manager
2. Select:
   - Add Roles and Features
3. Install:
   - Active Directory Domain Services
4. Install required features
5. Complete installation

---

# Promote Server to Domain Controller

## Configure New Forest

```text
barry-tech.local
```

Configured:
- DNS Server
- Global Catalog
- Forest Functional Level
- Domain Functional Level

---

# Configure DNS

Added forwarders:

```text
8.8.8.8
1.1.1.1
```

Validation:

```powershell
nslookup
ipconfig /all
```

---

# Configure UPN Suffix

Added custom UPN suffix:

```text
barry-tech.com
```

Updated user accounts to authenticate using:

```text
user@barry-tech.com
```

---

# Organizational Unit Structure

```text
Barry-Tech
│
├── Users
├── Devices
├── Admins
├── Security Groups
├── Servers
└── Service Accounts
```

---

# Security Groups

Configured:
- Intune Users
- MFA Users
- Defender Users
- Helpdesk Admins
- Device Groups

---

# Device Domain Join

1. Open:
   - Settings → System → About
2. Select:
   - Rename this PC (Advanced)
3. Join domain:

```text
barry-tech.local
```

4. Restart device
5. Verify domain login

---

# Group Policy Configuration

## GPO 1 — Register Domain Joined Computers as Devices

Path:

```text
Computer Configuration
→ Policies
→ Administrative Templates
→ Windows Components
→ Device Registration
```

Setting:

```text
Register domain joined computers as devices = Enabled
```

---

## GPO 2 — Automatic MDM Enrollment

Path:

```text
Computer Configuration
→ Policies
→ Administrative Templates
→ Windows Components
→ MDM
```

Setting:

```text
Enable automatic MDM enrollment using default Azure credentials = Enabled
```

Credential Type:

```text
User Credential
```

---

# Validation

Commands:

```powershell
gpupdate /force
gpresult /r
```

Verified:
- DNS resolution
- Domain join
- GPO application
- User authentication
