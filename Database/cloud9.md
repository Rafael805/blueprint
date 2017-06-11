Creating Databases Code
Start the CLI:
```
mysql-ctl cli; 
```

List available databases:

```
show databases; 
```

The general command for creating a database:

```
CREATE DATABASE <database_name>; 
```

A specific example:

```
CREATE DATABASE soap_store; 
```

To drop a database:

```
DROP DATABASE <database_name>; 
```

For Example:

```
DROP DATABASE hello_world_db; 
```

Remember to be careful with this command! Once you drop a database, it's gone!

Tell MySQL which database you want to be using: 

```
USE <database_name>; 
```



Check the currrently used database:

```
SELECT database();
```
 
-- example:  

```
USE dog_walking_app;
 
SELECT database();
```

# Tables 

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

Deleting Tables *Note:* Be careful with this command!
```
DROP TABLE <table_name>;
```




   
