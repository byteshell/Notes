# Use mysql-cli specifying username

```
mysql -u <username> -h <ip>
```

# Connect to mysql without providing password

```
mysql -h <ip> -u root 
```

# Connect to mysql skipping SSL certificate (if throws an error about it)

```
mysql -h <ip> --skip-ssl
```

# Print databases which are accessible

- In mysql's CLI:
```
SHOW databases;
```

# Set database to use

- In mysql's CLI:
```
USE <database_name>;
```

# Show tables in database

- In mysql's CLI:
```
SHOW tables;
```

# Query table

- In mysql's CLI:
```
SELECT * FROM <table_name>;
```
