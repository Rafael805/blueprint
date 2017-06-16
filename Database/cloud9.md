# Databases

Creating Databases Code
### Start
Start the CLI:
```
mysql-ctl cli; 
```

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

## CRUD (Create Read Update Delete)

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
