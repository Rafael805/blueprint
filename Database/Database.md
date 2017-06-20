# What is a database?
+ A structured set of compmuterized data with an accesible interface 
+ A collection of data
+ EX: phonebook 
+ Provides method for accessing and manipulating that data 

# Relational Database Management Systems (RDBMS)
A relational database management system (RDBMS) is a program that lets you create, update, and administer a relational database. Most relational database management systems use SQL to access the database. A relational database is a set of tables (relations). Each table consists of rows (fields of attributes) which could be of various types (integer, float, date, etc.) SQL is the language used to create and manipulate such database.

# Key Difference between DBMS and RDBMS
+ EX: App --> DBMS --> Database 
+ DBMS: PostgreSQL, Oracle Database
+ Database: MySQL, SQLite

# SQL vs. NoSQL
A no SQL database provides a mechanism for storage and retrieval of data which is modeld by means other than the tabular relations used in relational databases. MongoDB is a popular NoSQL database.

# SQL (Structured Query Language)  
+ SQL is the language we use to "talk" to our database 
+ Exists seperately from MySQL
+ EX: Find all users who are 18 or olders  
```  
SELECT * FROM Users WHERE Age >= 18;
```  
+ Relational databases that use SQL: MySQL, SQLite, PostgreSQL, Oracle, ...
+ SQL is not unique to MySQL  
+ There is a SQL Standard on how SQL should work 
+ Once you learn SQL, it's pretty easy to switch to another DB that uses SQL 

Here is a brief description of popular types of RDBMS: 

# MySQL 
+ The most popular open source SQL database.
+ DBMS that implements SQL 
+ Primarily writing SQL 
+ Both MySQL and PostgreSQL have slight differences in syntax but are quite identical 
+ What makes databases (DBMS) unique are the features they offer, not the language

# SQLite
+ SQLite is a popular open source SQL database. 
+ Able to store an entire database in a single file.
+ All of the data can be stored locally without having to connect your database to a server.
+ SQLite is a popular choice for databases in cellphones, PDAs, MP3 players, set-top boxes, and other electronic gadgets.

# PostgreSQL
+ Open source SQL database that is not controlled by any corporation. 
+ Typically used for web application development.
+ Shares many of the same advantages of MySQL.
+ It is easy to use, inexpensive, reliable, and has a large community of developers.
+ Provides some additional features such as foreign key support without requiring complex configuration.
+ The main disadvantage of PostgreSQL is that it is slower in performance than other databases such as MySQL.
+ Less popular than MySQL which makes it harder to come by hosts or service providers that offer managed PostgreSQL instances.

# Oracle DB
+ Oracle DB is owned by the Oracle corporation and the code is not open sourced.
+ Used for large applications, particularly in the banking industry. 
+ Most of the world’s top banks run Oracle applications because Oracle offers a powerful combination of technology and comprehensive, pre-integrated business applications, including key functionality built specifically for banks.
+ The main disadvantage of using Oracle is that it is not free to use like its open source competitors and can be quite expensive.

# SQL Server
+ Owned by Microsoft.
+ Mainly used by large enterprise applications.
+ The major difference between Oracle and SQL Server is that SQL Server only supports the Windows Operating System.
