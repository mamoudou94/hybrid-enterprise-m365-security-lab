# Identity & Access Management (IAM)

# Overview

Configured a hybrid identity environment integrating Active Directory with Microsoft Entra ID using Azure AD Connect.

Implemented enterprise authentication, access control, governance, and privileged access management.

---

# Tenant Setup

Configured:
- Microsoft 365 E5 tenant
- Custom domain
- Administrative roles
- User licensing

---

# Custom Domain Configuration

Added:

```text
barry-tech.com
```

Validated ownership using DNS TXT records.

![UPN Suffix](./Screenshoots/custom-domain.png)

---

# Azure AD Connect Deployment

Installed Azure AD Connect on Windows Server 2025.

Configured:
- Password Hash Synchronization
- Seamless Single Sign-On
- Password Writeback
- OU Filtering

![UPN Suffix](./Screenshoots/pwd-sync.png)

Synchronized:
- Users
- Devices
- Security Groups

![UPN Suffix](./Screenshoots/ou-filtering.png)
---

# Hybrid Azure AD Join

Enabled:

```text
Hybrid Azure AD Join
```

For:

```text
Windows 10 and later
```
![UPN Suffix](./Screenshoots/custom-domain.png)
---

# Validate Hybrid Join

Command:

```powershell
dsregcmd /status
```
![UPN Suffix](./Screenshoots/validate-hybride-joined.png)

# Multi-Factor Authentication (MFA)

Configured:
- Microsoft Authenticator
- SMS verification
- MFA enforcement

![UPN Suffix](./Screenshoots/mfa.png)
---

# Conditional Access Policies

Configured:
- Require MFA
- Block legacy authentication
- Require compliant devices
- Restrict admin access

---

# Risk-Based Policies

Configured:
- Sign-in risk policies
- User risk policies

---

![UPN Suffix](./Screenshoots/conditional-access.png)

# RBAC

Configured:
- Global Administrator
- Intune Administrator
- Security Administrator
- Compliance Administrator
- Helpdesk Administrator

---

# Privileged Identity Management (PIM)

Configured:
- Eligible role assignments
- Just-in-Time access
- Approval workflows
- Time-limited activation

![UPN Suffix](./Screenshoots/pim-process.png)
![UPN Suffix](./Screenshoots/pim.png)
---

# Identity Governance

Configured:
- Access Reviews
- Entitlement Management
- Lifecycle Workflows
![UPN Suffix](./Screenshoots/lifecycle-workflow.png)
![UPN Suffix](./Screenshoots/entitlement.png)
---

# Self-Service Password Reset (SSPR)

Configured:
- Password writeback
- Authentication methods
- Self-service reset policies

---

