0x02. Redis basic.
📃 Topics Covered.
💻 Tasks.
0. List all databases
📃 Task requirements.
Write a script that lists all databases in MongoDB.

guillaume@ubuntu:~/0x01$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 0-list_databases
chmod +x 0-list_databases

# Test
cat 0-list_databases | mongo
✔️ Solution
👉 0-list_databases

1. Create a database
📃 Task requirements.
Write a script that creates or uses the database my_db:

guillaume@ubuntu:~/0x01$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/0x01$
guillaume@ubuntu:~/0x01$ cat 1-use_or_create_database | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
switched to db my_db
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 1-use_or_create_database
chmod +x 1-use_or_create_database

# Test
cat 1-use_or_create_database | mongo
✔️ Solution
👉 1-use_or_create_database

2. Insert document
📃 Task requirements.
Write a script that inserts a document in the collection school:

The document must have one attribute name with value “Holberton school”
The database name will be passed as option of mongo command
guillaume@ubuntu:~/0x01$ cat 2-insert | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
WriteResult({ "nInserted" : 1 })
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 2-insert
chmod +x 2-insert

# Tests
cat 2-insert | mongo my_db
✔️ Solution
👉 2-insert

3. All documents
📃 Task requirements.
Write a script that lists all documents in the collection school:

The database name will be passed as option of mongo command
guillaume@ubuntu:~/0x01$ cat 3-all | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 3-all
chmod +x 3-all

#Test
cat 3-all | mongo my_db
✔️ Solution
👉 3-all

4. All matches
📃 Task requirements.
Write a script that lists all documents with name="Holberton school" in the collection school:

The database name will be passed as option of mongo command
guillaume@ubuntu:~/0x01$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 4-match
chmod +x 4-match
cat 4-main.sql | mysql -uroot -p holberton 

# Test
cat 4-match | mongo my_db
✔️ Solution
👉 4-match

5. Count
📃 Task requirements.
Write a script that displays the number of documents in the collection school:

The database name will be passed as option of mongo command
guillaume@ubuntu:~/0x01$ cat 5-count | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
1
bye
guillaume@ubuntu:~/0x01$
🔧 Task setup.
# Create task files and set execute permission.
touch 5-count
chmod +x 5-count
cat 5-init.sql | mysql -uroot -p holberton 

# Tests
touch 5-init.sql
chmod +x 5-init.sql
cat 5-count | mysql -uroot -p holberton 

