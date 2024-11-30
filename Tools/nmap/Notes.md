# Scan ports

```
nmap <ip>
```

# Scan ports with software version

```
nmap -sV <ip>
```

# Scan ports with OS detection

```
nmap -O <ip>
```

# Scan all ports

```
nmap -p- <ip>
```

# Scan ports with ping probes (if original script for scan does not work)

```
nmap -Pn <ip>
```

# Specify the minimum number of packets (speeds up the scan as the number goes higher)

```
nmap --min-rate=1000 <ip>
```
