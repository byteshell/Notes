# SMB port and service name

- Port: 445
- Service name: "microsoft-ds"

# List shares

```
smbclient -L <ip>
```

# Connect to the host and share

```
smbclient \\\\<ip>\\<share>
```

# Recursively retrieve files without prompt

- In smbclient's CLI:
```
RECURSE ON
PROMPT OFF
mget *
```

# Smbmap usage

```
smbmap -d <domain_name> -u <username> -p <password> -H <ip>
```
