---
title: JavaScript CheatSheet
description: The most commonly used JavaScript concepts are given here.
created: 2022-10-21
---

## Table of Contents

- [JavaScript CheatSheet for Developers](#javascript-cheatsheet-for-developers)
  - [JavaScript Basics](#javascript-basics)
    - [JavaScript Code in the HTML Page](#javascript-code-in-the-html-page)
    - [Comments](#comments)
    - [Variables](#variables)
    - [Arrays](#arrays)
    - [Array Methods](#array-methods)
    - [Functions](#functions)
    - [Loops](#loops)
      - [For](#for)
      - [While](#while)
      - [Do While](#do-while)
      - [Break](#break)
    - [Strings](#strings)
    - [String Methods](#string-methods)
  - [Numbers and Math](#numbers-and-math)
    - [Number Properties](#number-properties)
    - [Dealing with Dates](#dealing-with-dates)
      - [Setting Dates](#setting-dates)
      - [Pulling Date and Time Values](#pulling-date-and-time-values)
      - [Setting Part of a Date](#setting-part-of-a-date)
  - [DOM (Document Object Modulation)](#dom-document-object-modulation)
    - [Element Methods](#element-methods)
  - [Events](#events)
    - [Mouse](#mouse)
    - [Keyboard](#keyboard)
    - [Frame](#frame)
    - [Form](#form)
  - [Errors](#errors)

# JavaScript CheatSheet for Developers

## JavaScript Basics

### JavaScript Code in the HTML Page

``` JavaScript
<script type="text/javascript">
    // JS code goes here
</script>
```

**[🔼Back to Top](#table-of-contents)**

### Comments

``` JavaScript
// Single line comments

/* Multi-line comments */ 
```

**[🔼Back to Top](#table-of-contents)**

### Variables

| Variables | Description |
| ---- | --- |
| var | The most common variable. Can be reassigned but only accessed within a function, Variables defined with var move to the top when code is executed. |
| const | Cannot be reassigned and not accessible before they appear within the code. |
| let | Similar to const, however, let variable can be reassigned but not re-declared. |

**[🔼Back to Top](#table-of-contents)**

### Arrays

``` JavaScript
// Example
var names= ["Raj", "Ram", "Sham"];
```

**[🔼Back to Top](#table-of-contents)**

### Array Methods

| Method        | Description                                                             |
| ------------- | ----------------------------------------------------------------------- |
| concat()      | Join several arrays into one                                            |
| indexOf()     | Returns the first position at which a given element appears in an array |
| join()        | Combine elements of an array into a single string and return the string |
| lastIndexOf() | the last position at which a given element appears in an array          |
| pop()         | Removes the last element of an array                                    |
| push()        | Add a new element at the end                                            |
| reverse()     | Reverse the order of the elements in an array                           |
| shift()       | Remove the first element of an array                                    |
| slice()       | Pulls a copy of a portion of an array into a new array                  |
| sort()        | Sorts elements alphabetically                                           |
| splice()      | Adds elements in a specified way and position                           |
| toString()    | Converts elements to strings                                            |
| unshift()     | Adds a new element to the beginning                                     |
| valueOf()     | Returns the primitive value of the specified object                     |

**[🔼Back to Top](#table-of-contents)**

### Functions 

``` JavaScript
function name(parameter1, parameter2, parameter3) {
    // what the function does
}
```

**[🔼Back to Top](#table-of-contents)**

### Loops

``` JavaScript
for (Initialization; Condition; Increment/Decrement) {
    // what to do during the loop
}
```

**[🔼Back to Top](#table-of-contents)**

#### For

> The most common way to create a loop in Javascript

**[🔼Back to Top](#table-of-contents)**

#### While

> Sets up conditions under which a loop executes

**[🔼Back to Top](#table-of-contents)**

#### Do While

> Similar to the while loop, however, it executes at least once and performs a check at the end to see if the condition is met to execute again

**[🔼Back to Top](#table-of-contents)**

#### Break

> Used to stop and exit the cycle at certain conditions continue Skip parts of the cycle if certain conditions are met

**[🔼Back to Top](#table-of-contents)**

### Strings

``` JavaScript
var event = "Hacktoberfest 2022";
```

**[🔼Back to Top](#table-of-contents)**

### String Methods

| Method         | Description                                                                              |
| -------------- | ---------------------------------------------------------------------------------------- |
| charAt()       | Returns a character at a specified position inside a string                              |
| charCodeAt()   | Gives you the unicode of character at that position                                      |
| concat()       | Concatenates (joins) two or more strings into one                                        |
| fromCharCode() | Returns a string created from the specified sequence of UTF-16 code units                |
| indexOf()      | Provides the position of the first occurrence of a specified text within a string        |
| lastIndexOf()  | Same as indexOf() but with the last occurrence, searching backwards                      |
| match()        | Retrieves the matches of a string against a search pattern                               |
| replace()      | Find and replace specific text in a string                                               |
| search()       | Executes a search for a matching text and returns its position                           |
| slice()        | Extracts a section of a string and returns it as a new string                            |
| split()        | Splits a string object into an array of strings at a specified position                  |
| substr()       | Similar to slice() but extracts a substring depended on a specified number of characters |
| substring()    | Also similar to slice() but can’t accept negative indices                                |
| toLowerCase()  | Convert strings to lowercase                                                             |
| toUpperCase()  | Convert strings to uppercase                                                             |
| valueOf()      | Returns the primitive value (that has no properties or methods) of a string object       |

**[🔼Back to Top](#table-of-contents)**

## Numbers and Math

### Number Properties

| Method            | Description                                                 |
| ----------------- | ----------------------------------------------------------- |
| MAX_VALUE         | The maximum numeric value representable in JavaScript       |
| MIN_VALUE         | Smallest positive numeric value representable in JavaScript |
| NaN               | The “Not-a-Number” value                                    |
| NEGATIVE_INFINITY | The negative Infinity value                                 |
| POSITIVE_INFINITY | Positive Infinity value                                     |

**[🔼Back to Top](#table-of-contents)**

### Dealing with Dates

> `Contents need to be added in this section.`  

**[🔼Back to Top](#table-of-contents)**

#### Setting Dates

| Method                          | Description                                                                                                                                                          |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Date()                          | Creates a new date object with the current date and time                                                                                                             |
| Date(2022, 5, 21, 3, 23, 10, 0) | Create a custom date object. The numbers represent year, month, day, hour, minutes, seconds, milliseconds. You can omit anything you want except for year and month. |
| Date("2017-06-23")              | Date declaration as a string                                                                                                                                         |

**[🔼Back to Top](#table-of-contents)**

#### Pulling Date and Time Values

| Function          | Description                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| getDate()         | Get the day of the month as a number (1-31)                                                                                                  |
| getDay()          | The weekday as a number (0-6)                                                                                                                |
| getFullYear()     | Year as a four digit number (yyyy)                                                                                                           |
| getHours()        | Get the hour (0-23)                                                                                                                          |
| getMilliseconds() | The millisecond (0-999)                                                                                                                      |
| getMinutes()      | Get the minute (0-59)                                                                                                                        |
| getMonth()        | Month as a number (0-11)                                                                                                                     |
| getSeconds()      | Get the second (0-59)                                                                                                                        |
| getTime()         | Get the milliseconds since January 1, 1970                                                                                                   |
| getUTCDate()      | The day (date) of the month in the specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.) |

**[🔼Back to Top](#table-of-contents)**

#### Setting Part of a Date

| Method            | Description                                                                                                                               |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| setDate()         | Set the day as a number (1-31)                                                                                                            |
| setFullYear()     | Sets the year (optionally month and day)                                                                                                  |
| setHours()        | Set the hour (0-23)                                                                                                                       |
| setMilliseconds() | Set milliseconds (0-999)                                                                                                                  |
| setMinutes()      | Sets the minutes (0-59)                                                                                                                   |
| setMonth()        | Set the month (0-11)                                                                                                                      |
| setSeconds()      | Sets the seconds (0-59)                                                                                                                   |
| setTime()         | Set the time (milliseconds since January 1, 1970)                                                                                         |
| setUTCDate()      | Sets the day of the month for a specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.) |

**[🔼Back to Top](#table-of-contents)**

## DOM (Document Object Modulation)

### Element Methods
  
| Method                   | Description                                                                                                         |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| getAttribute()           | Returns the specified attribute value of an element node                                                            |
| getAttributeNS()         | Returns string value of the attribute with the specified namespace and name                                         |
| getAttributeNode()       | Gets the specified attribute node                                                                                   |
| getAttributeNodeNS()     | Returns the attribute node for the attribute with the given namespace and name                                      |
| getElementsByTagName()   | Provides a collection of all child elements with the specified tag name                                             |
| getElementsByTagNameNS() | Returns a live HTMLCollection of elements with a certain tag name belonging to the given namespace                  |
| hasAttribute()           | Returns true if an element has any attributes, otherwise false                                                      |
| hasAttributeNS()         | Provides a true/false value indicating whether the current element in a given namespace has the specified attribute |
| removeAttribute()        | Removes a specified attribute from an element                                                                       |
| removeAttributeNS()      | Removes the specified attribute from an element within a certain namespace                                          |
| removeAttributeNode()    | Takes away a specified attribute node and returns the removed node                                                  |
| setAttribute()           | Sets or changes the specified attribute to a specified value                                                        |
| setAttributeNS()         | Adds a new attribute or changes the value of an attribute with the given namespace and name                         |
| setAttributeNode()       | Sets or changes the specified attribute node                                                                        |
| setAttributeNodeNS()     | Adds a new name spaced attribute node to an element                                                                 |

**[🔼Back to Top](#table-of-contents)**

## Events

### Mouse

| Method        | Description                                                           |
| ------------- | --------------------------------------------------------------------- |
| onclick       | The event occurs when the user clicks on an element                   |
| oncontextmenu | User right-clicks on an element to open a context menu                |
| ondblclick    | The user double-clicks on an element                                  |
| onmousedown   | User presses a mouse button over an element                           |
| onmouseenter  | The pointer moves onto an element                                     |
| onmouseleave  | Pointer moves out of an element                                       |
| onmousemove   | The pointer is moving while it is over an element                     |
| onmouseover   | When the pointer is moved onto an element or one of its children      |
| onmouseout    | User moves the mouse pointer out of an element or one of its children |
| onmouseup     | The user releases a mouse button while over an element                |

**[🔼Back to Top](#table-of-contents)**

### Keyboard

| Method     | Description                               |
| ---------- | ----------------------------------------- |
| onkeydown  | When the user is pressing a key down      |
| onkeypress | The moment the user starts pressing a key |
| onkeyup    | The user releases a key                   |

**[🔼Back to Top](#table-of-contents)**

### Frame

| Method         | Description                                                                          |
| -------------- | ------------------------------------------------------------------------------------ |
| onabort        | The loading of a media is aborted                                                    |
| onbeforeunload | Event occurs before the document is about to be unloaded                             |
| onerror        | An error occurs while loading an external file                                       |
| onhashchange   | There have been changes to the anchor part of a URL onload When an object has loaded |
| onpagehide     | The user navigates away from a webpage                                               |
| onpageshow     | When the user navigates to a webpage                                                 |
| onresize       | The document view is resized                                                         |
| onscroll       | An element’s scrollbar is being scrolled                                             |
| onunload       | Event occurs when a page has unloaded                                                |

**[🔼Back to Top](#table-of-contents)**

### Form
  
| Method     | Description                                 |
| ---------- | ------------------------------------------- |
| onblur     | When an element loses focus                 |
| onchange   | The content of a form element changes       |
| onfocus    | An element gets focus                       |
| onfocusin  | When an element is about to get focus       |
| onfocusout | The element is about to lose focus          |
| oninput    | User input on an element                    |
| oninvalid  | An element is invalid                       |
| onreset    | A form is reset                             |
| onsearch   | The user writes something in a search field |

**[🔼Back to Top](#table-of-contents)**

## Errors

| Error Handlers | Description                                                            |
| -------------- | ---------------------------------------------------------------------- |
| try            | Lets you define a block of code to test for errors                     |
| catch          | Set up a block of code to execute in case of an error                  |
| throw          | Create custom error messages instead of the standard JavaScript errors |
| finally        | Lets you execute code, after try and catch, regardless of the result   |

**[🔼Back to Top](#table-of-contents)**
