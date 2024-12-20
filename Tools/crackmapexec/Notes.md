# Crackmapexec + smb

```
crackmapexec smb <ip> -d <domain> -u <username> -p <password>
```

# Look for shares

```
crackmapexec smb <ip> -u <username> -p <password> --shares
```

# Check if winrm is available

```
crackmapexec winrm <ip> -u <username> -p <password>
```

# Send Bloodhound

```
crackmapexec ldap <ip> -u <username> -p <password> --bloodhound --collection All --dns-server <ip>
```
