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

**[🔼Back to Top](#table-of-contents)**


