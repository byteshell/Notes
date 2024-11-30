# Install mongosh

```
curl -O https://downloads.mongodb.com/compass/mongosh-2.3.2-linux-x64.tgz
tar xvf mongosh-2.3.2-linux-x64.tgz
```

# Connect to mongodb using mongosh

```
./mongosh mongodb://<ip>:<port>
```

# Show databases

- In mongosh:
```
show dbs;
```

# Show collections

- In mongosh:
```
show collections;
```

# Command to dump contents of all documents within the collection (pretty format)

- In mongosh:
```
db.flag.find().pretty();
```
