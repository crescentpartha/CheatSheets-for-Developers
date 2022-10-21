# Table of Content

 - [Data Types](#data-types)
 - [Data Conversion](#data-conversion)
 - [Operators](#operators)
 - [Statements](#statements)
 - [String Methods](#string-methods)
 
## Data Types
| Data Type | Size |
|--|--|
| boolean | 1 bit |
| char | 2 byte |
| int | 4 byte |
| short | 2 byte| 
|long |8 byte |
|float|4 byte|
|double|8 byte |

## Data Conversion

### String to Number
```java
    int i = Intege­r.p­ars­eInt(_str_);  
	double d = Double.pa­rse­Double(_str_);
```
	
### Any Type to String
```java
	String s = String.va­lueOf(_value_);  

```
  
### Numeric Conver­sions
```java
	int i = (int) _numeric expression_; 

```

## Operators
| Operator Category | Operators |
|--|--|
| Arithmetic operators |+, -, /, *, %  |
|Relational operators|<, >, <=, >=,==, !=|
|Logical operators|&&, \|\||
|Assignment operator|=, +=, −=, ×=, ÷=, %=, &=, ^=, \|=, <<=, >>=, >>>=|
|Increment and Decrement operator|++ , - -|
|Conditional operators|?, :|
|Bitwise operators|^, &, \||
|Special operators|. (dot operator to access methods of class)|

## Statements
### If Statement
```java
if ( _expression_ ) {  
­ _statements_  
} else if ( _expression_ ) {  
­ _statements_  
} else {  
­ _statements_  
}  
```
### While Loop 
```java
while ( _expression_ ) {  
­ _statements_  
}  
```

  
### Do-While Loop 
```java
do {  
­ _statements_  
} while ( _expression_ ); 
```
  
### For Loop 
```java
for ( int i = 0; i < _max_; ++i) {  
­ _statements_  
}  
```

  
### For Each Loop
```java
for ( _var_ : _collection_ ) {  
­ _statements_  
} 
```
 
  
### Switch Statement 
```java
switch ( _expression_ ) {  
­ case _value_:  
­ ­ ­ _statements_  
­ ­ ­ ­break;  
­ case _value2_:  
­ ­ ­ _statements_  
­ ­ ­ ­break;  
­ ­def­ault:  
­ ­ ­ _statements_  
} 
```
  
### Exception Handling
```java
try {  
­ ­sta­tem­ents;  
} catch (_Except­ionType_  _e1_) {  
­ ­sta­tem­ents;  
} catch (Exception _e2_) {  
­ ­cat­ch-all statem­ents;  
} finally {  
­ ­sta­tem­ents;  
}
```

## String Methods
| Command |Description  |
|--|--|
|length | length of string |
|charAt(_i_) |extract _i_th character  |
|subst­ring(_start_, _end_) |substring from _start_ to _end_-1  |
|toUpp­erC­ase() |returns copy of _s_ in ALL CAPS  |
|toLow­erC­ase() |returns copy of _s_ in lowercase  |
|indexOf(_x_) |index of first occurence of _x_  |
|replace(_old_, _new_)|search and replace  |
|split(_regex_) |splits string into tokens  |
|trim()  |trims surrou­nding whitespace  |
|equals(_s2_)  |true if s equals s2  |
|compa­reTo(_s2_)  | 0 if equal/+ if s > s2/- if s < s2 |

## Math Library Methods
|Command|Description|
|--|--|
|abs(_x_)|abstract value of x|
|max(a, b|maximum of a and b|
|min(a, b)|minimum of a and b|
|E|value of _e (constant)_|
|sin(theta)| sine of theta|
|cos(theta|cosine of theta|
|tan(theta)|tangent of theta|