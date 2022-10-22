# contents
**1** [**Introduction: What is SQL?**](#Introduction-What-is-SQL?)

**2** [**SQL features?**](#SQL-Features?)

**3** [**Basic SQL**](#Basic-SQL?)

**4** [**important SQL keywords**](#important-sql-keywords)


**5** [**clauses in SQL**](#clauses-in-SQL)


# Introduction-What-is-SQL?

To get introduced to **SQL**, we first need to know about Databases and **Database Management Systems(DBMS)**.
Data is basically a collection of facts related to some object. A **Database** is a collection of small units of data arranged in a systematic manner.
A **Relational Database Management System** is a collection of tools that allows the users to **manipulate, organize and visualize** the contents of a database while following some standard rules that facilitate fast response between the database and the user side.

After getting introduced to the concept of data, databases and **DBMS/RDBMS**, we can finally learn about SQL.
SQL or **Structured Query Language** is basically the language that we (the user) use to communicate with the Databases and get our required interpretation of data out of it. 
It is used for **storing, manipulating and retrieving** data out of a database.



# SQL-Features?


The following functionalities can be performed on a database using SQL:

	
```sql
  1 Create or Delete a Database.
```

```sql
  2 Create or Alter or Delete some tables in a Database.
```
```sql
  3 SELECT data from tables.
 ```
```sql
  4 INSERT data into tables.
```
```sql
  5 UPDATE data in tables.
```
``` sql
  6 DELETE data from tables.
```
``` sql 
  7 Create Views in the database.
```
``` sql 
  8 Execute various aggregate functions.
```


# Basic SQL

**1 Create Database and drop database**


| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| **1** CREATE DATABASE| CREATE DATABASE databasename  | Used to create new SQL database in the server        |
| **2** DROP DATABASE  | CREATE DATABASE databasename  | Used to drop the existing database   |

# 2 String-Datatype


The table below lists all the String type datatypes available in SQL, along with their descriptions:

|Datatype |	Description|
|---------|---------------|
|**1**  CHAR(size) |	A fixed-length string containing numbers, letters or special characters. Length may vary from 0-255.|
|**2**  VARCHAR(size)	|Variable-length string where the length may vary from 0-65535. Similar to CHAR.|
|**3**  TEXT(size)|	Can contain a string of size up to 65536 bytes. |
|**4**  TINY TEXT	|Can contain a string of up to 255 characters.|
|**5**  MEDIUM TEXT |	Can contain a string of up to 16777215 characters.|
|**6**  LONG TEXT|	Can contain a string of up to 4294967295 characters.|
|**7**  BINARY(size)|	Similar to CHAR() but stores binary byte strings.|
|**8**  VARBINARY(size)|	Similar to VARCHAR() but stores binary byte strings.|
|**9**  BLOB(size)|	Holds blobs up to 65536 bytes.|
|**10** TINYBLOB|	It is used for Binary Large Objects and has a maximum size of 255bytes.|
|**11** MEDIUMBLOB|	Holds blobs up to 16777215 bytes.|
|**12** LONGBLOB	|Holds blobs upto 4294967295 bytes.|
|**13** ENUM(val1,val2) |	String object that can have only 1 possible value from a list of size at most 65536 values in an ENUM list. If no value is inserted, a blank value is inserted.|
|**14** SET(val1,val2,…)	|String object with 0 or more values, chosen from a list of possible values with a maximum limit of 64 values.|



# Numeric Datatypes:
The table below lists all the Numeric Datatypes in SQL along with their descriptions:

|Datatype	|Description|
|-------|-------------|
|**1** BIT(size) |	Bit-value type, where size varies from 1 to 64. Default value: 1|
|**2** INT(size)	|Integer with values in the signed range of -2147483648 to 2147483647 and values in the unsigned range of 0 to 4294967295.|
|**3** TINYINT(size)	|Integer with values in the signed range of -128 to 127 and values in the unsigned range of 0 to 255.|
|**4** SMALLINT(size)|	Integer with values in the signed range of -32768 to 32767 and values in the unsigned range of 0 to 65535.|
|**5** MEDIUMINT(size)	|Integer with values in the signed range of -8388608 to 8388607 and values in the unsigned range of 0 to 16777215.|
|**6** BIGINT(size) |	Integer with values in the signed range of 9223372036854775808 to 9223372036854775807 and values in the unsigned range of 0 to 18446744073709551615.|
|**7** BOOLEAN	|Boolean values where 0 is considered as FALSE and non-zero values are considered TRUE.|
|**8** FLOAT (p)	|The floating-point number is stored. If the precision parameter is set between 0 to 24, the type is FLOAT() else if it lies between 25 to 53, the datatype is DOUBLE().|
|**9** DECIMAL(size,d) |	Decimal number with a number of digits before decimal place set by size parameter, and a number of digits after the decimal point set by d parameter. Default values: size = 10, d = 10. Maximum Values: size = 65, d = 30.|

# Date/Time Datatypes:
The datatypes available in SQL to handle Date/Time operations effectively are called the Date/Time datatypes. The below table lists all the Date/Time variables in SQL along with their description:

|Datatype|	Description|
|-------|---------|
|**1** DATE	|Stores date in YYYY-MM-DD format with dates in the range of ‘1000-01-01’ to ‘9999-12-31’.|
|**2** TIME(fsp)	|Stores time in hh:mm:ss format with times in the range of ‘-838:59:59’ to ‘838:59:59’.|
|**3** DATETIME(fsp)	|Stores a combination of date and time in YYYY-MM-DD and hh:mm:ss format, with values in the range of ‘1000-01-01 00:00:00’ to ‘9999-12-31 23:59:59’.|
|**4** TIMESTAMP(fsp)	|It stores values relative to the Unix Epoch, basically a Unix Timestamp. Values lie in the range of ‘1970-01-01 00:00:01’ UTC to ‘2038-01-09 03:14:07’ UTC.|
|**5** YEAR	|Stores values of years as a 4digit number format, with a range lying between -1901 to 2155.|




# 2 Tables

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| CREATE TABLE| CREATE TABLE table_name (column1 datatype,column2 datatype,column3 datatype)  | Used to create new table        |
| DROP TABLE  | DROP TABLE table_name  | Used to drop the existing table   |
|TRUNCATE TABLE|TRUNCATE TABLE table_name|used to delete the data inside a table, but not the table itself.|


# 3 Alter Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| ALTER TABLE ADD| ALTER TABLE table_name ADD column_name datatype  | Used to add column in existing table        |
| ALTER TABLE DROP  | ALTER TABLE table_name DROP COLUMN column_name  | Used to drop column in existing table   |
| ALTER TABLE MODIFY|ALTER TABLE table_name MODIFY COLUMN column_name datatype |Used to modify column in existing table |

# 4 Insert Data into Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| INSERT INTO| INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...); | Used to insert data for particular columnn to add new records into  existing table        |
| INSERT INTO  |INSERT INTO table_name VALUES (value1, value2, value3, ...);  | used to insert new record in existing table with all column  |

# 5 Update Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| UPDATE| UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;  | Used to update data for particular row for existing records in existing table        |
| UPDATE| UPDATE table_name SET column1 = value1, column2 = value2, ... ;| Used to update data for all row exist in existing table        |



# 6 Delete Table 
| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| DELETE|DELETE FROM table_name WHERE condition;  | Used to delete data for particular row for existing records in existing table        |
| DELETE| DELETE FROM table_name;| Used to delete data for all row exist in existing table        |


# important-sql-keywords

|Keyword |	Description |	Example|
|----------|---------|------------|
|ADD |	Will add a new column to an existing table.|	ALTER TABLE student ADD email_address VARCHAR(255)|
|ALTER TABLE |	Adds edits or deletes columns in a table|	ALTER TABLE student DROP COLUMN email_address|
|ALTER COLUMN|	Can change the datatype of a table’s column|	ALTER TABLE student ALTER COLUMN phone VARCHAR(15)|
|AS	|Renames a table/column with an alias existing only for the query duration.|	SELECT name AS student_name, phone FROM student|
|ASC |Used in conjunction with ORDER BY to sort data in ascending order.|	SELECT column1, column2, … FROM table_name ORDER BY column1, column2, … ASC|
|DESC |	Used in conjunction with ORDER BY to sort data in descending order.|	SELECT column1, column2, … FROM table_name ORDER BY column1, column2, … DESC|
|CHECK	|Constrains the value which can be added to a column.|	CREATE TABLE student(fullName varchar(255), age INT, CHECK(age >= 18))|
|CREATE DATABASE|	Creates a new database.	|CREATE DATABASE student;|
|DEFAULT|	Sets the default value for a given column.|	CREATE TABLE products(ID int, name varchar(255) DEFAULT ‘Username’, from date DEFAULT GETDATE())|
|DELETE	|Delete values from a table.	|DELETE FROM users WHERE user_id= 674|
|DROP COLUMN|	Deletes/Drops a column from a table.|	ALTER TABLE student DROP COLUMN name|
|DROP DATABASE|	Completely deletes a database with all its content within.|	DROP DATABASE student|
|DROP DEFAULT|	Removes a default value for a column.	|ALTER TABLE student ALTER COLUMN age DROP DEFAULT|
|DROP TABLE|	Deletes a table from a database.|	DROP TABLE students|
|FROM|	Determines which table to read or delete data from.|	SELECT * FROM students|
|IN	|Used with WHERE clause for multiple OR conditionals.|	SELECT * FROM students WHERE name IN(‘Scaler’, ‘Interviewbit’,‘Academy’)|
|ORDER BY|	Used to sort given data in Ascending or Descending order.|	SELECT * FROM student ORDER BY age ASC|
|SELECT DISTINCT|	Works in the same war as SELECT, except that only unique values are included in the results.|	SELECT DISTINCT age from student|
|TOP|	Used in conjunction with SELECT to select a fixed number of records from a table.|SELECT TOP 5 * FROM students|
|VALUES|	Used along with the INSERT INTO keyword to add new values to a table.|INSERT INTO Customers (CustomerName, City, Country) VALUES (‘Cardinal’, ‘Stavanger’, ‘Norway’)|
|WHERE|	Filters given data based on some given condition.|	SELECT * FROM students WHERE age >= 18|
|UNIQUE|	Ensures that all values in a column are different.|	UNIQUE (ID)|
|UNION|	Used to combine the result-set of two or more SELECT statements.|	SELECT column_name(s) FROM Table1 UNION SELECT column_name(s) FROM Table2|
|UNION ALL|	Combines the result set of two or more SELECT statements(it allows duplicate values)|	SELECT City FROM table1 UNION ALL SELECT City FROM table2 ORDER BY City;|
|SELECT TOP|	Used to specify the number of records to return.|	SELECT TOP 3 * FROM Students|
|LIMIT|	Puts a restriction on how many rows are returned from a query.|	SELECT * FROM table1 LIMIT 3|
|UPDATE|	Modifies the existing records in a table.|	UPDATE Customers SET ContactName = ‘Scaler’, City = ‘India’ WHERE CustomerID = 1;|
|SET|	Used with UPDATE to specify which columns and values should be updated in a table.|	UPDATE Customers SET ContactName = ‘Scaler’, City= ‘India’ WHERE |CustomerID = 1|
|IS NULL|	Column values are tested for NULL values using this operator.|	SELECT CustomerName, ContactName, Address FROM Customers WHERE Address IS NULL|
|LIKE	|Used to search for a specified pattern in a column.|	SELECT * FROM Students WHERE Name LIKE ‘a%’|
|ROWNUM|	Returns a number indicating the order in which Oracle selects the row from a table or set of joined rows.|	SELECT * FROM Employees WHERE ROWNUM < 10;|
|GROUP BY|	Groups rows that have the same values into summary rows.|	SELECT COUNT(StudentID), State FROM Students GROUP BY State|
|HAVING	|Enables the user to specify conditions that filter which group results appear in the results.|	HAVING COUNT(CustomerID) > 5|



# clauses-in-SQL
