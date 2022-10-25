---
title: PHP CheatSheet
description: The most commonly used php concepts are given here.
created: 2022-10-23
---

## Table of Contents

- [PHP CheatSheet for Developers](#php-cheatsheet-for-developers)
  - [Escape Sequence](#escape-sequence)
  - [Operators](#operators)
    - [Arithmetic Operators](#arithmetic-operators)
    - [Comparison Operators](#comparison-operators)
    - [Logical	Operators](#logicaloperators)
    - [String Operators](#string-operators)
    - [Array Operators](#array-operators)
    - [Conditional Assignment Operators](#conditional-assignment-operators)
    - [Increment/Decrement Operators](#incrementdecrement-operators)
  - [Super global variable](#super-global-variable)
  - [Important keywords $_SERVER](#important-keywords-_server)
  - [Functions](#functions)
    - [Array Function](#array-function)
    - [PHP standard functions](#php-standard-functions)
    - [String function](#string-function)
    - [File function](#file-function)
  - [Read File](#read-file)
  - [Cookies and Session](#cookies-and-session)
  - [Most Important Function](#most-important-function)
    - [calender function](#calender-function)
    - [Date/time Function](#datetime-function)
    - [Filter Function](#filter-function)
    - [MySQLi  Function](#mysqli--function)
    - [PHP Regular Expression Functions](#php-regular-expression-functions)


# PHP CheatSheet for Developers

## Escape Sequence

| Command                | Description                                     |
| :--------------------: | :----------------------------------------------- |
| `// Comment Message` | This is a single-line comment |
| `$Title = "Title"` | Defining Variables |
| `\n` | New Line |
| `\r` | It inserts a carriage return in the text at this point. |
| `\t` | It gives a horizontal tab space |
| `\v` | It gives a vertical tab space |
| `\\` | It adds a backslash |
| `\$` | Print the next character as a dollar, not as part of a variable |
| `\'` | Print the next character as a double quote, not a string closer |
| `\"` | Print the next character as a double quote, not a string closer |

**[🔼Back to Top](#table-of-contents)**

## Operators

### Arithmetic Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`+`|	Addition|	$x + $y|
|`-`|	Subtraction|	$x - $y|
|`*` |	Multiplication|	$x * $y |
| `/` |	Division|	$x / $y|	
|`%`|	Modulus|	$x % $y|	
|` ** `|	Exponentiation |	$x ** $y	|	

**[🔼Back to Top](#table-of-contents)**

### Comparison Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`==`|	Equal|	$x == $y|	
|`===`|	Identical|	$x === $y|
| `!= `| 	Not equal|	$x != $y|	
| `<>` |	Not equal |	$x <> $y	|	
|`!==` |	Not identical|	$x !== $y |	
|`>`|	Greater than|	$x > $y|	
|`<`|	Less than|	$x < $y|	
|`>=`|	Greater than or equal to|	$x >= $y|	
|`<=`|	Less than or equal to|	$x <= $y|	
|`<=>`|	Spaceship|	$x <=> $y	|

**[🔼Back to Top](#table-of-contents)**

### Logical	Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`and`|	And|	$x and $y|
|`or`	|Or|	$x or $y	|
|`xor`|	Xor|	$x xor $y	|
|`&&`|	And|	$x && $y|	
| `\|` | Or | $x \| $y |
|`!`	|Not	|!$x |	

**[🔼Back to Top](#table-of-contents)**

### String Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`.`|	Concatenation|	$txt1 . $txt2	|
|`.=`|	Concatenation assignment|	$txt1 .= $txt2|	

**[🔼Back to Top](#table-of-contents)**

### Array Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`+`|	Union|	$x + $y|	
|`==`|	Equality|	$x == $y	|
|`===`|	Identity|	$x === $y |
|`!=`|	Inequality|	$x != $y	|
|`<>`|	Inequality|	$x <> $y	|
|`!==`|	Non-identity|	$x !== $y	|	

**[🔼Back to Top](#table-of-contents)**

### Conditional Assignment Operators

|operator|name |syntax|
|:--------:|:------:|:-----:|
|`?:	`|Ternary|	$x = expr1 ? expr2 : expr3|
|`??`|	Null coalescing|	$x = expr1 ?? expr2|

**[🔼Back to Top](#table-of-contents)**

### Increment/Decrement Operators

|operator|name |description|
|:--------:|:------:|:-----:|
|`++$x`|	Pre-increment|	Increments $x by one|
|`$x++`|	Post-increment|	Returns $x, then increments $x by one	|
|`--$x`|	Pre-decrement	|Decrements $x by one, then returns $x|
|`$x--`	|Post-decrement	|Returns $x, then decrements $x by one	|	

**[🔼Back to Top](#table-of-contents)**

## Super global variable

|keyword|description|
|:--------:|:------|
|`$GLOBALS`| used to access global variables from anywhere in the PHP script |
|`$_SERVER`|holds information about headers, paths, and script locations|
|` $_REQUEST`|used to collect data after submitting an HTML form|
|`$_POST`|used to collect form data after submitting an HTML form with method="post"|
|`$_GET`|used to collect form data after submitting an HTML form with method="get"|
|`$_FILES`| an associative array containing items uploaded via HTTP POST method|
|`$_ENV`|An associative array of variables passed to the current script via the environment method.|
|`$_COOKIE`|etrieve the value of the cookie|
|`$_SESSION`|A session is a way to store information (in variables) to be used across multiple pages.|

**[🔼Back to Top](#table-of-contents)**

## Important keywords $_SERVER

|Element/Code|	Description|
|:--------:|:------|
|`$_SERVER['PHP_SELF']`|	Returns the filename of the currently executing script|
|`$_SERVER['GATEWAY_INTERFACE']`	|Returns the version of the Common Gateway Interface (CGI) the server is using|
|`$_SERVER['SERVER_ADDR']`	|Returns the IP address of the host server|
|`$_SERVER['SERVER_NAME']`	|Returns the name of the host server (such as www.w3schools.com)|
|`$_SERVER['SERVER_SOFTWARE']`	|Returns the server identification string (such as Apache/2.2.24)|
|`$_SERVER['SERVER_PROTOCOL']`	|Returns the name and revision of the information protocol (such as HTTP/1.1)|
|`$_SERVER['REQUEST_METHOD']`	|Returns the request method used to access the page (such as POST)|
|`$_SERVER['REQUEST_TIME']`	|Returns the timestamp of the start of the request (such as 1377687496)|
|`$_SERVER['QUERY_STRING']`	|Returns the query string if the page is accessed via a query string|
|`$_SERVER['HTTP_ACCEPT']`	|Returns the Accept header from the current request|
|`$_SERVER['HTTP_ACCEPT_CHARSET']`|	Returns the Accept_Charset header from the current request (such as utf-8,ISO-8859-1)|
|`$_SERVER['HTTP_HOST']`	|Returns the Host header from the current request|
|`$_SERVER['HTTP_REFERER']`|	Returns the complete URL of the current page (not reliable because not all user-agents support it)|
|`$_SERVER['HTTPS']`	|Is the script queried through a secure HTTP protocol|
|`$_SERVER['REMOTE_ADDR']`|	Returns the IP address from where the user is viewing the current page|
|`$_SERVER['REMOTE_HOST']	`|Returns the Host name from where the user is viewing the current page|
|`$_SERVER['REMOTE_PORT']	`|Returns the port being used on the user's machine to communicate with the web server|
|`$_SERVER['SCRIPT_FILENAME']`|	Returns the absolute pathname of the currently executing script|
|`$_SERVER['SERVER_ADMIN']`	|Returns the value given to the SERVER_ADMIN directive in the web server configuration file (if your script runs on a virtual host, it will be the value defined for that virtual host) (such as someone@hools.com)|
|`$_SERVER['SERVER_PORT']	`|Returns the port on the server machine being used by the web server for communication (such as 80)|
|`$_SERVER['SERVER_SIGNATURE']`	|Returns the server version and virtual host name which are added to server-generated pages|
|`$_SERVER['PATH_TRANSLATED']`	|Returns the file system based path to the current script|
|`$_SERVER['SCRIPT_NAME']`	|Returns the path of the current script|
|`$_SERVER['SCRIPT_URI']`	|Returns the URI of the current page|

**[🔼Back to Top](#table-of-contents)**

## Functions

### Array Function 

|Function |Description|
|:--------:|:------|
|`count(arr)`| Returns the length of an array arr|
|`print_r(arr)`| Prints the arr’s contents|
|`array_pop(arr)`| Pops (removes) an element off the end of the array arr|
|`array_shift(arr)`| Shifts (removes) an element off the beginning of the array arr|
|`array_push(arr, el)`| Pushes (adds) one or more elements onto the end of the array arr|
|`array_unshift(arr, el)`| Prepends one or more elements to the beginning of the array arr|
|`sort(arr)`| Sorts the array arr|
|`array_reverse(arr)`| Returns an array with elements of arr in reverse order|
|`in_array(el, arr)`| Returns whether a value el exists in an array arr|
|`list(a, b, ...)` |Assigns variables as if they were an array|
|`implode(glue, pieces)`| Joins array elements (pieces) with a string (glue)|
|`array_rand(arr)`| Randomly selects a random entry from the array and returns the key(or keys) of the random entries|

**[🔼Back to Top](#table-of-contents)**

### PHP standard functions

|Function| Description|
|:--------:|:------|
|`isset(el)` |Will return false if el has been assigned the constant NULL, el has not been set to any value yet (undefined) el has been deleted using the unset function|
|`print str` <br /> or <br /> `echo str` | Prints str |
|`time()`| Returns the current time in seconds|
|`date(format, time)`| Converts an optional time in seconds to a date based on format|
|`mt_rand(min, max)`| Returns a random integer between min and max (inclusive)|
|`header(string)`| Sends a raw HTTP header. |
|`die(message)`| Ends execution and sends back optional message|
|`include "path"` |Includes and evaluates the specified file path such as "hidden/config.php"|

**[🔼Back to Top](#table-of-contents)**

### String function

|Function| Description|
|:--------:|:------|
|`strlen(s)`| Returns the length of a string s|
|`strpos(str, substr)`| Returns the position of the first occurrence of substr in str, or FALSE if not found|
|`substr(s, start,len)`| Returns a substring of s starting at start and up to len characters in length. If s is less than start characters long, FALSE will be returned|
|`trim(s)`| Strips whitespace characters from both ends of a string s|
|`strtolower(s)`| Returns a lowercase version of s|
|`strtoupper(s)` |Returns an uppercase version of s|
|`explode(delimiter,s)`| Returns an array of substrings of s split by delimiter|

**[🔼Back to Top](#table-of-contents)**

### File function

|Function| Description|
|:--------:|:------|
|`file(path, [int flags = 0])`| Reads entire file path into an array. Optional flags parameter can be passed in such as FILE_IGNORE_NEW_LINES or FILE_SKIP_EMPTY_LINES|
|`file_exists(path) `|Returns whether a file or directory path exists|
|`file_get_contents(path) `|Reads entire file path into a string|
|`file_put_contents(path, data)`| Writes a string data to a file path|
|`scandir(path) `|Returns an array of all files and directories inside the specified path including . and ..|
|`glob(pattern) `|Returns an array of path names matching pattern|
|`basename(path)`|Given a filename path, this function will strip any leading directory from a file path and return just the filename|

**[🔼Back to Top](#table-of-contents)**

## Read File

|Modes	|Description|pointer|
|:--------:|:------|:-------|
|`r`|	Open a file for read only.| File pointer starts at the beginning of the file|
|`w`|	Open a file for write only.| Erases the contents of the file or creates a new file if it doesn't exist. File pointer starts at the beginning of the file|
|`a`|	Open a file for write only.| The existing data in file is preserved. File pointer starts at the end of the file. Creates a new file if the file doesn't exist|
|`x`|	Creates a new file for write only.| Returns FALSE and an error if file already exists|
|`r+`|	Open a file for read/write.| File pointer starts at the beginning of the file|
|`w+`|	Open a file for read/write.| Erases the contents of the file or creates a new file if it doesn't exist. File pointer starts at the beginning of the file|
|`a+`|	Open a file for read/write.| The existing data in file is preserved. File pointer starts at the end of the file. Creates a new file if the file doesn't exist|
|`x+`|	Creates a new file for read/write.| Returns FALSE and an error if file already exists|

**[🔼Back to Top](#table-of-contents)**

## Cookies and Session

|keyword	|Description
|:--------:|:------|
|`setcookie(name, value)`|used to set cookie with HTTP response|
|`$_COOKIE`|etrieve the value of the cookie|
|`session_start()`|A session is started |
|`$_SESSION`|Session variables are set with the PHP global variable|
|`session_unset() and session_destroy()`|To remove all global session variables and destroy the session|

**[🔼Back to Top](#table-of-contents)**

## Most Important Function  

### calender function

|Function|	Description|
|:--------:|:------|
|`cal_days_in_month()`|	Returns the number of days in a month for a specified year and calendar|
|`cal_from_jd()`|	Converts a Julian Day Count into a date of a specified calendar|
|`cal_info()`|	Returns information about a specified calendar|
|`cal_to_jd()`|	Converts a date in a specified calendar to Julian Day Count|
|`easter_date()`|	Returns the Unix timestamp for midnight on Easter of a specified year|
|`easter_days()`|	Returns the number of days after March 21, that the Easter Day is in a specified year|
|`frenchtojd()`|	Converts a French Republican date to a Julian Day Count|
|`gregoriantojd()`|	Converts a Gregorian date to a Julian Day Count|
|`jddayofweek()`|	Returns the day of the week|
|`jdmonthname()`|	Returns a month name|
|`jdtofrench()`|	Converts a Julian Day Count to a French Republican date|
|`jdtogregorian()`|	Converts a Julian Day Count to a Gregorian date|
|`jdtojewish()`|	Converts a Julian Day Count to a Jewish date|
|`jdtojulian()`|	Converts a Julian Day Count to a Julian date|
|`jdtounix()`|	Converts Julian Day Count to Unix timestamp|
|`jewishtojd()`|	Converts a Jewish date to a Julian Day Count|
|`juliantojd()`|	Converts a Julian date to a Julian Day Count|
|`unixtojd()`|	Converts Unix timestamp to Julian Day Count|

**[🔼Back to Top](#table-of-contents)**

### Date/time Function

|Function|	Description|
|:--------:|:------|
|`checkdate()	`|Validates a Gregorian date|
|`date_add()`|	Adds days, months, years, hours, minutes, and seconds to a date|
|`date_create_from_format()	`|Returns a new DateTime object formatted according to a specified format|
|`date_create()`|Returns a new DateTime object|
|`date_date_set()`|	Sets a new date|
|`date_default_timezone_get()`|	Returns the default timezone used by all date/time functions|
|`date_default_timezone_set()`|	Sets the default timezone used by all date/time functions|
|`date_diff()`|	Returns the difference between two dates|
|`date_format()	`|Returns a date formatted according to a specified format|
|`date_get_last_errors()`|	Returns the warnings/errors found in a date string|
|`date_interval_create_from_date_string()`|	Sets up a DateInterval from the relative parts of the string|
|`date_interval_format()`|	Formats the interval|
|`date_isodate_set()`|	Sets the ISO date|
|`date_modify()`|	Modifies the timestamp|
|`date_offset_get()`|	Returns the timezone offset|
|`date_parse_from_format()`|	Returns an associative array with detailed info about a specified date, according to a specified format|
|`date_parse()`|	Returns an associative array with detailed info about a specified date|
|`date_sub()`|	Subtracts days, months, years, hours, minutes, and seconds from a date|
|`date_sun_info()`|	Returns an array containing info about sunset/sunrise and twilight begin/end, for a specified day and location|
|`date_sunrise()`|	Returns the sunrise time for a specified day and location|
|`date_sunset()	`|Returns the sunset time for a specified day and location|
|`date_time_set()	`|Sets the time|
|`date_timestamp_get()`|	Returns the Unix timestamp|
|`date_timestamp_set()`|	Sets the date and time based on a Unix timestamp|
|`date_timezone_get()	`|Returns the time zone of the given DateTime object|
|`date_timezone_set()`|	Sets the time zone for the DateTime object|
|`date()	`|Formats a local date and time|
|`getdate()	`|Returns date/time information of a timestamp or the current local date/time|
|`gettimeofday()`|	Returns the current time|
|`gmdate()`|	Formats a GMT/UTC date and time|
|`gmmktime()`|	Returns the Unix timestamp for a GMT date|
|`gmstrftime()`|	Formats a GMT/UTC date and time according to locale settings|
|`idate()	`|Formats a local time/date as integer|
|`localtime()`|	Returns the local time|
|`microtime()`|	Returns the current Unix timestamp with microseconds|
|`mktime()	`|Returns the Unix timestamp for a date|
|`strftime()`|	Formats a local time and/or date according to locale settings|
|`strptime()`|	Parses a time/date generated with strftime()|
|`strtotime()`|	Parses an English textual datetime into a Unix timestamp|
|`time()`|	Returns the current time as a Unix timestamp|
|`timezone_abbreviations_list()`|	Returns an associative array containing dst, offset, and the timezone name|
|`timezone_identifiers_list()`|	Returns an indexed array with all timezone identifiers|
|`timezone_location_get()`|	Returns location information for a specified timezone|
|`timezone_name_from_ abbr()`|	Returns the timezone name from abbreviation|
|`timezone_name_get()`|	Returns the name of the timezone|
|`timezone_offset_get()`|	Returns the timezone offset from GMT|
|`timezone_open()`|	Creates new DateTimeZone object|
|`timezone_transitions_get()`|	Returns all transitions for the timezone|
|`timezone_version_get()`|	Returns the version of the timezonedb|

**[🔼Back to Top](#table-of-contents)**

### Filter Function

|Function|	Description|
|:--------:|:------|
|`filter_has_var()`|	Checks whether a variable of a specified input type exist|
|`filter_id()`|	Returns the filter ID of a specified filter name|
|`filter_input()`|	Gets an external variable (e.g. from form input) and optionally filters it|
|`filter_input_array()`|	Gets external variables (e.g. from form input) and optionally filters them|
|`filter_list()`|	Returns a list of all supported filter names|
|`filter_var()`|	Filters a variable with a specified filter|
|`filter_var_array()`|	Gets multiple variables and filter them|

**[🔼Back to Top](#table-of-contents)**

### MySQLi  Function

|Function|	Description|
|:--------:|:------|
|`affected_rows()`|	Returns the number of affected rows in the previous MySQL operation|
|`autocommit()`|	Turns on or off auto-committing database modifications|
|`begin_transaction()`|	Starts a transaction|
|`change_user()`|	Changes the user of the specified database connection|
|`character_set_name()`|	Returns the default character set for the database connection|
|`close()`|	Closes a previously opened database connection|
|`commit()`|	Commits the current transaction|
|`connect()`|	Opens a new connection to the MySQL server|
|`connect_errno()`|	Returns the error code from the last connection error|
|`connect_error()`|	Returns the error description from the last connection error|
|`data_seek()`| Adjusts the result pointer to an arbitrary row in the result-set|
|`debug()`|	Performs debugging operations|
|`dump_debug_info()`|	Dumps debugging info into the log|
|`errno()`|	Returns the last error code for the most recent function call|
|`error()`|	Returns the last error description for the most recent function call|
|`error_list()`|	Returns a list of errors for the most recent function call|
|`fetch_all()`|	Fetches all result rows as an associative array, a numeric array, or both|
|`fetch_array()`|	Fetches a result row as an associative, a numeric array, or both|
|`fetch_assoc()`|	Fetches a result row as an associative array|
|`fetch_field()`|	Returns the next field in the result-set, as an object|
|`fetch_field_direct()`|	Returns meta-data for a single field in the result-set, as an object|
|`fetch_fields()`|	Returns an array of objects that represent the fields in a result-set|
|`fetch_lengths()`|	Returns the lengths of the columns of the current row in the result-set|
|`fetch_object()`|	Returns the current row of a result-set, as an object|
|`fetch_row()`|	Fetches one row from a result-set and returns it as an enumerated array|
|`field_count()`|	Returns the number of columns for the most recent query|
|`field_seek()`|	Sets the field cursor to the given field offset|
|`info()`|	Returns information about the last executed query|
|`init()`|	Initializes MySQLi and returns a resource for use with real_connect()|
|`insert_id()`|	Returns the auto-generated id from the last query|
|`kill()`|	Asks the server to kill a MySQL thread|
|`more_results()`|	Checks if there are more results from a multi query|
|`multi_query()`|	Performs one or more queries on the database|
|`next_result()`|	Prepares the next result-set from multi_query()|
|`options()`|	Sets extra connect options and affect behavior for a connection|
|`ping()`|	Pings a server connection, or tries to reconnect if the connection has gone down|
|`poll()`|	Polls connections|
|`prepare()`|	Prepares an SQL statement for execution|
|`query()`|	Performs a query against a database|
|`real_connect()`|	Opens a new connection to the MySQL server|
|`real_escape_string()`|	Escapes special characters in a string for use in an SQL statement|
|`real_query()`|	Executes a single SQL query|
|`reap_async_query()`|	Returns result from an async SQL query|
|`refresh()`|	Refreshes/flushes tables or caches, or resets the replication server information|
|`rollback()`|	Rolls back the current transaction for the database|
|`select_db()`|	Select the default database for database queries|
|`set_charset()`|	Sets the default client character set|
|`set_local_infile_default()`|	Unsets user defined handler for load local infile command|
|`set_local_infile_handler()`|	Set callback function for LOAD DATA LOCAL INFILE command|
|`sqlstate()`|	Returns the SQLSTATE error code for the error|
|`ssl_set()`|	Used to establish secure connections using SSL|
|`stat()`|	Returns the current system status|
|`stmt_init()`|	Initializes a statement and returns an object for use with stmt_prepare()|
|`store_result()`|	Transfers a result-set from the last query|
|`thread_id()`|	Returns the thread ID for the current connection|
|`thread_safe()`|	Returns whether the client library is compiled as thread-safe|
|`use_result()`|	Initiates the retrieval of a result-set from the last query executed|
|`warning_count()`|	Returns the number of warnings from the last query in the connection |

**[🔼Back to Top](#table-of-contents)**

### PHP Regular Expression Functions

|Function|	Description|
|:--------:|:------|
|`preg_filter()`|	Returns a string or an array with pattern matches replaced, but only if matches were found|
|`preg_grep()`|	Returns an array consisting only of elements from the input array which matched the pattern|
|`preg_last_error()`|	Returns an error code indicating the reason that the most recent regular expression call failed|
|`preg_match()`|	Finds the first match of a pattern in a string|
|`preg_match_all()`|	Finds all matches of a pattern in a string|
|`preg_replace()`|	Returns a string where matches of a pattern (or an array of patterns) are replaced with a substring (or an array of substrings) in a given string|
|`preg_replace_callback()`|	Given an expression and a callback, returns a string where all matches of the expression are replaced with the substring returned by the callback|
|`preg_replace_callback_array()`|	Given an array associating expressions with callbacks, returns a string where all matches of each expression are replaced with the substring returned by the callback|
|`preg_split()`|	Breaks a string into an array using matches of a regular expression as separators|
|`preg_quote()`|	Escapes characters that have a special meaning in regular expressions by putting a backslash in front of them|

**[🔼Back to Top](#table-of-contents)**
