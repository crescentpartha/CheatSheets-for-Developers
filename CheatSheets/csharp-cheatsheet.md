---
title: C#
description: C# cheatsheet contains useful code syntax with examples which is handy while coding.
created: 2020-05-19
updated: 2021-12-19
---

## Basics

### Sample Program

```c#
using System;

namespace HelloWorld
{
	public class Program
	{
		public static void Main(string[] args)
		{
			Console.WriteLine("Hello, World!");
		}
	}
}
```
* **Using Keyword** : using keyword is used to include namespaces in the program. 
* **Namespace declaration** : Namespace is a container for classes and other namespaces. The `HelloWorld` namespace contains the class `Program`.
* **Public Class** : class is a container for data and methods, you are declaring `Program` as a class with public visibility.
* **Main** : Beginning of your program
* **Console.WriteLine** : Console is a class of the System namespace and WriteLine() is a method in it which is used to print text to the console.
* C# statements end with a semicolon `;`
* C# is Case-sensitive
* `//` : Single line Comment
* `/* */` : Multi Line Comments

## Data types

| Data type | Description                                               | Range                                                   | Memory Size           |
| ---       | ---                                                       | ---                                                     | ---                   |
| byte      | used to store unsigned integer                            | 0 to 255                                                | 1 byte                |
| sbyte     | used to store signed integer                              | -128 to 127                                             | 1 byte                |
| short     | used to store signed integers                             | -32,768 to 32,767                                       | 2 bytes               |
| int       | used to store signed integers                             | -2,147,483,648 to 2,147,483,647                         | 4 bytes               |
| long      | used to store signed integers                             | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | 8 bytes               |
| float     | used to store fractional numbers                          | 6 to 7 decimal digits                                   | 4 bytes               |
| double    | used to store fractional numbers                          | 15 decimal digits                                       | 8 bytes               |
| char      | used to store a single character enclosed in single quote | one character                                           | 2 bytes               |
| bool      | Boolean data type                                         |Stores either true or false                              | 1 bit                 |
| String    | Stores a sequence of characters enclosed in double quotes | Sequence of Characters                                  | 2 bytes per character |

## Variables

```c#
datatype variableName = value;
```
```c#
int x = 10; // declaring int variable and assigning value 10 to it
char grade = 'A'; // declaring char variable and assigning value A to it
```

## Constants

```c
const datatype variable-name = value;
```

## String functions
| Function name | Description|
|----|----|
|str.Length| to return the length of string str|
|+| to concatenate two strings|
|string.Concat(str1,str2)| to concatenate two strings str1 and str2|
|Copy(str1, str2)| To copy string str2 into string str1.|
|Compare(str1, str2)| returns 0 if str1 and str2 are the same and less than 0 if str1 < str2 and a positive number if str1 > str2|
|Join(str, String[])| concatenate all the elements of the given string array with the specified separator between each element.|
|Split(Char[])| splits a string into substrings based on the characters in an array|
|str.ToUpper()| converts the string to upper case|
|str.ToLower()| converts the string to lower case|
|ToString()| to return instance of a string|
|Trim()| removes all leading and trailing whitespaces from a given string|
|Clone()| returns a reference to this instance of String|
|Format()| it returns a formatted string|
|LastIndexOf()| it returns the last occurence of the string|
|Replace()| it replaces the specified string character with new character|
|Contains()| it checks whether a string contains substring|
|ToCharArray()| it converts a string to a character(char) array| 
|isEmpty()| it checks whether the string is empty or not and return true or false respectively| 
|startsWith("char")| it checks the string start with given character or not and return true or false respectively|
|endsWith("char")| it checks the string end with given character or not and return true or false respectively|
|charAt(int)| it returns the character at the specified index in a string|
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
while(condition){  
//code 
}  
```
### 3. Do-While
```c
do{  
//code 
} while(condition); 
```
## Arrays
```c#
data-type[] array-name; //declaration
array-name = new data-type[size]{ array-elements }; //initialization
```
\[or\]

```c#
data-type[] array-name =  new data-type[size]{ array-elements }; //declaration and initialization
```
\[or\]

```c#
data-type[] array-name =  { array-elements }; //short syntax of array declaration and initialization
```
### Examples

```c
int[] num = {1,2,3,4,5};
```
## Functions

```c#
<AccessSpecifier> <return-type> FunctionName(<parameters>)  // functin definition
{  
//code
}
function_name (parameters); // calling a function
```
## Structures

```c
struct structure_name {

   member definition;
   member definition;
   ...
   member definition;
}; 

structure_name variable name; //declaring structure variables
```
## enum

```c#
enum name{constant1, constant2, constant3, ....... } ;
```
