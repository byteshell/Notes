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
