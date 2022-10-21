**Contributed by [Prateek Hebsur](https://github.com/Villain45) w.r.t Hacktoberfest 2022**

**Javascript Basics**
Including JavaScript in an HTML Page

    <script type="text/javascript">
    //JS code goes here
    </script>

Including Comments

    // Single line comments

`/* comment here */` Multi-line comments

**Variables**
var, const, let

- var The most common variable. Can be reassigned but only accessed
  within a function, Variables defined with var move to the top when
  code is executed.
- const Cannot be reassigned and not accessible before they appear
  within the code.
- let Similar to const, however, let variable can be reassigned but not
  re-declared.

**Arrays**
Example: var names= ["Raj", "Ram", "Sham"];

_Array Methods_

    concat()
    Join several arrays into one

    indexOf()
    Returns the first position at which a given element appears in an array

    join()
    Combine elements of an array into a single string and return the string

    lastIndexOf()
    the last position at which a given element appears in an array

    pop()
    Removes the last element of an array

    push()
    Add a new element at the end

    reverse()
    Reverse the order of the elements in an array

    shift()
    Remove the first element of an array

    slice()
    Pulls a copy of a portion of an array into a new array

    sort()
    Sorts elements alphabetically

    splice()
    Adds elements in a specified way and position

    toString()
    Converts elements to strings

    unshift()
    Adds a new element to the beginning

    valueOf()
    Returns the primitive value of the specified object

**Functions**

    function name(parameter1, parameter2, parameter3) {
    // what the function does
    }

**Loops**

    for (before loop; condition for loop; execute after loop) {
       // what to do during the loop
       }

**for**
The most common way to create a loop in Javascript
**while**
Sets up conditions under which a loop executes
**do while**
Similar to the while loop, however, it executes at least once and performs a check at the end to see if the condition is met to execute again
**break**
Used to stop and exit the cycle at certain conditions continue Skip parts of the cycle if certain conditions are met

**Strings**

    var event = "Hacktoberfest 2022";

_String Methods_

    charAt()
    Returns a character at a specified position inside a string

    charCodeAt()
    Gives you the unicode of character at that position

    concat()
    Concatenates (joins) two or more strings into one

    fromCharCode()
    Returns a string created from the specified sequence of UTF-16 code units

    indexOf()
    Provides the position of the first occurrence of a specified text within a string

    lastIndexOf()
    Same as indexOf() but with the last occurrence, searching backwards

    match()
    Retrieves the matches of a string against a search pattern

    replace()
    Find and replace specific text in a string

    search()
    Executes a search for a matching text and returns its position

    slice()
    Extracts a section of a string and returns it as a new string

    split()
    Splits a string object into an array of strings at a specified position

    substr()
    Similar to slice() but extracts a substring depended on a specified number of characters

    substring()
    Also similar to slice() but can’t accept negative indices

    toLowerCase()
    Convert strings to lowercase

    toUpperCase()
    Convert strings to uppercase

    valueOf()
    Returns the primitive value (that has no properties or methods) of a string object

**Numbers and Math**

_Number Properties_

    MAX_VALUE
    The maximum numeric value representable in JavaScript

    MIN_VALUE
    Smallest positive numeric value representable in JavaScript

    NaN
    The “Not-a-Number” value

    NEGATIVE_INFINITY
    The negative Infinity value

    POSITIVE_INFINITY
    Positive Infinity value

**Dealing with Dates**

_Setting Dates_

    Date()
    Creates a new date object with the current date and time

    Date(2022, 5, 21, 3, 23, 10, 0)
    Create a custom date object. The numbers represent year, month, day, hour, minutes, seconds, milliseconds. You can omit anything you want except for year and month.

    Date("2017-06-23")
    Date declaration as a string

_Pulling Date and Time Values_

    getDate()
    Get the day of the month as a number (1-31)

    getDay()
    The weekday as a number (0-6)

    getFullYear()
    Year as a four digit number (yyyy)

    getHours()
    Get the hour (0-23)

    getMilliseconds()
    The millisecond (0-999)

    getMinutes()
    Get the minute (0-59)

    getMonth()
    Month as a number (0-11)

    getSeconds()
    Get the second (0-59)

    getTime()
    Get the milliseconds since January 1, 1970

    getUTCDate()
    The day (date) of the month in the specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.)

_Setting Part of a Date_

    setDate()
    Set the day as a number (1-31)

    setFullYear()
    Sets the year (optionally month and day)

    setHours()
    Set the hour (0-23)

    setMilliseconds()
    Set milliseconds (0-999)

    setMinutes()
    Sets the minutes (0-59)

    setMonth()
    Set the month (0-11)

    setSeconds()
    Sets the seconds (0-59)

    setTime()
    Set the time (milliseconds since January 1, 1970)

    setUTCDate()
    Sets the day of the month for a specified date according to universal time (also available for day, month, fullyear, hours, minutes etc.)

**DOM (Document Object Modulation)**

_Node Properties_

    attributes
    Returns a live collection of all attributes registered to and element

    baseURI
    Provides the absolute base URL of an HTML element

    childNodes
    Gives a collection of an element’s child nodes

    firstChild
    Returns the first child node of an element

    lastChild
    The last child node of an element

    nextSibling
    Gives you the next node at the same node tree level

    nodeName
    Returns the name of a node

    nodeType
    Returns the type of a node

    nodeValue
    Sets or returns the value of a node

    ownerDocument
    The top-level document object for this node

    parentNode
    Returns the parent node of an element

    previousSibling
    Returns the node immediately preceding the current one

    textContent
    Sets or returns the textual content of a node and its descendants

_Element Methods_

    getAttribute()
    Returns the specified attribute value of an element node

    getAttributeNS()
    Returns string value of the attribute with the specified namespace and name

    getAttributeNode()
    Gets the specified attribute node

    getAttributeNodeNS()
    Returns the attribute node for the attribute with the given namespace and name

    getElementsByTagName()
    Provides a collection of all child elements with the specified tag name

    getElementsByTagNameNS()
    Returns a live HTMLCollection of elements with a certain tag name belonging to the given namespace

    hasAttribute()
    Returns true if an element has any attributes, otherwise false

    hasAttributeNS()
    Provides a true/false value indicating whether the current element in a given namespace has the specified attribute

    removeAttribute()
    Removes a specified attribute from an element

    removeAttributeNS()
    Removes the specified attribute from an element within a certain namespace

    removeAttributeNode()
    Takes away a specified attribute node and returns the removed node

    setAttribute()
    Sets or changes the specified attribute to a specified value

    setAttributeNS()
    Adds a new attribute or changes the value of an attribute with the given namespace and name

    setAttributeNode()
    Sets or changes the specified attribute node

    setAttributeNodeNS()
    Adds a new name spaced attribute node to an element

**Events**
_Mouse_

    onclick
    The event occurs when the user clicks on an element

    oncontextmenu
    User right-clicks on an element to open a context menu

    ondblclick
    The user double-clicks on an element

    onmousedown
    User presses a mouse button over an element

    onmouseenter
    The pointer moves onto an element

    onmouseleave
    Pointer moves out of an element

    onmousemove
    The pointer is moving while it is over an element

    onmouseover
    When the pointer is moved onto an element or one of its children

    onmouseout
    User moves the mouse pointer out of an element or one of its children

    onmouseup
    The user releases a mouse button while over an element

_Keyboard_

    onkeydown
    When the user is pressing a key down

    onkeypress
    The moment the user starts pressing a key

    onkeyup
    The user releases a key

_Frame_

    onabort
    The loading of a media is aborted

    onbeforeunload
    Event occurs before the document is about to be unloaded

    onerror
    An error occurs while loading an external file

    onhashchange
    There have been changes to the anchor part of a URL onload When an object has loaded

    onpagehide
    The user navigates away from a webpage

    onpageshow
    When the user navigates to a webpage

    onresize
    The document view is resized

    onscroll
    An element’s scrollbar is being scrolled

    onunload
    Event occurs when a page has unloaded

_Form_

    onblur
    When an element loses focus

    onchange
    The content of a form element changes

    onfocus
    An element gets focus

    onfocusin
    When an element is about to get focus

    onfocusout
    The element is about to lose focus

    oninput
    User input on an element

    oninvalid
    An element is invalid

    onreset
    A form is reset

    onsearch
    The user writes something in a search field

**Errors**

    try
    Lets you define a block of code to test for errors

    catch
    Set up a block of code to execute in case of an error

    throw
    Create custom error messages instead of the standard JavaScript errors

    finally
    Lets you execute code, after try and catch, regardless of the result
