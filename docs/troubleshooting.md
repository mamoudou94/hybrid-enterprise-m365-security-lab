# Troubleshooting

# Devices Not Appearing in Intune

Verified:
- MDM user scope
- Licensing
- Hybrid Join status
- Group Policy application

Commands:

```powershell
gpupdate /force
dsregcmd /status
```

---

# Azure AD Connect Sync Issues

Restarted:

```text
Microsoft Azure AD Sync
```

Forced synchronization:

```powershell
Start-ADSyncSyncCycle -PolicyType Delta
```

---

# Hybrid Join Failures

Verified:
- SCP configuration
- Device OU synchronization
- Azure AD Connect Health

Command:

```powershell
dsregcmd /status
```

---

# Defender Onboarding Failures

Verified:
- Intune connector
- Device compliance
- EDR onboarding profile assignment
- Defender licensing

---

# MFA Not Prompting

Verified:
- Conditional Access assignments
- User included in MFA scope
- Legacy authentication blocked
