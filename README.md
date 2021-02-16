# EasyDB
Easily manage SQLite3 databases in Python without any prior knowledge.

Example for initializing database:
```py
from easydb import *
db = EasyDB("students.db")
db.create_table("info", "name", "age", "grade")
data = DBTable(db, "info")
data.insert_values(name="Mark Baker", age=11, grade=5)
close_db(db)
```
Example for getting data from a database:
```py
from easydb import *
db = EasyDB("students.db")
data = DBTable(db, "info")
age = DBKey(data, "name", "age")
print(age["Mark Baker"])
# Outputs 11
```
