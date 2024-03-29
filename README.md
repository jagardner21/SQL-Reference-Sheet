# SQL Reference Sheet
---
## How to start a SQL Shell (psql) session  
1. Open a SQL Shell (psql) window by searching for SQL Shell (psql) in the Windows search bar/Cortana  
2. Line will read "Server [localhost]:", hit Enter  
3. Line will read "Database [(default database)]:", hit Enter  
4. Line will read "Port [(default port number)]:", hit Enter  
5. Line will read "Username [(default username)]:", hit Enter  
6. Line will read "Password for user (default username):", enter password if you have set one up for Postgres, then Enter.  If you have not set a password, just hit enter  
## How to create a database  
2. Type the following statement, then hit enter:  
```SQL 
CREATE DATABASE databaseName;
```
3. Type `\l` to get a list of databases, and to confirm that your database was created
## How to delete a database
1. If you are currently connected to the database you wish to delete, enter the command `\q` to quit the database connection (this will quit the SQL session as well)
2. Enter command:  
```SQL  
DROP DATABASE databaseName;
```  
## How to create a table in a database
1. Connect to the database  
`\c databaseName`  
2. Create the table (in parenthesis, enter the name of a key-space-data type, keys are comma separated)  
```SQL  
CREATE TABLE users (id int, name text);
```
3. Enter `\d` to check the list of relations (tables) to confirm table created  
## How to delete a table in a database  
1. Enter command: 
```SQL  
DROP TABLE table_name;
```  
## How to get everything from a single table  
1. Enter command:  
```SQL  
SELECT * FROM table_name;
```
## How to get one thing from a single table with a "where" clause  
1. Enter command:  
```SQL  
SELECT * FROM table_name WHERE column_name = value;
```
## How to add data/a row to table:  
1. Type following command, the parenthesis with column names is optional:  
```SQL  
INSERT INTO table_name (column1, column2)
```  
2. Hit Enter, then type the following:  
```SQL  
VALUES (value-for-column1, value-for-column2);
```  
3. Hit Enter, and data will be added to table  
## How to edit data in a table  
1. Specify the table you want to update:  
```SQL  
UPDATE table_name
```  
2. Hit Enter, then specify the column you want to update, use 'WHERE' to specify a condition in order to update the desired rows:  
```SQL  
SET column_name = newValue WHERE column_name = value;
```  
e.g.  
```SQL  
UPDATE users
```  
```SQL  
SET name = 'Jesse' WHERE id = 1;
```  
## How to remove data/a row from a table:  
1. Specify the table you wish to delete a row from, use 'WHERE' to define the condition to specify what rows are to be deleted:  
```SQL  
DELETE FROM table_name WHERE condition;
```  
e.g.  
```SQL  
DELETE FROM users WHERE id = 1;
```  
