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

# Connect to host and share using username and password

```
smbclient -U <username>%<password> //<ip>/<share>
```
