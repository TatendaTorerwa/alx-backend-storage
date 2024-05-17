# MySQL Advanced

## Introduction
This project focuses on advanced MySQL concepts, including creating tables with constraints, optimizing queries, implementing stored procedures, functions, views, and triggers.

## Concepts Covered
- Advanced SQL
  - Creating tables with constraints
  - Optimizing queries with indexes
  - Implementing stored procedures, functions, views, and triggers

## Resources
Read or watch:
- [MySQL cheatsheet](https://devhints.io/mysql)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://www.digitalocean.com/community/tutorials/how-to-leverage-mysql-indexing)
- [Stored Procedure](https://dev.mysql.com/doc/refman/8.0/en/stored-routines.html)
- [Triggers](https://dev.mysql.com/doc/refman/8.0/en/triggers.html)
- [Views](https://dev.mysql.com/doc/refman/8.0/en/views.html)
- [Functions and Operators](https://dev.mysql.com/doc/refman/8.0/en/functions.html)
- [Trigger Syntax and Examples](https://dev.mysql.com/doc/refman/8.0/en/trigger-syntax.html)
- [CREATE TABLE Statement](https://dev.mysql.com/doc/refman/8.0/en/create-table.html)
- [CREATE PROCEDURE and CREATE FUNCTION Statements](https://dev.mysql.com/doc/refman/8.0/en/create-procedure.html)
- [CREATE INDEX Statement](https://dev.mysql.com/doc/refman/8.0/en/create-index.html)
- [CREATE VIEW Statement](https://dev.mysql.com/doc/refman/8.0/en/create-view.html)

## Requirements
- Ubuntu 18.04 LTS
- MySQL 5.7 (version 5.7.30)
- All SQL files should end with a new line
- All SQL queries should have a comment just before
- All files should start with a comment describing the task
- All SQL keywords should be in uppercase
- A README.md file is mandatory at the root of the project folder

## Setup
- Use "container-on-demand" to run MySQL
- Start MySQL in the container using `$ service mysql start`
- Import a SQL dump using the provided commands

## Tasks
- [0. We are all unique!](./0-uniq_users.sql)
- [1. In and not out](./1-country_users.sql)
- [2. Best band ever!](./2-fans.sql)
- [3. Old school band](./3-glam_rock.sql)
- [4. Buy buy buy](./4-store.sql)
- [5. Email validation to sent](./5-valid_email.sql)
- [6. Add bonus](./6-bonus.sql)
- [7. Average score](./7-average_score.sql)
- [8. Optimize simple search](./8-index_my_names.sql)
- [9. Optimize search and score](./9-index_name_score.sql)
- [10. Safe divide](./10-div.sql)
- [11. No table for a meeting](./11-need_meeting.sql)

## Conclusion
This project provides hands-on experience with advanced MySQL features, enhancing database management skills.

## MySQL Usage Guide

### Comments for your SQL file
```bash
$ cat my_script.sql
-- 3 first students in the Batch ID=3
-- because Batch 3 is the best!
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;

##Running MySQL in a Container-on-Demand
###To run MySQL in a container-on-demand, follow these steps:

1. Ask for a container with Ubuntu 18.04 and Python 3.7.
2. Connect to the container via SSH or WebTerminal.
3. Start MySQL in the container before interacting with it:

$ service mysql start
 * MySQL Community Server 5.7.30 is started

##MySQL is started, you can list databases using the following command:

$ cat 0-list_databases.sql | mysql -uroot -p my_database
Enter password: 

4. This will display the list of databases available in MySQL.

In the container, the default credentials are root for both the username and password.

##Importing a SQL Dump

###To import a SQL dump into MySQL, follow these steps:

1. Create a new database using the following command:

$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
Enter password: 

2. Download the SQL dump file using curl and import it into the newly created database:

$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
Enter password: 

3. Verify the import by executing a query on the imported data, for example:

$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
Enter password: 

This will display the contents of the tv_genres table.

