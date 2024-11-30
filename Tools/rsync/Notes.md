# List shares

```
rsync --list-only <ip>::
```

# Use anonymous authentication

```
rsync --list-only <ip>::public
```

# Transfer file from remote machine to local

- Note: command returns no output
```
rsync <ip>::public/flag.txt flag.txt
```

