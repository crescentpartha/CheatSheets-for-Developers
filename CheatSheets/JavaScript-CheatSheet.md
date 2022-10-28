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
      - [Array.Prototype.Push()](#arrayprototypepush)
      - [Array.Prototype.Pop()](#arrayprototypepop)
      - [Array.Prototype.Shift()](#arrayprototypeshift)
      - [Array.Prototype.Unshift()](#arrayprototypeunshift)
      - [Array.Prototype.Slice()](#arrayprototypeslice)
      - [Array.Prototype.Splice()](#arrayprototypesplice)
      - [Array.Prototype.Concat()](#arrayprototypeconcat)
      - [Array.Prototype.IndexOf()](#arrayprototypeindexof)
      - [Array.Prototype.LastIndexOf()](#arrayprototypelastindexof)
      - [Array.Prototype.Join()](#arrayprototypejoin)
      - [Array.Prototype.Reverse()](#arrayprototypereverse)
      - [Array.Prototype.Sort()](#arrayprototypesort)
      - [Array.Prototype.ForEach()](#arrayprototypeforeach)
      - [Array.Prototype.Map()](#arrayprototypemap)
      - [Array.Prototype.Filter()](#arrayprototypefilter)
      - [Array.Prototype.Reduce()](#arrayprototypereduce)
      - [Array.Prototype.ReduceRight()](#arrayprototypereduceright)
      - [Array.Prototype.Every()](#arrayprototypeevery)
      - [Array.Prototype.Some()](#arrayprototypesome)
      - [Array.Prototype.Find()](#arrayprototypefind)
      - [Array.Prototype.FindIndex()](#arrayprototypefindindex)
      - [Array.Prototype.Fill()](#arrayprototypefill)
      - [Array.Prototype.CopyWithin()](#arrayprototypecopywithin)
      - [Array.Prototype.Includes()](#arrayprototypeincludes)
      - [Array.Prototype.Flat()](#arrayprototypeflat)
      - [Array.Prototype.FlatMap()](#arrayprototypeflatmap)
      - [Array.Prototype.Keys()](#arrayprototypekeys)
      - [Array.Prototype.Values()](#arrayprototypevalues)
      - [Array.Prototype.Entries()](#arrayprototypeentries)
      - [Array.Prototype.at()](#arrayprototypeat)
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
      - [Format Date Object](#format-date-object)
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
| :----:    | :--- |
| `var`     | The most common variable. Can be reassigned but only accessed within a function, Variables defined with var move to the top when code is executed. |
| `const`   | Cannot be reassigned and not accessible before they appear within the code. |
| `let`     | Similar to const, however, let variable can be reassigned but not re-declared. |

**[🔼Back to Top](#table-of-contents)**

### Arrays

``` JavaScript
// Example
var names= ["Raj", "Ram", "Sham"];
```

**[🔼Back to Top](#table-of-contents)**

### Array Methods

| Method          | Description                                                             |
| :-------------: | :---------------------------------------------------------------------- |
| `push()`        | Adds an element to the end of an array                                  |
| `pop()`         | Removes the last element of an array                                    |
| `shift()`       | Removes the first element of an array                                   |
| `unshift()`     | Adds an element to the beginning of an array                            |
| `slice()`       | Selects a part of an array and returns the new array                    |
| `splice()`      | Adds/Removes elements to/from an array                                  |
| `concat()`      | Joins two or more arrays, and returns a copy of the joined arrays       |
| `indexOf()`     | Search the array for an element and returns its position                |
| `lastIndexOf()` | Search the array for an element, starting at the end, and returns its position |
| `join()`        | Joins all elements of an array into a string                            |
| `reverse()`     | Reverses the order of the elements in an array                          |
| `sort()`        | Sorts the elements of an array                                          |
| `forEach()`     | Calls a function for each array element                                 |
| `map()`         | Creates a new array with the result of calling a function for each array element |
| `filter()`      | Creates a new array with every element in an array that pass a test     |
| `reduce()`      | Reduce the values of an array to a single value (going left-to-right)   |
| `reduceRight()` | Reduce the values of an array to a single value (going right-to-left)   |
| `every()`       | Check if all array values pass a test                                   |
| `some()`        | Check if some array values pass a test                                  |
| `find()`        | Returns the value of the first array element that pass a test           |
| `findIndex()`   | Returns the index of the first array element that pass a test           |
| `fill()`        | Fill the elements in an array with a static value                       |
| `copyWithin()`  | Copy array elements within the array                                    |
| `includes()`    | Check if an array contains the specified element                        |
| `flat()`        | Creates a new array with sub-array elements concatenated into it        |
| `flatMap()`     | First maps each element using a mapping function, then flattens the result into a new array |
| `keys()`        | Returns a Array Iterator object with the keys of an array               |
| `values()`      | Returns a Array Iterator object with the values of an array             |
| `entries()`     | Returns a Array Iterator object with key/value pairs                    |
| `at()`          | Returns the element at the specified index in an array                  |

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Push()

``` JavaScript
// Syntax
array.push(element1, element2, ..., elementN);
// Example
var names= ["Raj", "Ram", "Sham"];
names.push("Ramesh");
// Output
["Raj", "Ram", "Sham", "Ramesh"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Pop()

``` JavaScript
// Syntax
array.pop();
// Example
var names= ["Raj", "Ram", "Sham"];
names.pop();
// Output
["Raj", "Ram"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Shift()

``` JavaScript
// Syntax
array.shift();
// Example
var names= ["Raj", "Ram", "Sham"];
names.shift();
// Output
["Ram", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Unshift()

``` JavaScript
// Syntax
array.unshift(element1, element2, ..., elementN);
// Example
var names= ["Raj", "Ram", "Sham"];
names.unshift("Ramesh");
// Output
["Ramesh", "Raj", "Ram", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Slice()

``` JavaScript
// Syntax
array.slice();
array.slice(start);
array.slice(start, end);
// Example
var names= ["Raj", "Ram", "Sham"];
names.slice(1, 2);
// Output
["Ram"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Splice()

``` JavaScript
// Syntax
array.splice(start)
array.splice(start, deleteCount)
array.splice(start, deleteCount, item1)
array.splice(start, deleteCount, item1, item2, itemN)
// Example
var names= ["Raj", "Ram", "Sham"];
names.splice(1, 2);
// Output
["Ram", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Concat()

``` JavaScript
// Syntax
array.concat(array1, array2, ..., arrayN);
// Example
var names= ["Raj", "Ram", "Sham"];
var names2= ["Ramesh", "Rajesh", "Rakesh"];
names.concat(names2);
// Output
["Raj", "Ram", "Sham", "Ramesh", "Rajesh", "Rakesh"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.IndexOf()

``` JavaScript
// Syntax
array.indexOf(searchElement);
// Example
var names= ["Raj", "Ram", "Sham"];
names.indexOf("Ram");
// Output
1
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.LastIndexOf()

``` JavaScript
// Syntax
array.lastIndexOf(searchElement);
// Example
var names= ["Raj", "Ram", "Sham", "Ram"];
names.lastIndexOf("Ram");
// Output
3
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Join()

``` JavaScript
// Syntax
array.join(separator);
// Example
var names= ["Raj", "Ram", "Sham"];
names.join(" ");
// Output
Raj Ram Sham
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Reverse()

``` JavaScript
// Syntax
array.reverse();
// Example
var names= ["Raj", "Ram", "Sham"];
names.reverse();
// Output
["Sham", "Ram", "Raj"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Sort()

``` JavaScript
// Syntax
array.sort();
array.sort(compareFunction);
// Example
var names= ["Raj", "Ram", "Sham"];
names.sort();
// Output
["Ram", "Raj", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.ForEach()

``` JavaScript
// Syntax
array.forEach(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.forEach(function(name) {
    console.log(name);
});
// Output
Raj
Ram
Sham
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Map()

``` JavaScript
// Syntax
array.map(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.map(function(name) {
    return name + " Singh";
});
// Output
["Raj Singh", "Ram Singh", "Sham Singh"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Filter()

``` JavaScript
// Syntax
array.filter(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.filter(function(name) {
    return name.length > 3;
});
// Output
["Raj", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Reduce()

``` JavaScript
// Syntax
array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.reduce(function(total, name) {
    return total + name;
}, "");
// Output
RajRamSham

// Example
var numbers= [1, 2, 3];
numbers.reduce(function(total, number) {
    return total * number;
}, 1);
// Output
6
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.ReduceRight()

``` JavaScript
// Syntax
array.reduceRight(function(total, currentValue, currentIndex, arr), initialValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.reduceRight(function(total, name) {
    return total + name;
}, "");
// Output
ShamRamRaj
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Every()

``` JavaScript
// Syntax
array.every(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.every(function(name) {
    return name.length > 3;
});
// Output
false
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Some()

``` JavaScript
// Syntax
array.some(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.some(function(name) {
    return name.length > 3;
});
// Output
true
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Find()

``` JavaScript
// Syntax
array.find(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.find(function(name) {
    return name.length > 3;
});
// Output
Raj
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.FindIndex()

``` JavaScript
// Syntax
array.findIndex(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.findIndex(function(name) {
    return name.length > 3;
});
// Output
0
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Fill()

``` JavaScript
// Syntax
array.fill(value, start, end)
// Example
var names= ["Raj", "Ram", "Sham"];
names.fill("Ramesh");
// Output
["Ramesh", "Ramesh", "Ramesh"]

// Example
var names= ["Raj", "Ram", "Sham"];
names.fill("Ramesh", 1, 2);
// Output
["Raj", "Ramesh", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.CopyWithin()

``` JavaScript
// Syntax
array.copyWithin(target, start, end)
// Example
var names= ["Raj", "Ram", "Sham"];
names.copyWithin(1, 0);
// Output
["Raj", "Raj", "Ram"]

// Example
var names= ["Raj", "Ram", "Sham"];
names.copyWithin(1, 0, 2);
// Output
["Raj", "Raj", "Sham"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Includes()

``` JavaScript
// Syntax
array.includes(searchElement, fromIndex)
// Example
var names= ["Raj", "Ram", "Sham"];
names.includes("Ram");
// Output
true

// Example
var names= ["Raj", "Ram", "Sham"];
names.includes("Ram", 1);
// Output
false
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Flat()

``` JavaScript
// Syntax
array.flat(depth)
// Example
var names= ["Raj", ["Ram", "Sham"]];
names.flat();
// Output
["Raj", "Ram", "Sham"]

// Example
var names= ["Raj", ["Ram", ["Sham"]]];
names.flat(1);
// Output
["Raj", "Ram", ["Sham"]]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.FlatMap()

``` JavaScript
// Syntax
array.flatMap(function(currentValue, index, arr), thisValue)
// Example
var names= ["Raj", "Ram", "Sham"];
names.flatMap(function(name) {
    return name + " Singh";
});
// Output
["Raj Singh", "Ram Singh", "Sham Singh"]
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Keys()

``` JavaScript
// Syntax
array.keys()
// Example
var names= ["Raj", "Ram", "Sham"];
var iterator = names.keys();
iterator.next();
// Output
{value: 0, done: false}
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Values()

``` JavaScript
// Syntax
array.values()
// Example
var names= ["Raj", "Ram", "Sham"];
var iterator = names.values();
iterator.next();
// Output
{value: "Raj", done: false}
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.Entries()

``` JavaScript
// Syntax
array.entries()
// Example
var names= ["Raj", "Ram", "Sham"];
var iterator = names.entries();
iterator.next();
// Output
{value: Array(2), done: false}
```

**[🔼Back to Top](#table-of-contents)**

#### Array.Prototype.at()

``` JavaScript
// Syntax
array.at(index)
// Example
var names= ["Raj", "Ram", "Sham"];
names.at(1);
// Output
Ram
```

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

| Method           | Description                                                                              |
| :--------------: | :--------------------------------------------------------------------------------------- |
| `charAt()`       | Returns a character at a specified position inside a string                              |
| `charCodeAt()`   | Gives you the unicode of character at that position                                      |
| `concat()`       | Concatenates (joins) two or more strings into one                                        |
| `fromCharCode()` | Returns a string created from the specified sequence of UTF-16 code units                |
| `indexOf()`      | Provides the position of the first occurrence of a specified text within a string        |
| `lastIndexOf()`  | Same as indexOf() but with the last occurrence, searching backwards                      |
| `match()`        | Retrieves the matches of a string against a search pattern                               |
| `replace()`      | Find and replace specific text in a string                                               |
| `search()`       | Executes a search for a matching text and returns its position                           |
| `slice()`        | Extracts a section of a string and returns it as a new string                            |
| `split()`        | Splits a string object into an array of strings at a specified position                  |
| `substr()`       | Similar to slice() but extracts a substring depended on a specified number of characters |
| `substring()`    | Also similar to slice() but can’t accept negative indices                                |
| `toLowerCase()`  | Convert strings to lowercase                                                             |
| `toUpperCase()`  | Convert strings to uppercase                                                             |
| `valueOf()`      | Returns the primitive value (that has no properties or methods) of a string object       |

**[🔼Back to Top](#table-of-contents)**

## Numbers and Math

### Number Properties

| Method              | Description                                                 |
| :-----------------: | :---------------------------------------------------------- |
| `MAX_VALUE`         | The maximum numeric value representable in JavaScript       |
| `MIN_VALUE`         | Smallest positive numeric value representable in JavaScript |
| `NaN`               | The “Not-a-Number” value                                    |
| `NEGATIVE_INFINITY` | The negative Infinity value                                 |
| `POSITIVE_INFINITY` | Positive Infinity value                                     |

**[🔼Back to Top](#table-of-contents)**

### Dealing with Dates

> `Contents need to be added in this section.`  

**[🔼Back to Top](#table-of-contents)**

#### Setting Dates

| Method                            | Description                                                                                                                                                          |
| :-------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Date()`                          | Creates a new date object with the current date and time                                                                                                             |
| `Date(2022, 5, 21, 3, 23, 10, 0)` | Create a custom date object. The numbers represent year, month, day, hour, minutes, seconds, milliseconds. You can omit anything you want except for year and month. |
| `Date("2017-06-23")`              | Date declaration as a string                                                                                                                                         |

**[🔼Back to Top](#table-of-contents)**

#### Pulling Date and Time Values

| Function            | Description                                                                                                                                  |
| :-----------------: | :------------------------------------------------------------------------------------------------------------------------------------------- |
| `getDate()`         | Get the day of the month as a number (1-31)                                                                                                  |
| `getDay()`          | The weekday as a number (0-6)                                                                                                                |
| `getFullYear()`     | Year as a four digit number (yyyy)                                                                                                           |
| `getHours()`        | Get the hour (0-23)                                                                                                                          |
| `getMilliseconds()` | The millisecond (0-999)                                                                                                                      |
| `getMinutes()`      | Get the minute (0-59)                                                                                                                        |
| `getMonth()`        | Month as a number (0-11)                                                                                                                     |
| `getSeconds()`      | Get the second (0-59)                                                                                                                        |
| `getTime()`         | Get the milliseconds since January 1, 1970                                                                                                   |
| `getUTCDate()`      | The day (date) of the month in the specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.) |

**[🔼Back to Top](#table-of-contents)**

#### Setting Part of a Date

| Method              | Description                                                                                                                               |
| :-----------------: | :---------------------------------------------------------------------------------------------------------------------------------------- |
| `setDate()`         | Set the day as a number (1-31)                                                                                                            |
| `setFullYear()`     | Sets the year (optionally month and day)                                                                                                  |
| `setHours()`        | Set the hour (0-23)                                                                                                                       |
| `setMilliseconds()` | Set milliseconds (0-999)                                                                                                                  |
| `setMinutes()`      | Sets the minutes (0-59)                                                                                                                   |
| `setMonth()`        | Set the month (0-11)                                                                                                                      |
| `setSeconds()`      | Sets the seconds (0-59)                                                                                                                   |
| `setTime()`         | Set the time (milliseconds since January 1, 1970)                                                                                         |
| `setUTCDate()`      | Sets the day of the month for a specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.) |

**[🔼Back to Top](#table-of-contents)**

#### Format Date Object

| Method                 | Description                                                                                                                      |
| :--------------------: | :------------------------------------------------------------------------------------------------------------------------------- |
| `toLocaleDateString()` | Returns a string with a language-sensitive representation of the date portion of the specified date in the user agent's timezone |

**[🔼Back to Top](#table-of-contents)**

## DOM (Document Object Modulation)

### Element Methods
  
| Method                     | Description                                                                                                         |
| :------------------------: | :------------------------------------------------------------------------------------------------------------------ |
| `getAttribute()`           | Returns the specified attribute value of an element node                                                            |
| `getAttributeNS()`         | Returns string value of the attribute with the specified namespace and name                                         |
| `getAttributeNode()`       | Gets the specified attribute node                                                                                   |
| `getAttributeNodeNS()`     | Returns the attribute node for the attribute with the given namespace and name                                      |
| `getElementsByTagName()`   | Provides a collection of all child elements with the specified tag name                                             |
| `getElementsByTagNameNS()` | Returns a live HTMLCollection of elements with a certain tag name belonging to the given namespace                  |
| `hasAttribute()`           | Returns true if an element has any attributes, otherwise false                                                      |
| `hasAttributeNS()`         | Provides a true/false value indicating whether the current element in a given namespace has the specified attribute |
| `removeAttribute()`        | Removes a specified attribute from an element                                                                       |
| `removeAttributeNS()`      | Removes the specified attribute from an element within a certain namespace                                          |
| `removeAttributeNode()`    | Takes away a specified attribute node and returns the removed node                                                  |
| `setAttribute()`           | Sets or changes the specified attribute to a specified value                                                        |
| `setAttributeNS()`         | Adds a new attribute or changes the value of an attribute with the given namespace and name                         |
| `setAttributeNode()`       | Sets or changes the specified attribute node                                                                        |
| `setAttributeNodeNS()`     | Adds a new name spaced attribute node to an element                                                                 |

**[🔼Back to Top](#table-of-contents)**

## Events

### Mouse

| Method          | Description                                                           |
| :-------------: | :-------------------------------------------------------------------- |
| `onclick`       | The event occurs when the user clicks on an element                   |
| `oncontextmenu` | User right-clicks on an element to open a context menu                |
| `ondblclick`    | The user double-clicks on an element                                  |
| `onmousedown`   | User presses a mouse button over an element                           |
| `onmouseenter`  | The pointer moves onto an element                                     |
| `onmouseleave`  | Pointer moves out of an element                                       |
| `onmousemove`   | The pointer is moving while it is over an element                     |
| `onmouseover`   | When the pointer is moved onto an element or one of its children      |
| `onmouseout`    | User moves the mouse pointer out of an element or one of its children |
| `onmouseup`     | The user releases a mouse button while over an element                |

**[🔼Back to Top](#table-of-contents)**

### Keyboard

| Method       | Description                               |
| :----------: | :---------------------------------------- |
| `onkeydown`  | When the user is pressing a key down      |
| `onkeypress` | The moment the user starts pressing a key |
| `onkeyup`    | The user releases a key                   |

**[🔼Back to Top](#table-of-contents)**

### Frame

| Method           | Description                                                                          |
| :--------------: | :----------------------------------------------------------------------------------- |
| `onabort`        | The loading of a media is aborted                                                    |
| `onbeforeunload` | Event occurs before the document is about to be unloaded                             |
| `onerror`        | An error occurs while loading an external file                                       |
| `onhashchange`   | There have been changes to the anchor part of a URL onload When an object has loaded |
| `onpagehide`     | The user navigates away from a webpage                                               |
| `onpageshow`     | When the user navigates to a webpage                                                 |
| `onresize`       | The document view is resized                                                         |
| `onscroll`       | An element’s scrollbar is being scrolled                                             |
| `onunload`       | Event occurs when a page has unloaded                                                |

**[🔼Back to Top](#table-of-contents)**

### Form
  
| Method       | Description                                 |
| :----------: | :------------------------------------------ |
| `onblur`     | When an element loses focus                 |
| `onchange`   | The content of a form element changes       |
| `onfocus`    | An element gets focus                       |
| `onfocusin`  | When an element is about to get focus       |
| `onfocusout` | The element is about to lose focus          |
| `oninput`    | User input on an element                    |
| `oninvalid`  | An element is invalid                       |
| `onreset`    | A form is reset                             |
| `onsearch`   | The user writes something in a search field |

**[🔼Back to Top](#table-of-contents)**

## Errors

| Error Handlers   | Description                                                            |
| :--------------: | :--------------------------------------------------------------------- |
| `try`            | Lets you define a block of code to test for errors                     |
| `catch`          | Set up a block of code to execute in case of an error                  |
| `throw`          | Create custom error messages instead of the standard JavaScript errors |
| `finally`        | Lets you execute code, after try and catch, regardless of the result   |

**[🔼Back to Top](#table-of-contents)**
