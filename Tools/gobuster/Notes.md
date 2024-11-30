# Directory busting

```
gobuster <dir>
```

# Specify what pages needed

```
gobuster -x <extension>
```

# Use wordlist

```
gobuster -w <path_to_wordlist>
```

# Exclude other statuses

```
gobuster dir -u <URL> -w <wordlist> 2>&1 | grep -v "(404\|403)"
```

# Send output to the file

```
gobuster dir -u <URL> -w <wordlist> 2>&1 | grep -v "(404\|403)" > <filename>
```
