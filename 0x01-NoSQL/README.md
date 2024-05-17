# 0x01. NoSQL

## Description
This project is part of the ALX Backend curriculum and focuses on learning and implementing NoSQL concepts using MongoDB. It covers various tasks such as creating databases, inserting documents, querying data, and performing updates in MongoDB using Python scripts.

## Learning Objectives
- Understand the concept of NoSQL databases
- Differentiate between SQL and NoSQL databases
- Explore MongoDB and its usage
- Learn how to perform CRUD operations in MongoDB
- Gain proficiency in querying MongoDB data using Python

## Resources
To successfully complete this project, it is recommended to read or watch the following resources:
- [NoSQL Databases Explained](https://www.mongodb.com/nosql-explained)
- [What is NoSQL?](https://www.youtube.com/watch?v=sBVvgkqWa7M)
- [MongoDB with Python Crash Course - Tutorial for Beginners](https://www.youtube.com/watch?v=E-1xI85Zog8)
- [MongoDB Tutorial 2: Insert, Update, Remove, Query](https://www.youtube.com/watch?v=9awhlLfkSh4)
- [Introduction to MongoDB and Python](https://realpython.com/introduction-to-mongodb-and-python/)
- [mongo Shell Methods](https://docs.mongodb.com/manual/reference/method/)
- [Mongosh](https://docs.mongodb.com/mongodb-shell/)

## Requirements
### MongoDB Command File
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using MongoDB (version 4.2)
- All files should end with a new line
- The first line of all files should be a comment: `// my comment`
- A `README.md` file, at the root of the folder of the project, is mandatory

### Python Scripts
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7) and PyMongo (version 3.10)
- All files should end with a new line
- The first line of all files should be exactly `#!/usr/bin/env python3`
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5.*)
- All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- Your code should not be executed when imported (by using `if __name__ == "__main__":`)

### More Info
- Install MongoDB 4.2 in Ubuntu 18.04 (official installation guide provided)
- Ensure proper setup of MongoDB environment including service startup
- Handle potential issues like missing data directories or init.d files
- Utilize container-on-demand for running MongoDB if required

## More Info

### Install MongoDB 4.2 in Ubuntu 18.04

Follow the official installation guide:

```bash
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" > /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org

##Check MongoDB status:

$ sudo service mongod status
mongod start/running, process 3627
$ mongo --version
MongoDB shell version v4.2.8
git version: 43d25964249164d76d5e04dd6cf38f6111e21f5f
OpenSSL version: OpenSSL 1.1.1  11 Sep 2018
allocator: tcmalloc
modules: none
build environment:
    distmod: ubuntu1804
    distarch: x86_64
    target_arch: x86_64

##Install pymongo:

$ pip3 install pymongo

##Verify pymongo installation:

$ python3
>>> import pymongo
>>> pymongo.__version__
'3.10.1'

##Potential issue resolution:

$ sudo mkdir -p /data/db
Or if /etc/init.d/mongod is missing, please find an example of the file in this repository.
[Click to expand/hide file contents]

##In the container, start MongoDB before using it:

$ service mongod start
* Starting database mongod                                              [ OK ]

##List databases:

$ cat 0-list_databases | mongo
MongoDB shell version v4.2.8
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("70f14b38-6d0b-48e1-a9a4-0534bcf15301") }
MongoDB server version: 4.2.8
admin   0.000GB
config  0.000GB
local   0.000GB
bye


## Tasks
The project consists of several tasks covering different aspects of MongoDB usage and Python scripting. Each task has specific requirements and involves writing Python scripts to perform various operations on MongoDB collections.

## Repository Structure
- GitHub repository: [alx-backend-storage](https://github.com/username/alx-backend-storage)
- Directory: 0x01-NoSQL

## Tasks Overview
1. List all databases
2. Create a database
3. Insert document
4. List all documents
5. List all documents with a specific condition
6. Count documents
7. Update documents
8. Delete documents
9. List all documents in Python
10. Insert a document in Python
11. Update document attributes
12. Delete documents with a specific condition
13. Retrieve documents using regex filter
14. Retrieve top students based on average score
15. Analyze Nginx logs stored in MongoDB
