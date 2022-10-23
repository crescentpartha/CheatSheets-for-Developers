## Table of Contents

- [Numpy CheatSheet for Developers](#Numpy-cheatsheet-for-developers)
- [Introduction-What-is-Numpy?](#introduction-what-is-Numpy)
- [Key and Imports?](#Key-and-Imports)
- [Data Type In Numpy](#Data-types-in-numpy)
- [Save And Load Data](#Save-And-Load-Data)
- [Operations](#Operations)
- [Array Mathematics](#Array-Mathematics)
- [Functions](#Functions)



# Numpy CheatSheet for Developers

## Introduction-What-is-Numpy?

> A library consisting of **multidimensional array objects** and a collection of routines for processing those arrays. 
 
**[🔼Back to Top](#table-of-contents)**


# Key and Imports

We use following shorthand in the cheat sheet:
|Command | description|
|----------|-------------|
|`np`|import numpy library| 
|`np.array` |  The array object in NumPy|
|`np.array.shape`|The shape of an array is the number of elements in each dimension.|
|`np.array.reshape`|Reshaping means changing the shape of an array(Example 1-D to 2-D)|
|`np.zeros(3)` | 1D array of length 3 all zeros|
|`np.zeros((2,3))` | 2D array of all zeros|
|`np.zeros((3,2,4))` | 3D array of all zeros|
|`np.full((3,4),2)`| 3x4 array with all values 2|
|`np.random.rand(3,5)` | 3x5 array of random floats between 0 and 1 |
|`np.ones((3,4))` | 3x4 array with all values 1|
|`np.eye(4)` | 4x4 array of 0 with 1 on diagonal|

**[🔼Back to Top](#table-of-contents)**

# Data Types In Numpy

NumPy has some extra data types, and refer to data types with one character, like i for integers, u for unsigned integers etc.

Below is a list of all data types in NumPy and the characters used to represent them.

|Command | description|
|-------------|----------|
|`i`|  integer|
|`b `| boolean|
|`u`|  unsigned integer|
|`f`|  float|
|`c` | complex float|
|`m` | timedelta|
|`M` | datetime|
|`O`|  object|
|`S` | string|
|`U `| unicode string|
|`V`|  fixed chunk of memory for other type ( void )|


**[🔼Back to Top](#table-of-contents)**

# Save And Load Data

- Text/CSV files:

|Command | description|
|-------------|----------|
|`np.loadtxt('New_file.txt')` | From a text file|
|`np.genfromtxt('New_file.csv',delimiter=',') `| From a CSV file|
|`np.savetxt('New_file.txt',arr,delimiter=' ') `| Writes to a text file|
|`np.savetxt('New_file.csv',arr,delimiter=',') `| Writes to a CSV file|

- Properties:

|Command | description|
|-------------|----------|
|`array.size` | Returns number of elements in array|
|`array.shape` | Returns dimensions of array(rows,columns)|
|`array.dtype` | Returns type of elements in array|


**[🔼Back to Top](#table-of-contents)**

# Operations

- Copying

|keywords | description|
|-------------|----------|
|`np.copy(array)` | Copies array to new memory array.|
|`view(dtype)` | Creates view of array elements with type dtype|

- Sorting

|keywords | description|
|-------------|----------|
|`array.sort()` | Sorts array|
| `array.sort(axis=0)` | Sorts specific axis of array|
| `array.reshape(2,3)` | Reshapes array to 2 rows, 3 columns without changing data.|

- Adding

|keywords | description|
|-------------|----------|
|`np.append(array,values)`| Appends values to end of array|
|`np.insert(array,4,values)` | Inserts values into array before index 4|

- Removing

|keywords | description|
|-------------|----------|
|`np.delete(array,2,axis=0)` | Deletes row on index 2 of array|
|`np.delete(array,3,axis=1)` | Deletes column on index 3 of array|

- Combining

|keywords | description|
|-------------|----------|
|`np.concatenate((array1,array2),axis=0)` | Adds array2 as rows to the end of array1|
| `np.concatenate((array1,array2),axis=1)` | Adds array2 as columns to end of array1|

- Splitting

|keywords | description|
|-------------|----------|
|`np.split(array,3)` | Splits array into 3 sub|arrays|

- Indexing

|keywords | description|
|-------------|----------|
|`a[0]=5` | Assigns array element on index 0 the value 5|
| `a[2,3]=1` | Assigns array element on index [2][3] the value 1|

- Subseting

|keywords | description|
|-------------|----------|
| `a[2]`| Returns the element of index 2 in array a.|
|`a[3,5]` | Returns the 2D array element on index [3][5]|

- Slicing

|keywords | description|
|-------------|----------|
|`a[0:4]` | Returns the elements at indices 0,1,2,3|
|`a[0:4,3]`| Returns the elements on rows 0,1,2,3 at column 3|
|`a[:2]`| Returns the elements at indices 0,1|
|`a[:,1]` | Returns the elements at index 1 on all rows|

**[🔼Back to Top](#table-of-contents)**

# Array Mathematics

- Arithmetic Operations
|Operation type | Syntax|
|-------------|----------|
| Addition| np.add(a,b)|
| Subtraction| np.subtract(a,b)|
| Multiplication| np.multiply(a,b)|
| Division| np.divide(a,b)|
| Exponentiation| np.exp(a)|
| Square Root| np.sqrt(b)|

- Comparison

|Operations type| Syntax|
|-------------|----------|
| Element-wise| a==b|
| Array-wise| np.array_equal(a,b)|

**[🔼Back to Top](#table-of-contents)**


# Functions

|Operation Type | Syntax|
|-------------|----------|
|Array-wise Sum| a.sum()|
| Array-wise min value| a.min()|
| Array row max value| a.max(axis=0)|
| Mean| a.mean()|
| Median| a.median()|


**[🔼Back to Top](#table-of-contents)**


