# What is SQL (Structured Query Language)?

SQL is a programming language designed to manage data stored in relational databases. SQL operates through simple, declarative statements. This keeps data accurate and secure, and helps maintain the integrity of databases, regardless of size.

One of the core purposes of the SQL language is to retrieve information stored in a database. This is commonly referred to as querying. **Queries** allow us to communicate with the database by asking questions and having the result set return data relevant to the question. ```SELECT``` is used every time you want to query data from a database.


```SELECT DISTINCT``` is used to return unique values in the result set and filters out all duplicate values. 
```
SELECT DISTINCT <column_name> FROM <table_name>;
```

```LIKE``` is a special operator used with the WHERE clause to search for a specific pattern in a column.
--example: 
```
SELECT * FROM movies
WHERE name LIKE 'Se_en';
```
```Se_en``` represents a pattern with a wildcard character. The ```_``` means you can substitute any individual character here without breaking the pattern. The names ```Seven``` and ```Se7en``` both match this pattern.

```%``` is a wildcard character that matches zero or more missing letters in the pattern.

```A%``` matches all movies with names that begin with "A"
```%a``` matches all movies that end with "a"

The ```BETWEEN``` operator is used to filter the result set within a certain range. The values can be numbers, text or dates. 

--example:
```
SELECT * FROM movies WHERE year BETWEEN 1990 AND 2000;
```
In this statement, the ```BETWEEN``` operator is being used to filter the result set to only include movies with ```year```s between 1990 up to and including 2000. ```AND``` is an operator that combines two conditions. Both conditions must be true for the row to be included in the result set.
--example:
```
SELECT * FROM movies
WHERE genre = 'comedy'
OR year < 1980;
```
The ```OR``` operator can also be used to combine more than one condition in a ```WHERE``` clause. The ```OR``` operator evaluates each condition separately and if any of the conditions are true then the row is added to the result set.

You can sort the results of your query using ```ORDER BY```. Sorting the results often makes the data more useful and easier to analyze. ```DESC``` is a keyword in SQL that is used with ```ORDER BY``` to sort the results in *descending order* (high to low or Z-A). It is also possible to sort the results in ascending order. ```ASC``` is a keyword in SQL that is used with ```ORDER BY``` to sort the results in ascending order (low to high or A-Z).

--example: 
```
SELECT * FROM movies
ORDER BY imdb_rating DESC;
```

```LIMIT``` is a clause that lets you specify the maximum number of rows the result set will have. It lets you specify the maximum number of rows that the query will return. This is especially important in large tables that have thousands or even millions of rows.


# Databases

### List databases
List available databases:
```
show databases; 
```

### Create database
The general command for creating a database:
```
CREATE DATABASE <database_name>; 
```

--example: ```CREATE DATABASE soap_store;```

### Use database
Tell MySQL which database you want to be using: 
```
USE <database_name>; 
```

### Check database
Check the currrently used database:
```
SELECT database();
```
 
-- example:  

```
USE dog_walking_app;
 
SELECT database();
```

### Drop database
To drop a database:

```DROP DATABASE <database_name>; ```

--example: ```DROP DATABASE hello_world_db; ```

Remember to be careful with this command! Once you drop a database, it's gone!

# Tables 

### Create table 
Create a table 
*Note:* table names should be pluralized

```
CREATE TABLE <table_name> (
    <column_name> <data_type>,
    <column_name> <data_type>
  );
```

-- examlpe: 
```
CREATE TABLE cats (
    name VARCHAR(100),
    age INT
  );
```

### NULL/NOT NULL && DEFAULT
--example:
``` CREATE TABLE cats(name VARCHAR(100) NOT NULL, age INT NOT NULL);```

Using NOT NULL will not allow a empty value as data

Setting default values:
--example: 
```
CREATE TABLE cats4
  (
    name VARCHAR(20) NOT NULL DEFAULT ‘unnamed’,
    age INT NOT NULL DEFAULT 99
  );
```

### Assigning key w/ autoincrement 
--example:
```
CREATE TABLE unique_cats2 (
    cat_id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    PRIMARY KEY (cat_id)
);
```

### Show tables 
Show current tables in your database
```
SHOW TABLES;
```

Show columns from a specific table 
```
SHOW COLUMNS FROM <table_name>;
```
**Or...**(Describe table name)
```
DESC <table_name>;
```

### Drop table
Deleting Tables *Note:* Be careful with this command!
```
DROP TABLE <table_name>;
```

-- example:
```
CREATE TABLE pastries
  (
    name VARCHAR(100),
    quantity INT
  );
 
SHOW TABLES;
 
DESC pastries;
 
DROP TABLE pastries;
```

# Insert 

### Add data
Adding data to a table  
```
INSERT INTO <table_name>(<column_name>, <column_name>) #specifying the columns
VALUES (<data>, <data>) #the values for the columns
```

--example:
```
INSERT INTO cats(name, age) VALUES ('Jetson', 7);
```

# Warning 

### Show warnings
To show warnings use: 
```SHOW WARNINGS;```

# Aliases (AKA)

```SELECT <column_name> AS <new_column_name> FROM <table>;```
*Note:* The fields do not really change. You can check by printing your table. 

# Source 
To execute an SQL script file use the source command:

``` source book_data.sql```

# String Functions 

## Concatenate
```CONCAT (<column_name>, 'text', <another_column_name>, 'more text' ```

--example: 
```
SELECT author_fname AS first, author_lname AS last, 
  CONCAT(author_fname, ' ', author_lname) AS full
FROM books;
```

To save you typing use ```CONCAT_WS``` to add a text/symbol 
```
SELECT 
    CONCAT_WS(' - ', title, author_fname, author_lname) 
FROM books;
```

## Substring
--example: 
```
SELECT SUBSTRING('Hello World', 1, 4);
```

## Replace
--example: 
```
SELECT REPLACE('Hello World', 'Hell', '%$#@');
```

## Reverse
--example:
```
SELECT REVERSE('Hello World');
```
## Character lenght 
--example:
```
SELECT CHAR_LENGTH('Hello World');
 ```
 Output: 11
 
 ## Upper/Lowercase
 --example: 
 ```
SELECT UPPER('Hello World');
Output: HELLO WORLD
 
SELECT LOWER('Hello World');
OUTPUT: hello world
```
 
# CRUD (Create Read Update Delete)

### Create 
```INSERT INTO <table_name>(<column_name>, <column_name>) VALUES(<value>, <value>);```

### Read
```SELECT * FROM <table_name>;```
```SELECT <column_name>, <column_name> FROM <table_name>;```
--example:```SELECT size, color FROM shirts;

```SELECT * FROM <table_name> WHERE <column_name> = <value>```
--example:```SELECT * FROM food WHERE name='Egg'```
*Note:* Egg && EGG will give you the same results because it is case insensitive 

```SELECT cat_id, age WHERE cat_id=age;```

### Update 
```UPDATE <table_name> SET <column_name> = <value> WHERE <column_name> = <value>```

--example:  ```UPDATE cats SET breed= `Shorthair WHERE breed = `Tabby`;```

--example: ```UPDATE cats SET age=14 WHERE name='Misty';```

When you're updating something make sure you're selecting the right data. Try SELECTing before you UPDATE. 

### Delete
```DELETE FROM <table_name> WHERE <column_name> = <value>```

--example: ```DELETE FROM cats WHERE name='Fluffy';```

*Note:* SELECT the data before using DELETE.

To delete all the data in the table use: ```DELETE FROM <table_name>```

This is different from dropping a table. Dropping a table gets rid of the table entirely and all data inside of it but DELETE just deletes the entrie s but you are still left with the table. 

