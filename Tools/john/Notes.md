# Run johntheripper with wordlist and file

- First of all, add your found hash into separate file. It is not necessary, but will be much better to use

```
john -w=<wordlist> <file>
```

# Convert .psafe to john

```
pwsafe2john <psafe_file> > pwsafe_hash.txt
```
