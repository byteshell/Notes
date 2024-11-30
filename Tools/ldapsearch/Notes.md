# Query Domain Controller for Active Directory UserAccountControl attributes of active accounts

- "active.htb" -> "dc=active,dc=htb"
```
ldapsearch -x -H 'ldap://<ip>' -D '<domain_name>' -w '<password>' -b
"dc=active,dc=htb" -s sub "(&(objectCategory=person)(objectClass=user)(!
(useraccountcontrol:1.2.840.113556.1.4.803:=2)))" samaccountname | grep sAMAccountName
```

-s sub : The -s option specifies the search scope. sub means a subtree search, including the
base DN and all its child entries. This is the most comprehensive search scope, as it traverses the
entire directory tree below the base DN.

```(&(objectCategory=person)(objectClass=user)(! (useraccountcontrol:1.2.840.113556.1.4.803:=2)))``` is an LDAP search filter to find all user
objects that are not disabled. Here's the breakdown:

- ```objectCategory=person``` : Searches for objects in the category "person".
- ```objectClass=user``` : Narrows down to objects with a class of "user".
- ```!(useraccountcontrol:1.2.840.113556.1.4.803:=2)``` : Excludes disabled accounts. The
userAccountControl attribute is a bit flag; this part of the filter excludes accounts with the
second bit set (which indicates a disabled account).
