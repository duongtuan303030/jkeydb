# jkeydb

a simple key-value database

how to install
```
pip install jkeydb
```
or
```
pip install git+https://github.com/duongtuan303030/jkeydb
```

how to use
```py
from jkeydb import database

with database("file name") as kv:
    #save items (support json and str and int)
    kv["key"] = 32323

    #load items
    data = kv["key"]
    print(data)

    #get all key as list
    data - kv.keys()
    print(data)

    #get all items as list
    data - kv.items()
    print(data)

    #get all values as list
    data - kv.values()
    print(data)

    #get all List keys with a prefix
    data = kv.prefix("text key")
    print(data)
```

#same as dict obj

# no with
```py
from jkeydb import database

kv = database("file name")

#save items (support json and str and int)
kv["key"] = 32323

#load items
data = kv["key"]
print(data)

#get all key as list
data - kv.keys()
print(data)

#get all items as list
data - kv.items()
print(data)

#get all values as list
data - kv.values()
print(data)

#get all List keys with a prefix
data = kv.prefix("text key")
print(data)
    

#save data
kv.close()

```
