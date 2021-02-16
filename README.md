# EasyDB
Easily manage SQLite3 databases in Python without any prior knowledge.

Example:
```py
from easydb import *
db = EasyDB("students.db")
db.create_table("info", "name", "age", "grade")
data = DBTable(db, "info")
data.insert_values(name="Mark Baker", age=11, grade=5)
close_db(db)
```
