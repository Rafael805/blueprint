### What is a database?
+ A structured set of compmuterized data with an accesible interface 
+ A collection of data
+ EX: phonebook 
+ Provides method for accessing and manipulating that data 

## What is a relational database?
A relational database is a set of tables (relations). Each table consists of rows (fields of attributes) which could be of various types (integer, float, date, etc.) SQL is the language used to create and manipulate such database.

### Database VS Database Management System (DBMS) 
+ EX: App --> DBMS --> Database 
+ DBMS: PostgreSQL, Oracle Database
+ Database: MySQL, SQLite

# SQL vs. NoSQL
A no SQL database provides a mechanism for storage and retrieval of data which is modeld by means other than the tabular relations used in relational databases. MongoDB is a popular NoSQL database.

# SQL vs. MySQL 

**SQL**: Structured Query Language: 
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

**MySQL**  
+ Popular relational database
+ DBMS that implements SQL 
+ Primarily writing SQL 
+ Both MySQL and PostgreSQL have slight differences in syntax but are quite identical 
+ What makes databases (DBMS) unique are the features they offer, not the language
