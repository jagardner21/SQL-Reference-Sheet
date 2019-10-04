# SQL Reference Sheet
---
## How to create a database
1. Open a SQL Shell (psql) window
2. Type the following statement, then hit enter:  
`CREATE DATABASE databaseName;`
3. Type `\l` to get a list of databases, and to confirm that your database was created  
![create database](CreateDatabase.jpg)
## How to delete a database
1. Enter command:  
`DROP DATABASE databaseName;`  
## How to create a table in a database
1. Connect to the database  
`\c testDB`  
2. Create the table (in parenthesis, enter the name of a key-space-data type, keys are comma separated)  
`CREATE TABLE users (id int, name text);`
3. Enter `\d` to check the list of relations (tables) to confirm table created  
## How to delete a table in a database  
1. Enter command: 
`DROP TABLE table_name`;  
## How to get everything from a single table  
1. Enter command:  
`SELECT * FROM table_name;`
## How to get one thing from a single table with a "where" clause  
1. Enter command:  
`SELECT * FROM table_name WHERE column-name = value;`
## How to add data/a row to table:  
1. Type following command, the parenthesis with column names is optional:  
`INSERT INTO table_name (column1, column2)`  
2. Hit Enter, then type the following:  
`VALUES (value-for-column1, value-for-column2);`  
3. Hit Enter, and data will be added to table  
## How to edit data in a table  
1. Specify the table you want to update, then hit enter:  
`UPDATE table_name`  
2. Specify the column you want to update, then hit enter:  
`SET column_name = newValue`  
3. Specify a condition in order to update the desired rows:  
`WHERE column_name = value;`  
e.g.  
`UPDATE users`  
`SET name = 'Jesse'`  
`WHERE id = 1;`  
## How to remove data/a row from a table:  
1. Specify the table you wish to delete a row from, then hit enter:  
`DELETE FROM table_name`  
2. Define a condition to specify what rows are to be deleted:  
`WHERE condition;`  
e.g.  
`DELETE FROM users`  
`WHERE id = 1;`  
