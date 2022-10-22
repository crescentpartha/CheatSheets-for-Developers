---
title: Common Lisp 
description: Common Lisp cheatsheet gives you a quick reference to code syntax with examples makes it handy while coding.
created: 2020-07-05
updated: 2020-07-05
---

## Sample program

```lisp
(setq name (read))
(princ "Hello ")
(write name)
```
* **read** : used to read the data from console
* **setq** : used to create and assign values to the variables
* **princ** : used to print the output to the console
* **write** : used to write output to the console
* **`;`** : Indicates a comment line.

## Variables

Multiple ways to declare variables
### Example

```lisp
(defvar x 10)
(write x)
```
* `let` and `prog`are used to declare local variables.

```lisp
(let ((var1  value1) (var2  value2).. (varn  valuen))<expressions>)
```
* `setq` is used to declare both global and local variables.

```lisp
(setq a 10)
```
## Macros
```lisp
(defmacro macroName (parameter-list))
"Optional string for documentation"
;body
```
## Constants
```lisp
(defconstant constName value)
```
### Example
```lisp
(defconstant PI 3.141592)
```
## Operators

| Operator type | Description|
|----|-----|
| Arithmetic Operator|+ , - , * , / , rem, mod,incf,decf|
| Relational Operator| < , > , <= , >=, /= , ==, max, min|
| Logical Operator| and, or, not|
| Bitwise Operator | logand, logior, lognor, logxor, logeqv|

## Conditional statements

### 1. If
```lisp
(if [test] [then do this] [else do this])
```

### 2. When
```lisp
(when ([conditional-expr])
    ([do this])
    ([do this])
    ([do this, which returns value]))
```
### 3. Case

```lisp
(cond   (condition1    action1)
        (condition2    action2)
        ...
        (conditionn   actionn))
```

## Loops

### 1. Loop

```lisp
(loop (s-expressions))
```

### 2. For

```lisp
(loop for loop-variable in <a list>
   do (action)
)
```
### 3. Do

```lisp
(do ((var1    val1   updated-val1)
      (var2   val2   updated-val2)
      (var3   val3   updated-val3)
   ...)
   (test return-value)
   (s-expressions)
)
```

### 4. Dotimes

```lisp
(dotimes (n val)
  statements
```
## Arrays

```lisp
(setf arrayName (make-array '(length)))
```
## Lists

```lisp
(list 1 2 3 4 5)
(list 'a 'b 'c 'd 'e)
```
|List methods| Usage|Description|
|----|----|----|
| cons | (cons 'a '(b c)) --> (A B C) |  used to put together list items|
|append| (append '(a b) '(c d)) --> (A B C D) | Used to append lists|
|reverse| (reverse '(a b c)) --> (C B A) | used to reverse the list items|
|sort |(sort '(0 5 1 3 2) #'>) --> (5 3 2 1 0)| used to sort the list items|
|substitute | (substitute 'y 'x '(x 1 x 2)) --> (Y 1 Y 2) | used to substitute the list items with the given value|
|length|(length '(1 2 3 4 5)) --> 5 used to find the length of a list||
|count |(count '1 '(1 2 1 2 1)) --> 3| to count the occurence of a list item|
|remove| (remove 'item list) | removes the given item from list|

## Hash Table

```lisp
make-hash-table &key :test :size :rehash-size :rehash-threshold
```

## Structures

```lisp
(defstruct structureName 
    ; structureElements
)
```
