Python Cheatsheet
===============================

Contents
--------
**&nbsp;&nbsp;&nbsp;** **1. Collections:** **&nbsp;** **[`List`](#list)**__,__ **[`Dictionary`](#dictionary)**__,__ **[`Set`](#set)**__,__ **[`Tuple`](#tuple)**__,__ **[`Range`](#range)**__,__ **[`Enumerate`](#enumerate)**__,__ **[`Iterator`](#iterator)**__,__ **[`Generator`](#generator)**__.__  
**&nbsp;&nbsp;&nbsp;** **2. Types:** **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**  **[`Type`](#type)**__,__ **[`String`](#string)**__,__ **[`Regular_Exp`](#regex)**__,__ **[`Format`](#format)**__,__ **[`Numbers`](#numbers-1)**__,__ **[`Combinatorics`](#combinatorics)**__,__ **[`Datetime`](#datetime)**__.__  
**&nbsp;&nbsp;&nbsp;** **3. Syntax:** **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**  **[`Args`](#arguments)**__,__ **[`Inline`](#inline)**__,__ **[`Import`](#imports)**__,__ **[`Decorator`](#decorator)**__,__ **[`Class`](#class)**__,__ **[`Duck_Types`](#duck-types)**__,__ **[`Enum`](#enum)**__,__ **[`Exception`](#exceptions)**__.__  
**&nbsp;&nbsp;&nbsp;** **4. System:** **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**  **[`Exit`](#exit)**__,__ **[`Print`](#print)**__,__ **[`Input`](#input)**__,__ **[`Command_Line_Arguments`](#command-line-arguments)**__,__ **[`Open`](#open)**__,__ **[`Path`](#paths)**__,__ **[`OS_Commands`](#os-commands)**__.__  
**&nbsp;&nbsp;&nbsp;** **5. Data:** **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**  **[`JSON`](#json)**__,__ **[`Pickle`](#pickle)**__,__ **[`CSV`](#csv)**__,__ **[`SQLite`](#sqlite)**__,__ **[`Bytes`](#bytes)**__,__ **[`Struct`](#struct)**__,__ **[`Array`](#array)**__,__ **[`Memory_View`](#memory-view)**__,__ **[`Deque`](#deque)**__.__  
**&nbsp;&nbsp;&nbsp;** **6. Advanced:** **&nbsp;&nbsp;&nbsp;**  **[`Threading`](#threading)**__,__ **[`Operator`](#operator)**__,__ **[`Introspection`](#introspection)**__,__ **[`Metaprograming`](#metaprogramming)**__,__ **[`Eval`](#eval)**__,__ **[`Coroutines`](#coroutines)**__.__  
**&nbsp;&nbsp;&nbsp;** **7. Libraries:** **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**  **[`Progress_Bar`](#progress-bar)**__,__ **[`Plot`](#plot)**__,__ **[`Table`](#table)**__,__ **[`Curses`](#curses)**__,__ **[`Logging`](#logging)**__,__ **[`Scraping`](#scraping)**__,__ **[`Web`](#web)**__,__ **[`Profile`](#profiling)**__,__  
**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;** **[`NumPy`](#numpy)**__,__ **[`Image`](#image)**__,__ **[`Audio`](#audio)**__,__ **[`Games`](#pygame)**__,__ **[`Data`](#pandas)**__.__


Main
----
```python
if __name__ == '__main__':     # Runs main() if file wasn't imported.
    main()
```


List
----
```python
<list> = <list>[<slice>]       # Or: <list>[from_inclusive : to_exclusive : ±step]
```

```python
<list>.append(<el>)            # Or: <list> += [<el>]
<list>.extend(<collection>)    # Or: <list> += <collection>
```

```python
<list>.sort()                  # Sorts in ascending order.
<list>.reverse()               # Reverses the list in-place.
<list> = sorted(<collection>)  # Returns a new sorted list.
<iter> = reversed(<list>)      # Returns reversed iterator.
```

```python
sum_of_elements  = sum(<collection>)
elementwise_sum  = [sum(pair) for pair in zip(list_a, list_b)]
sorted_by_second = sorted(<collection>, key=lambda el: el[1])
sorted_by_both   = sorted(<collection>, key=lambda el: (el[1], el[0]))
flatter_list     = list(itertools.chain.from_iterable(<list>))
product_of_elems = functools.reduce(lambda out, el: out * el, <collection>)
list_of_chars    = list(<str>)
```
* **For details about sorted(), min() and max() see [sortable](#sortable).**
* **Module [operator](#operator) provides functions itemgetter() and mul() that offer the same functionality as [lambda](#lambda) expressions above.**

```python
<list>.insert(<int>, <el>)     # Inserts item at index and moves the rest to the right.
<el>  = <list>.pop([<int>])    # Removes and returns item at index or from the end.
<int> = <list>.count(<el>)     # Returns number of occurrences. Also works on strings.
<int> = <list>.index(<el>)     # Returns index of the first occurrence or raises ValueError.
<list>.remove(<el>)            # Removes first occurrence of the item or raises ValueError.
<list>.clear()                 # Removes all items. Also works on dictionary and set.
```
