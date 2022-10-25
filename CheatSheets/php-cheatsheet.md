## Table of Contents

- [PHP CheatSheet for Developers](#php-cheatsheet-for-developers)
  - [Escape Sequence](#escape-sequence)
  - [Operators](#operators)
  -  - [Operators](#operators)
  - [Super global variable](#super-global-variable)
  - [Important keywords $_SERVER](#Important-keywords)

# PHP CheatSheet for Developers

## Escape Sequence

| Command                | Description                                                                                                                               |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `// Comment Message` | This is a single-line comment |
| `$Title = "Title"` | Defining Variables|
| `\n` | New Line|
| `\r` | It inserts a carriage return in the text at this point.|
| `\t` | It gives a horizontal tab space|
| `\v` | It gives a vertical tab space|
| `\\` | It adds a backslash|
| `\$` | Print the next character as a dollar, not as part of a variable|
| `\'` | Print the next character as a double quote, not a string closer|
| `\"` | Print the next character as a double quote, not a string closer|

**[🔼Back to Top](#table-of-contents)**

## Operators

|operator|name |syntax|type|
|---------|------|-----|----|
|`+`|	Addition|	$x + $y|Arithmetic Operators|
|`-`|	Subtraction|	$x - $y|Arithmetic Operators|
|`*` |	Multiplication|	$x * $y |Arithmetic Operators|
| `/` |	Division|	$x / $y|Arithmetic Operators|	
|`%`|	Modulus|	$x % $y|	Arithmetic Operators|y	
|` ** `|	Exponentiation |	$x ** $y	|Arithmetic Operators|	
|`==`|	Equal|	$x == $y|Comparison Operators|	
|`===`|	Identical|	$x === $y|Comparison Operators|
| `!= `| 	Not equal|	$x != $y|Comparison Operators|	
| `<>` |	Not equal |	$x <> $y	|Comparison Operators|	
|`!==` |	Not identical|	$x !== $y |Comparison Operators|	
|`>`|	Greater than|	$x > $y|Comparison Operators|	
|`<`|	Less than|	$x < $y|Comparison Operators|	
|`>=`|	Greater than or equal to|	$x >= $y|Comparison Operators|	
|`<=`|	Less than or equal to|	$x <= $y|Comparison Operators|	
|`<=>`|	Spaceship|	$x <=> $y	|Comparison Operators|
|`and`|	And|	$x and $y|Logical	Operators|
|`or`	|Or|	$x or $y	|Logical	Operators|
|`xor`|	Xor|	$x xor $y	|Logical	Operators|
|`&&`|	And|	$x && $y|	Logical	Operators|
| ![image](https://user-images.githubusercontent.com/47249568/197706502-62d506bd-5596-4c5f-a1e3-7e58633c4139.png)	|Or|	$x ![image](https://user-images.githubusercontent.com/47249568/197706528-2bbe3369-5c51-4e1b-b295-c607f05bfa77.png) $y |Logical	Operators|	
|`!`	|Not	|!$x |	Logical	Operators|
|`.`|	Concatenation|	$txt1 . $txt2	|String Operators|
|`.=`|	Concatenation assignment|	$txt1 .= $txt2|	String Operators|
|`+`|	Union|	$x + $y|Array Operators|	
|`==`|	Equality|	$x == $y	|Array Operators|
|`===`|	Identity|	$x === $y |Array Operators|
|`!=`|	Inequality|	$x != $y	|Array Operators|
|`<>`|	Inequality|	$x <> $y	|Array Operators|
|`!==`|	Non-identity|	$x !== $y	|Array Operators|	
|`?:	`|Ternary|	$x = expr1 ? expr2 : expr3|	Conditional Assignment Operators|
|`??`|	Null coalescing|	$x = expr1 ?? expr2|	Conditional Assignment Operators|


|operator|name |description|type|
|---------|------|-----|----|
|`++$x`|	Pre-increment|	Increments $x by one |Increment|
|`$x++`|	Post-increment|	Returns $x, then increments $x by one	|Increment|
|`--$x`|	Pre-decrement	|Decrements $x by one, then returns $x|decrement|	
|`$x--`	|Post-decrement	|Returns $x, then decrements $x by one	|decrement|	


**[🔼Back to Top](#table-of-contents)**

## Super global variable

|keyword|description|
|---------|--------|
|`$GLOBALS`| used to access global variables from anywhere in the PHP script |
|`$_SERVER`|holds information about headers, paths, and script locations|
|` $_REQUEST`|used to collect data after submitting an HTML form|
|`$_POST`|used to collect form data after submitting an HTML form with method="post"|
|`$_GET`|used to collect form data after submitting an HTML form with method="get"|
|`$_FILES`| an associative array containing items uploaded via HTTP POST method|
|`$_ENV`|An associative array of variables passed to the current script via the environment method.|
|`$_COOKIE`|a small file that the server embeds on the user's computer|
|`$_SESSION`|A session is a way to store information (in variables) to be used across multiple pages.|

**[🔼Back to Top](#table-of-contents)**

## Important keywords $_SERVER

|Element/Code|	Description|
|----------|--------------|
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
