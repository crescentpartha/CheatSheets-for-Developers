---
title: C Programming language
description: C Programming language cheatsheet contains useful code syntax with examples which is handy while coding.
created: 2020-04-25
updated: 2022-10-20
---

## Basics

* `scanf("%d", &x);` -- read value into the variable x from input stream
* `printf("%d",x);` -- printf value to the output stream
* `gets(str);` -- reads a line from input stream into a variable
* `scanf("%[^\n]",s);` --reads a line from input using scanf only

### Sample C program

```c
#include <stdio.h>    
int main() {    
    printf("Hello World!!");    
    return 0;   
}  
```
* `#include` is a keyword which is used to include header files like : `<stdlib.h>` and `<stdio.h>`. 
* `<stdio.h>` library file is used to read the data from terminal and to display the data on terminal. It has several in-built functions like printf(), scanf() etc.
* `main()` function is the entry point of any C program.
* `printf and scanf` are inbuilt library functions which are used for input and output in C language. They are defined in `stdio.h` header file.
* `return 0` is used to terminate the main() function and returns the value 0
* `//` -- single line comment
* `/* comments */` -- Multi line comment

## Data types

| Types | Data-type|
|----|----|
|Basic | bool, void, int/long, long long, char, float, double|
|Derived | array, pointer, structure, union|
|Enumeration | enum|
|Void |	void|

### 1. Basic Data types
| Data type | Description | Range | Memory Size| Format specifier|
|----|----|----|----|----|
| int| used to store whole numbers|-2,147,483,648 to 2,147,483,647|4 bytes| %d|
|unsigned int| used to store non-negative whole numbers|0 to 4,294,967,295|4 bytes| %u|
|short int| used to store whole numbers|-32,768 to 32,767| 2 bytes|%hd|
|unsigned short int| used to store non-negative whole numbers|0 to 65535| 2 bytes|%hu|
|long int| used to store whole numbers|	-2,147,483,648 to 2,147,483,647| 4 bytes|%ld|
|unsigned long int| used to store non-negative whole numbers|0 to 4,294,967,295 | 4 bytes|%lu|
|long long int| used to store whole numbers | -(2^63) to (2^63)-1 | 8 bytes|%lld|
|unsigned long long int| used to store non-negative whole numbers|0 to (2^64)| 4 bytes|%llu|
|float| used to store fractional numbers|6 to 7 decimal digits| 4 bytes|%f|
|double| used to store fractional numbers|15 decimal digits| 8 bytes|%lf|
|char|used to store a single character|one character|1 bytes|%c|

### 2. Derived Data types

Arrays:
```c
data-type array-name[size];
```
Pointers:

```c
datatype *pointername;
```
Structures: 

```c
struct structure_name {

   member definition;
   member definition;
   ...
   member definition;
} [one or more structure variables]; 

struct structure_name variable name;
```

### 3. Enumeration Data types non-negative

```c
enum name{constant1, constant2, constant3, ....... };
```
### 4. Void Data types

Void specifies that there is no return value. Generally used when function returns no value, pointer with type as void represents the address of an object but not it's type.

## Variables

### Syntax:
```c
data-type variable-name = value;
```
### Example:
```c
int x = 10; // declaring int variable and assigning value 10 to it
char grade = 'A'; // declaring char variable and assigning value A to it
```
## Literals
|Literal | Example|
|----|----|
|Integer Literal- decimal|255|
|Integer Literal- octal|0377|
|Integer Literal- hexadecimal|0xFF|
|Float point Literal|53.0f, 79.02|
|Character literals| 'a', '1'|
|String literals| "OneCompiler", "Foo"|

### Escape sequences
|Escape sequence| Description|
|----|----|
|\n	| New line|
|\r	| Carriage Return|
|\?	| Question mark|
|\t	| Horizontal tab|
|\v	| Vertical tab|
|\f	|Form feed|
|\\	| Backslash|
|\'	| Single quotation|
|\"	| Double quotation|
|\0 | Null character|
|\b	|Back space|
|\a	|Alarm or Beep|
|\nnn	|Octal Number|
|\xhh	|hexadecimal Number|

## Arrays

### One dimentional Array:

```c
data-type array-name[size];
```
### Example
```c
int a[5] = {1,2,3,4,5};
```

### Two dimensional array:

```c
data-type array-name[size][size];
```
### Example
```c
int a[2][3] = {
                {1,2,3},
                {4,5,6}
              };
```
## Operators

| Operator type | Description|
|----|-----|
| Arithmetic Operators|+ , - , * , / , %|
| Comparison Operators| < , > , <= , >=, != , ==|
| Bitwise Operators| & , ^ , \|, <<, >> |
| Logical Operators| && , `\|\|`, ! |
| Assignment Operators|= , += , -= , *= , /= , %=, <<=, >>=, &=, ^=, `\|=` |
| Ternary Operators| ? : |
| sizeof operators| sizeof() |


## Keywords(reserved words)

```c
auto         double      int        struct
break        else        long       switch
case         enum        register   typedef
char         extern      return     union
const        float       short      unsigned
continue     for         signed     void
default      goto        sizeof     volatile
do           if          static     while
alignas      nullptr     typeof     alignof
```
## Identifiers

Identifiers are user defined names for variables, functions and arrays.

### Rules:
* They must be less than or equal to 31 characters.
* No special characters.
* Must start with a letter or under score.
* Can contain letters, digits, or underscore only.

## Strings

Strings are an array of characters ended with null character. Enclosed in double quotes.

Declaration
```c
    char str[]="onecompiler";
```


| Function | Description| Example|
|----|----|---|
| gets() | It allows you to enter multi-word string | `gets("string")`|
| puts() | It is used to show string output | `puts("string")`|
| strlen() | It is used to calculate the length of the string | `strlen(string_name)`|
| strcpy() | It is used to copy the content of second-string into the first string passed to it | `strcpy(destination, source)`|
| strcat() |It is used to concatenate two strings | ` strcat(first_string, second_string)`|
| strcmp() | It is used to compare two strings | `strcmp(first_string, second_string)`|
| strrev() | It is used to return reverse of a string | `strrev("string")` |
| strupr() | It return string characters in uppercase | `strupr("string")` |
| strlwr() | It return string characters in lowercase | `strlwr("string")` |
| strcasecmp() | It compares two strings without comparing the sensitivity of the case | `strcasecmp(string1 , string2)` |
| strncat() | It concatenates n characters of one string to another string | `strncat(destination , source, size)` |
| strstr() | It stores the value in a pointer variable and takes two strings as input | `strstr(string1 , string2)` |

## Constants

Constants are the fixed values. They can be declared in two ways as shown below:

``` c
const datatype <constant-name> = <constant-value>;
```
```c
#define <constant-name> <constant-value>
```
## Special characters
* `{}` : specifies start and end of code blocks
* `[]` : used for arrays
* `()` : used for functions
* `,` : used to seperate variables, constants etc
* `*` : used for pointers
* `#` : used as a macro processor.

## Conditional Statements

### 1. If
```c
if(conditional-expression)
{
    //code
}
```
### 2. If-else

```c
if(conditional-expression)
{
    //code
} else {
    //code
}
```
### 3. If-else-if ladder

```c
if(conditional-expression-1)
{
    //code
} else if(conditional-expression-2) {
    //code
} else if(conditional-expression-3) {
    //code
}
....
else {
    //code
}
```
### 4. Switch

```c
switch(conditional-expression){    
case value1:    
 //code    
 break;  //optional  
case value2:    
 //code    
 break;  //optional  
...    
    
default:     
 //code to be executed when all the above cases are not matched;    
} 
```
## Loops

### 1. For
```c
for(Initialization; Condition; Increment/decrement){  
//code  
} 
```
### 2. While
```c
while (condition){  
//code 
}  
```
### 3. Do-While
```c
do {  
//code 
} while (condition); 
```

## Functions

Function is a sub-routine which contains set of statements.

```c
// declaring a function
return_type function_name(parameters);

// defining a function
return_type function_name(parameters){  
//code
}

// calling a function
function_name (parameters)
```

## Pointers

Pointer is a variable which holds the memory information(address) of another variable of same data type.

```c
datatype *pointername;
```
### Example
```c
int x = 10, *ptr;

/*ptr = x; // Error because ptr is adress and x is value
*ptr = &x;  // Error because x is adress and ptr is value */

ptr = &x; // valid because &x and ptr are addresses
*ptr = x; // valid because both x and *ptr values 

int a[10];
ptr = a;  // since a is the address of the first element in array (a[0])
ptr++;    // pointer points to next array element (a[1])
```

## Types of Pointers
| Serial Number |Pointer|Description|
|----|----|---|
| 1 | Null Pointer | `We can create a null pointer by assigning the null value at the time when we are declaring the pointer.It always contains the value 0`|
| 2 | Void Pointer | `This pointer has no associated data-type with it. A void pointer can hold addresses of any data-type and can be typecasted to another.It is created by using the keyword void`|
| 3 | Wild Pointer | `They are also called as uninitialised pointers.They are called so because they point to some arbitary memory location that is randomly alloted and the program can misbehave badly.This type of pointer is not efficient.`|
| 4 | Dangling Pointer | `The pointers that are pointing to deallocated memory or deleted memory block are known as Dangling pointers.They can raise an error because they point to a deallocated memory block.`|



## Structures

Structure is a user-defined data type where it allows you to combine data of different data types.

```c
struct structure_name {

   member definition;
   member definition;
   ...
   member definition;
} [one or more structure variables]; 

struct structure_name variable name; //declaring structure variables
```

## Unions

Union is a user-defined datatype similar to structs which allows to store different data types in the same memory location. In Unnions, one member can contain a value at any given time.

```c
union union_name {
   member definition;
   member definition;
   ...
   member definition;
} [one or more union variables];  

union union_name variable name; // Declaring Union Variables
```

## File handling

File operations like create, update, read, and deleting files which are stored on the local file system can be performed in C.

```c
FILE *fptr; //declaring a pointer of type File
fptr = fopen("filename",mode); //opening a file
fscanf(fptr, "format specifier", data); //read a file
fprintf(fptr, "format specifier", data); //write a file
fclose(fptr);
```

|Mode | Description|
|----|----|
|r|	Opens for reading.|
|rb| Opens for reading in binary mode.|
|r+| Opens for both reading and writing.|
|w|	Opens for writing. |
|wb| Opens for writing in binary mode.|
|a|	Opens for append. |
|ab| Opens for append in binary mode.|
|w+| Opens for both reading and writing.|
|wb+| Opens for both reading and writing in binary mode.|
|rb+| Opens for both reading and writing in binary mode.|
|a+| Opens for both reading and appending.|
|ab+| Opens for both reading and appending in binary mode.|


## Dynamic Memory Allocation

A set of functions for dynamic memory allocation from the heap. These methods are used to use the dynamic memory which makes our C programs more efficient


| Function | Description| Example|
|----|----|---|
| malloc() | Stands for 'Memory allocation' and reserves a block of memory with the given amount of bytes. | `ptr = (castType*) malloc(size)`|
| calloc() | Stands for 'Contiguous allocation' and reserves n blocks of memory with the given amount of bytes. | `ptr = (castType*)calloc(n, size)`|
| free | It is used to free the allocated memory. | `free(ptr)`|
| realloc() | If the allocated memory is insufficient, then we can change the size of previously allocated memory using this function for efficiency purposes | `ptr = realloc(ptr, x)`|


## Header Files

| Header Files | Description|
|----|----|
|stdio.h | Input/Output functions|
|conio.h | Console Input/Output functions|
|stdlib.h | General utility functions|
|math.h | Mathematics functions|
|string.h | String functions|
|ctype.h | Character handling functions|
|time.h | Date and time functions|
|float.h | Limits of float types|
|limits.h | Size of basic types|
|wctype.h | Functions to determine the type contained in wide character data|

## Mathematical Functions
All functions defined under `<math.h>` header file.

| Function | Description|
|----|----|
| sin(a) | Computes sine of the double angle (in radians) |
| cos(a) | Computes cosine of the double angle (in radians) |
| tan(a) | Computes tangent of the double angle (in radians) |
| asine(a) | Computes principle inverse of the sine (in radians) |
| acos(a) | Computes principle inverse of the cosine (in radians) |
| atan(a) | Computes principle inverse of the tangent (in radians) |
| atan2(a) | Computes principle inverse of tan(y/x) in same quadrant as (x,y) |
| sqrt(x) | Computes square root of x |
| log(x) | Computes natural logarithm of x (to the base e) |
| log2(x) | Computes natural logarithm of x (to the base 2) |
| log10(x) | Computes natural logarithm of x (to the base 10) |
| exp(p) | Computes e to the power of p |
| exp2(p) | Computes 2 to the power of p |
| exp10(p) | Computes 10 to the power of p |
| pow(x,y) | Computes x to the power of y |
| ceil(x) | Computes smallest integer (returned as double) no less than x |
| floor(x) | Computes largest integer (returned as double) no greater than x |
| abs(x) | Computes the absolute value of x |

## Randomize Functions
All functions defined under `<stdlib.h>` header file. These randomized functions are pseudo-random (time-based random functions).

* `random()` : returns a random long
* `srandom(seed)` : seeds the random generator with a new random seed

## How To Compile in GCC

* `gcc prog.c` : compiles prog.c into a.out, run result with  `./a.out`.
* `gcc -o prog prog.c` : compiles prog.c into prog, run result with `./prog`.
* `gcc -g -o prog prog.c` : as above, but allows for debugging.

## use of fflush()

*used to clear the buffer
*used to accept the next string
