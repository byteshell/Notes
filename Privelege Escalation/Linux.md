# Find files that can be run using sudo priveleges

```
find / -perm u=s -type f 2>/dev/null
```

# Find sudoers

```
sudo -l
```
