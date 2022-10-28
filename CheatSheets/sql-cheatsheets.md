---
title: SQL CheatSheet
description: The most commonly used sql queries are given here.
created: 2022-10-22
---

## Table of Contents

- [SQL CheatSheet for Developers](#sql-cheatsheet-for-developers)
- [Introduction-What-is-SQL?](#introduction-what-is-sql)
- [SQL-Features?](#sql-features)
- [Basic SQL](#basic-sql)
  - [Create Database and drop database](#create-database-and-drop-database)
  - [String Datatype](#string-datatype)
  - [Numeric Datatype:](#numeric-datatype)
  - [Date/Time Datatype:](#datetime-datatype)
- [Tables](#tables)
  - [Alter Table](#alter-table)
  - [Insert Table](#insert-table)
  - [Update Table](#update-table)
  - [Delete Table](#delete-table)
- [Important-Sql-Keywords](#important-sql-keywords)
- [clauses-in-SQL](#clauses-in-sql)
- [SQL-Operators](#sql-operators)
  - [Arithmetic Operators](#arithmetic-operators)
  - [Bitwise Operators](#bitwise-operators)
  - [Relational Operators](#relational-operators)
  - [Compound Operators](#compound-operators)
  - [Logical Operators](#logical-operators)
- [Function in sql](#function-in-sql)
  - [SQL Server Numeric Functions](#sql-server-numeric-functions)
  - [SQL Server Date Functions](#sql-server-date-functions)
  - [SQL Server Advanced Functions](#sql-server-advanced-functions)
- [Joins in SQL](#joins-in-sql)

# SQL CheatSheet for Developers

# Introduction-What-is-SQL?

> To get introduced to **SQL**, we first need to know about Databases and **Database Management Systems(DBMS)**. Data is basically a collection of facts related to some object. A **Database** is a collection of small units of data arranged in a systematic manner. A **Relational Database Management System** is a collection of tools that allows the users to **manipulate, organize and visualize** the contents of a database while following some standard rules that facilitate fast response between the database and the user side.

> After getting introduced to the concept of data, databases and **DBMS/RDBMS**, we can finally learn about SQL. SQL or **Structured Query Language** is basically the language that we (the user) use to communicate with the Databases and get our required interpretation of data out of it. It is used for **storing, manipulating and retrieving** data out of a database.

**[🔼Back to Top](#table-of-contents)**

# SQL-Features?

> The following functionalities can be performed on a database using SQL:

1. `Create a Database` or `Delete a Database`
2. `Create a table` or `Alter a table` or `Delete a table` from a ___Database___
3. `SELECT data from tables`
4. `INSERT data into tables`
5. `UPDATE data in tables`
6. `DELETE data from tables`
7. `Create Views in the database`
8. `Execute various aggregate functions`

**[🔼Back to Top](#table-of-contents)**

# Basic SQL

## Create Database and drop database

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| CREATE DATABASE| CREATE DATABASE database-name  | Used to create new SQL database in the server        |
| DROP DATABASE  | CREATE DATABASE database-name  | Used to drop the existing database   |

**[🔼Back to Top](#table-of-contents)**

## String Datatype

> The table below lists all the String datatype available in SQL, along with their descriptions:

|Datatype |	Description|
|---------|---------------|
| CHAR(size) |	A fixed-length string containing numbers, letters or special characters. Length may vary from 0-255.|
| VARCHAR(size)	|Variable-length string where the length may vary from 0-65535. Similar to CHAR.|
| TEXT(size)|	Can contain a string of size up to 65536 bytes. |
| TINY TEXT	|Can contain a string of up to 255 characters.|
| MEDIUM TEXT |	Can contain a string of up to 16777215 characters.|
| LONG TEXT|	Can contain a string of up to 4294967295 characters.|
| BINARY(size)|	Similar to CHAR() but stores binary byte strings.|
| VARBINARY(size)|	Similar to VARCHAR() but stores binary byte strings.|
| BLOB(size)|	Holds blobs up to 65536 bytes.|
| TINYBLOB|	It is used for Binary Large Objects and has a maximum size of 255bytes.|
| MEDIUMBLOB|	Holds blobs up to 16777215 bytes.|
| LONGBLOB	| Holds blobs upto 4294967295 bytes.|
| ENUM(val1,val2) |	String object that can have only 1 possible value from a list of size at most 65536 values in an ENUM list. If no value is inserted, a blank value is inserted.|
| SET(val1,val2,…)	|String object with 0 or more values, chosen from a list of possible values with a maximum limit of 64 values.|

**[🔼Back to Top](#table-of-contents)**

## Numeric Datatype:

> The table below lists all the Numeric Datatype in SQL along with their descriptions:

|Datatype	|Description|
|-------|-------------|
| BIT(size) |	Bit-value type, where size varies from 1 to 64. Default value: 1|
| INT(size)	|Integer with values in the signed range of -2147483648 to 2147483647 and values in the unsigned range of 0 to 4294967295.|
| TINYINT(size)	|Integer with values in the signed range of -128 to 127 and values in the unsigned range of 0 to 255.|
| SMALLINT(size)|	Integer with values in the signed range of -32768 to 32767 and values in the unsigned range of 0 to 65535.|
| MEDIUMINT(size)	|Integer with values in the signed range of -8388608 to 8388607 and values in the unsigned range of 0 to 16777215.|
| BIGINT(size) |	Integer with values in the signed range of 9223372036854775808 to 9223372036854775807 and values in the unsigned range of 0 to 18446744073709551615.|
| BOOLEAN	|Boolean values where 0 is considered as FALSE and non-zero values are considered TRUE.|
| FLOAT (p)	|The floating-point number is stored. If the precision parameter is set between 0 to 24, the type is FLOAT() else if it lies between 25 to 53, the datatype is DOUBLE().|
| DECIMAL(size,d) |	Decimal number with a number of digits before decimal place set by size parameter, and a number of digits after the decimal point set by d parameter. Default values: size = 10, d = 10. Maximum Values: size = 65, d = 30.|

**[🔼Back to Top](#table-of-contents)**

## Date/Time Datatype:

> The datatype available in SQL to handle Date/Time operations effectively are called the Date/Time datatype. <br /> The table listed below all the Date/Time variables in SQL along with their description:

|Datatype|	Description|
|-------|---------|
| DATE	|Stores date in YYYY-MM-DD format with dates in the range of ‘1000-01-01’ to ‘9999-12-31’.|
| TIME(fsp)	|Stores time in hh:mm:ss format with times in the range of ‘-838:59:59’ to ‘838:59:59’.|
| DATETIME(fsp)	|Stores a combination of date and time in YYYY-MM-DD and hh:mm:ss format, with values in the range of ‘1000-01-01 00:00:00’ to ‘9999-12-31 23:59:59’.|
| TIMESTAMP(fsp)	|It stores values relative to the Unix Epoch, basically a Unix Timestamp. Values lie in the range of ‘1970-01-01 00:00:01’ UTC to ‘2038-01-09 03:14:07’ UTC.|
| YEAR	|Stores values of years as a 4digit number format, with a range lying between -1901 to 2155.|

**[🔼Back to Top](#table-of-contents)**

# Tables

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| CREATE TABLE| CREATE TABLE table_name (column1 datatype,column2 datatype,column3 datatype)  | Used to create new table        |
| DROP DATABASE  | CREATE DATABASE database-name  | Used to drop the existing database   |
|TRUNCATE TABLE|TRUNCATE TABLE table_name|used to delete the data inside a table, but not the table itself.|

**[🔼Back to Top](#table-of-contents)**

## Alter Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| ALTER TABLE ADD| ALTER TABLE table_name ADD column_name datatype  | Used to add column in existing table        |
| ALTER TABLE DROP  | ALTER TABLE table_name DROP COLUMN column_name  | Used to drop column in existing table   |
| ALTER TABLE MODIFY|ALTER TABLE table_name MODIFY COLUMN column_name datatype |Used to modify column in existing table |

**[🔼Back to Top](#table-of-contents)**

## Insert Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| INSERT INTO| INSERT INTO table_name (column1, column2, column3, ...) VALUES (value1, value2, value3, ...); | Used to insert data for particular columnn to add new records into  existing table        |
| INSERT INTO  |INSERT INTO table_name VALUES (value1, value2, value3, ...);  | used to insert new record in existing table with all column  |

**[🔼Back to Top](#table-of-contents)**


## Update Table

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| UPDATE| UPDATE table_name SET column1 = value1, column2 = value2, ... WHERE condition;  | Used to update data for particular row for existing records in existing table        |
| UPDATE| UPDATE table_name SET column1 = value1, column2 = value2, ... ;| Used to update data for all row exist in existing table        |

**[🔼Back to Top](#table-of-contents)**


## Delete Table 

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| DELETE|DELETE FROM table_name WHERE condition;  | Used to delete data for particular row for existing records in existing table        |
| DELETE| DELETE FROM table_name;| Used to delete data for all row exist in existing table        |

**[🔼Back to Top](#table-of-contents)**


# Important-Sql-Keywords

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

**[🔼Back to Top](#table-of-contents)**



# clauses-in-SQL


|Name|	Description|	Example|
|-------|-------|-------|
|WHERE|	Used to select data from the database based on some conditions.|	SELECT * from Employee WHERE age >= 18;|
|AND |	Used to combine 2 or more conditions and returns true if all the conditions are True.|	SELECT * from Employee WHERE age >= 18 AND salary >= 45000 ;|
|OR |	Similar to AND but returns true if any of the conditions are True.|	Select * from Employee where salary >= 45000 OR age >= 18|
|LIKE |	Used to search for a specified pattern in a column.|	SELECT * FROM Students WHERE Name LIKE ‘a%’;|
|LIMIT|	Puts a restriction on how many rows are returned from a query.|	SELECT * FROM table1 LIMIT 3;|
|ORDER BY|	Used to sort given data in Ascending or Descending order.|	SELECT * FROM student ORDER BY age ASC|
|GROUP BY|	Groups rows that have the same values into summary rows.|	SELECT COUNT(StudentID), State FROM Students GROUP BY State;|
|HAVING	|It performs the same as the WHERE clause but can also be used with aggregate functions.|	SELECT COUNT(ID), AGE FROM Students GROUP BY AGE HAVING COUNT(ID) > 5;|

**[🔼Back to Top](#table-of-contents)**

 # SQL-Operators
 
 There are 3 main types of operators: Arithmetic, Comparision and Logical operators, each of which will be described below.
 
## Arithmetic Operators

Arithmetic Operators allows the user to perform arithmetic operations in SQL. The table below shows the list of arithmetic operators available in SQL:

|Operator|	Description|
|-----|-------|
|+|	Addition|
|-|	Subtraction| 
|* |	Multiplication|
| / |	Division|
| % |	Modulo|

**[🔼Back to Top](#table-of-contents)**

## Bitwise Operators

Bitwise operators are used to performing Bit manipulation operations in SQL. The table below shows the list of bitwise operators available in SQL:

|Operator|	Description|
|---------|----------|
|&|	Bitwise AND |
| ![image](https://user-images.githubusercontent.com/47249568/197326193-77622f96-20cd-4f8f-b4b6-997fb54b2d69.png)|	Bitwise OR|
|^|	Bitwise XOR|

**[🔼Back to Top](#table-of-contents)**

## Relational Operators

Relational operators are used to performing relational expressions in SQL, i.e those expressions whose value either result in true or false. The table below shows the list of relational operators available in SQL:

|Operator|	Description|
|---------|---------|
|=|	Equal to|
|>|	Greater than|
|<|	Less than|
|>=|	Greater than or equal to|
|<=|	Less than or equal to|
|<>|	Not equal to|

**[🔼Back to Top](#table-of-contents)**

## Compound Operators

Compound operators are basically a combination of 2 or more arithmetic or relational operator, which can be used as a shorthand while writing code. The table below shows the list of compound operators available in SQL:

|Operator|	Description|
|------|---------|
|+=|	Add equals|
|-=|	Subtract equals|
|*=|	Multiply equals|
|/=|	Divide equals|
|%=|	Modulo equals|
|&=|	AND equals|
| ![image](https://user-images.githubusercontent.com/47249568/197326390-7087561c-34d3-450e-aacb-0282cfd17922.png)= |	OR equals|
|^=|	XOR equals|

**[🔼Back to Top](#table-of-contents)**

## Logical Operators

Logical operators are used to combining 2 or more relational statements into 1 compound statement whose truth value is evaluated as a whole. The table below shows the SQL logical operators with their description:

|Operator|	Description|
|---------|-----------|
|ALL|	Returns True if all subqueries meet the given condition.|
|AND|	Returns True if all the conditions turn out to be true|
|ANY|	True if any of the subqueries meet the given condition|
|BETWEEN|	True if the operand lies within the range of the conditions|
|EXISTS	|True if the subquery returns one or more records|
|IN|	Returns True if the operands to at least one of the operands in a given list of expressions|
|LIKE|	Return True if the operand and some given pattern match.|
|NOT|	Displays some record if the set of given conditions is False|
|OR|	Returns True if any of the conditions turn out to be True|
|SOME|	Returns True if any of the Subqueries meet the given condition.|

**[🔼Back to Top](#table-of-contents)**

# Function in sql

## SQL Server Numeric Functions

The table below lists some of the Numeric functions in SQL with their description:

|Name|	Description|
|------|-------|
|ABS|	Returns the absolute value of a number.|
|ASIN|	Returns arc sine value of a number.|
|AVG|	Returns average value of an expression.|
|COUNT|	Counts the number of records returned by a SELECT query.|
|EXP|	Returns e raised to the power of a number.|
|FLOOR|	Returns the greatest integer <= the number.|
|RAND|	Returns a random number.|
|SIGN|	Returns the sign of a number.|
|SQRT|	Returns the square root of a number.|
|SUM|	Returns the sum of a set of values.|

**[🔼Back to Top](#table-of-contents)**

## SQL Server Date Functions

The table below lists some of the Date functions in SQL with their description:

|Name|	Description|
|----|------|
|CURRENT_TIMESTAMP|	Returns current date and time.|
|DATEADD|	Adds a date/time interval to date and returns the new date.|
|DATENAME|	Returns a specified part of a date(as a string).|
|DATEPART|	Returns a specified part of a date(as an integer).|
|DAY|	Returns the day of the month for a specified date.|
|GETDATE|	Returns the current date and time from the database.|

**[🔼Back to Top](#table-of-contents)**

## SQL Server Advanced Functions

The table below lists some of the Advanced functions in SQL with their description:

|Name|	Description|
|------|---------|
|CAST|	Typecasts a value into specified datatype.|
|CONVERT|	Converts a value into a specified datatype.|
|IIF|	Return a value if a condition evaluates to True, else some other value.|
|ISNULL|	Return a specified value if the expression is NULL, else returns the expression.|
|ISNUMERIC|	Checks if an expression is numeric or not.|
|SYSTEM_USER|	Returns the login name for the current user|
|USER_NAME|	Returns the database user name based on the specified id.|

**[🔼Back to Top](#table-of-contents)**

# Joins in SQL

| COMMAND  | SYNTAX | DESCRIPTION |
| ------------- | ------------- |--------|
| INNER JOIN| SELECT column_name(s) FROM table1 INNER JOIN table2 ON table1.column_name = table2.column_name;| selects records that have matching values in both tables.       |
| LEFT JOIN| SELECT column_name(s) FROM table1 LEFT JOIN table2 ON table1.column_name = table2.column_name;| returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.|
|RIGHT JOIN|SELECT column_name(s) FROM table1 RIGHT JOIN table2 ON table1.column_name = table2.column_name;|returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.|
|FULL JOIN|SELECT column_name(s) FROM table1 FULL OUTER JOIN table2 ON table1.column_name = table2.column_name WHERE condition;|returns all records when there is a match in left (table1) or right (table2) table records.|
|SELF JOIN |SELECT column_name(s) FROM table1 T1, table1 T2 WHERE condition;|A self join is a regular join, but the table is joined with itself.|

**[🔼Back to Top](#table-of-contents)**

