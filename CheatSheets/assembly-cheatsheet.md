---
title: Assembly language 
description: Assembly language cheatsheet gives you a quick reference to code syntax with examples makes it handy while coding.
created: 2020-07-06
updated: 2020-07-06
---

## Sample program
```c
section .data
	hello:     db 'Hello world!',10    ; 'Hello world!' plus a linefeed character
	helloLen:  equ $-hello             ; Length of the 'Hello world!' string

section .text
	global _start

_start:
	mov eax,4            ; The system call for write (sys_write)
	mov ebx,1            ; File descriptor 1 - standard output
	mov ecx,hello        ; Put the offset of hello in ecx
	mov edx,helloLen     ; helloLen is a constant, so we don't need to say
	                     ;  mov edx,[helloLen] to get it's actual value
	int 80h              ; Call the kernel
	mov eax,1            ; The system call for exit (sys_exit)
	mov ebx,0            ; Exit with return "code" of 0 (no error)
	int 80h;
```
Assembly language usually consists of three sections, 

1. Data section

    To initialize variables and constants, buffer size these values doesn't change at runtime. 

2. bss section

    To declare variables

3. text section

    `_start` specifies the starting of this section where the actually code is written. 

## Variables

There are various define directives to allocate space for variables for both initialized and uninitialized data.

### 1.  To allocate storage space to Initialized data

```c
variable-name    define-directive    initial-value 
```

|Define Directive| Description| Allocated Space|
|-----|----|----|
|DB| Define Byte| 1 byte|
|DW| Define Word| 2 bytes|
|DD| Define Doubleword | 4 bytes|
|DQ| Define Quadword | 8 bytes|
|DT| Define Ten Bytes | 10 bytes|


### 2.  To allocate storage space to un-initialized data

|Define Directive| Description|
|-----|----|
|RESB |	Reserve a Byte|
|RESW | Reserve a Word|
|RESD |	Reserve a Doubleword|
|RESQ |	Reserve a Quadword|
|REST |	Reserve a Ten Bytes|

## Constants

Constants can be defined using 

### 1. equ

 * To define numeric constants

```
CONSTANT_NAME EQU regular-exp or value
```
### 2. %assign

 * To define numeric constants.

 ```
 %assign constant_name value
 ```

### 3. %define
* To define numeric or string constants.

```
%define constant_name value
```

## Loops

Loops are used to iterate a set of statements for a specific number of times.

```
mov ECX,n
L1:
;<loop body>
loop L1
```
where n specifies the no of times loops should iterate.

## Procedures

```
procedure_name:
   ;procedure body
   ret
```
