# contents
**1** [**Introduction: What is SQL?**](#Introduction-What-is-SQL?)

**2** [**SQL features?**](#SQL-Features?)

**3** [**Basic SQL**](#Basic-SQL?)

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

# 2 String Datatype


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
| DROP DATABASE  | CREATE DATABASE databasename  | Used to drop the existing database   |



