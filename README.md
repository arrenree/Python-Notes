# Python Notes by Allen
<a name="top"></a>

### 1. [Datatypes, Basic Math, and Variable Assignments](#section1)
1. [Datatypes](#datatypes)
2. [Basic Math](#basicmath)
3. [Floor Division](#floor)
4. [Modulo](#modulo)
5. [Powers](#powers)
6. [Square Root](#square_root)
7. [Variable Assignment](#var_assign)
8. [Variable Reassignment](#var_reassign)
9. [Dynamic Typing](#dynamic_typing)


### 2. [Strings](#strings)
1. [Types of Strings](#string_type)
2. [Printing a String](#string_print)
3. [Len()](#string_length)
4. [String Indexing](#string_indexing)
5. [String Slicing](#string_slicing)
6. [Reversing a String](#string_reverse)
7. [String Immutability](#string_immut)
8. [String_Concatenation](#string_con)
9. [Concatenating Numbers with Strings](#string_con_num)
10. [String Methods](#string_methods)
11. [String Formatting / String Interporlation](#string_format)
12. [% Placeholder](#string_percent)
13. [%s Method](#string_percent_s)
14. [%d Method](#string_percent_d)
15. [%r Method](#string_percent_r)
16. [Float Precision](#string_float)
17. [Multiple % Placeholder](#string_percent_multiple)
18. [.format() Method](#string_.format)
19. [.format() Indexing](#string_.format_index)
20. [.format() Float Formatting](#string_.format_float)
21. [f String Literal](#string_fstring)

### 3. [Lists](#lists)
1. [Indexing and Slicing](#list_index_slice)
2. [List Concatenation](#list_con)
3. [Duplicating Strings](#list_dup)
4. [Amend / Append](#list_append)
5. [Remove](#list_remove)
6. [Sort](#list_sort)
7. [Reverse](#list_reverse)
8. [Nested Lists](#list_nested)
9. [List Comprehensions](#list_comp)

### 4. [Dictionaries](#dictionaries)
1. [Retrieving Values](#dict_retrieve)
2. [Retrieving Nested Values](#dict_retrieve_nest)
3. [Creating Keys by Assignment](#dict_key_assign)
4. [Append](#dict_append)
5. [Upsert](#dict_upsert)

### 5. [Tuples](#tuples)

### 6. [Sets](#sets)

### 7. [Files](#files)
1. [Opening and Reading](#files_opening)
2. [Readlines Method](#files_readlines)
3. [Writing to File](#files_writing)
4. [Appending to File](#files_append)

### 8. [Comparison Operators](#comp_operator)
1. [Equals](#comp_equals)
2. [Does not Equal](#comp_notequals)
3. [Chained Comparison Operators](#comp_chain)
4. [Appending to File](#files_append)


### 9. [if, elif, else Statements](#if)

### 10. [for Loops](#for_loops)
1. [for Loop](#for_loop)
2. [for Loop, if Statement](#for_if)
3. [for Loop, if, else Statements](#for_if_else)
4. [Running Tally](#running_tally)
5. [for Loop with Strings](#for_strings)
6. [for Loop with Tuples](#for_tuple)
7. [Tuple Unpacking](#for_tuple)
8. [for Loop with Dictionaries](#for_dict)
9. [Dictionary Methods](#for_dict_methods)

### 11. [while Loops](#while_loops)
1. [break, continue, pass](#while_break)
2. [while Loops, if, else](#while_if)

### 12. [Useful Operators](#useful_operators)
1. [range](#op_range)
2. [enumerate](#op_enumerate)
3. [zip](#op_zip)
4. [in and not in Operator](#op_in)
5. [min and max](#op_min)
6. [Random - Shuffle](#op_shuffle)
7. [Random - Randint](#op_randint)
8. [input](#op_input)

### 13. [List Comprehensions](#list_comprehension)
1. [Square Numbers in Range](#list_comp_sq)
2. [Check for even numbers](#list_comp_even)
3. [Converting C to F](#list_comp_convert)
4. [Nested List Comprehensions](#list_comp_nested)
5. [Print words start with S](#list_comp_split)
6. [Print all even numbers in range](#list_comp_even_print)
7. [Return multiples of 3 in range](#list_comp_range_three)
8. [Return words with even lengths](#list_comp_even_word)
9. [Return words for multiples of 3](#list_comp_three_word)
10. [Return first letter every word in string](#list_comp_first_letter)

### 14. [Guessing Game Challenge](#guessing_game)

### 15. [Methods](#methods)

### 16. [Functions](#functions)
1. [Intro to Functions](#func_intro)
2. [Functions with Arguments](#func_arg)
3. [Return vs Print](#func_return)
4. [Check if number is even](#func_num_even)
5. [Check if any number in list is even](#func_num_list_even)
6. [Return even numbers in list](#func_return_num)


<hr>

<a name="section1"></a>
## 🔴 1. Datatypes, Basic Math, and Variable Assignments
[Top](#top)

<a name="datatypes"></a>
### 1. Datatypes

```python
Integers

# type int
# an int is a whole number, such as 2, 100, 300
```

```python
Floating Point

# type float
# a float is a number with a decimal point, such as 2.3
```

```python
Strings

# type str
# a string is an ordered sequence of characters
# can be double or single quotes
# "sammy"
# 'hello'
# "2000"
```

```python
Lists

# type list
# a list is an ordered sequence of objects
# can include various datatypes
# [10, "hello", 200.3]
```

```python
Tuple

# type tup
# a tuple is an ordered immutable sequence of objects
# immutable means cannot change an object in the sequence
# (10, "hello", 200.3)
```

```python
Dictionaries

# type dict
# a dictionary is an unordered key:value pair
# {"mykey":"value", "name","allen"}
```

```python
Sets

# type set
# a set is an unordered collection of unique objects
# {"a","b"}
```

```python
Booleans

# type bool
# a boolean is a logical value indicating true or false
```

<a name="basicmath"></a>
### 2. Basic Math

```python
Addition
1+1
# 2

Subtraction
3-1
#2

Multiplication
2*2
# 4

Division
6 / 2
# 1.5
```

<a name="floor"></a>
### 3. Floor Division

```python
7 // 4
# 1

# // = floor division. 
# truncates decimal without rounding
# should be 1.75, but rounds to 1
```
<a name="Modulo"></a>
### 4. Modulo or Mod

```python
7 % 3
# 3

# % is mod = the remainder after division
# useful in checking if number is even or odd

50 % 5
# 0
# even number, since leftover is 0
# if returns anything other than 0 = odd
```

<a name="powers"></a>
### 5. Powers

```python
2 ** 3
# 8
```

<a name="square_root"></a>
### 6. Square Root

```python
4 ** 0.5
# 2.0

# 4 to the power of 0.5 = square root
# returns a float
```
<a name="var_assign"></a>
### 7. Variable Assignments

```python
# cannot start with number
# cannot have spaces
# cannot use special symbols
# best practices all lowercase
# avoid special python phrases like 'list' and 'str'
# avoid single characters
```

```python
Variable Assignment

# task: create object called 'a' and assign it number 5
a = 5

# name = object
# we've assigned int object 5 to variable name a
```

<a name="var_reassign"></a>
### 8. Variable Reassignments

```python
a = 10

a = a + a
# 20

# another way of saying this
a += 10
# 30
# same as a = a + 10

type (a)
int

# to check what datatype variable a is, use type()
```

<a name="dynamic_typing"></a>
### 9. Dynamic Typing

```python
# python uses dynamic typing, which means you can reassign variables to different data types

dogs = 2
dogs = ["sammy","frankie"]

# this is okay!
# initially assigned dog to an int
# reassigned as string

# statically-typed means you can't re-assign variables
```

<a name="strings"></a>
## 🔴 2. Strings
[Top](#top)

```python
# strings are a sequence of characters using single or double qoutes
# 'hello' "hello"
# since strings are ordered sequences, we can use indexing
```

<a name="string_type"></a>
### 1. Types of Strings

```python
# single word strings
'hello'

# entire prhase strings
'this is also a string'

# double quotes
"string with double quotes"
```

<a name="string_print"></a>
### 2. Printing a String

```python
print("hello")
# hello

# print will export the results, removing the parathesis
```

```python
print("hello \n world")
# hello
#  world

# the \n is a break sequence that starts new line
```

```python
print("hello \t world")
# hello   world

# \t is another break sequence that is the same as tab
```

<a name="string_length"></a>
### 3. len()

```python
len('hello world')
# 11

# use len to check length of a string
```

<a name="string_indexing"></a>
### 4. String Indexing

```python
# strings are ordered sequences, so can use indexing or slicing to grab sub-sections
# indexing starts at 0
# indexing uses [ ] and allows you to grab single characters
# can also do reverse indexing -1
```

```python
mystring = "Hello World"
mystring[0]
# H

# retrieve object from index position 0 from string "hello world"
```

```python
len(mystring)
# 11

# how many elements are in string mystring
```

```python
mystring = "Hello World"
mystring[-2]
# 'l'

# negative indexing
# retrieve object from index position -2 from mystring
```

<a name="string_slicing"></a>
### 5. String Slicing

```python
# slicing allows you to grab multiple characters
# syntax [ start:stop:step]
# stop = index you go up to, but NOT include
# step = size of the jump you take
```

```python
mystring[0:3:1]
# 'Hel'

# starts at 0, goes up to, but NOT include index 4 (l), 1 step
```

```python
mystring[ :3]
# 'Hel'
```

```python
mystring[::]
# 'Hello World'

# take everything from string
```

```python
mystring[::2]
# 'HloWrd'

# take all elements in step sizes of 2 
```

<a name="string_reverse"></a>
### 6. Reversing a String

```python
# how do you reverse a string?

mystring[::-1]
# 'dlroW olleH'

# using -1 step reverses the string
```

<a name="string_immut"></a>
### 7. String Immutability

```python
# strings are immutable. 
# once a string is created, the elements within it cannot be changed or replaced
# nor can it be re-assigned to something else

# say you want to reassign s to p
name = "Sam"
name[0] = 'P'

# error. you can't reassign the S to a P in a string
# need to use concatenation
```

<a name="string_con"></a>
### 8. String Concatention

```python
name = "Sam"
last_letters = name[1:]
last_letters
# 'am'

'P' + last_letters
# 'Pam'

# can use + to concatenate strings
# extracted 'am' from the original string 'Sam'
# concatenated with 'P' to produce 'Pam'
```

```python
x = 'Hello World'
x + ' it is a good day'
# 'Hello World it is a good day'
```

```python
letter = 'z'
letter * 10
# 'zzzzzzzzzz'
```

<a name="string_con_num"></a>
### 9. Concatenating Numbers with strings

```python
# you will get an error if concatenate numbers with string
2 + 3
# 5

'2' + '3'
'23'
# 2 and 3 are strings, so if you add them together, becomes 23
# and not 5
```

<a name="string_methods"></a>
### 10. String Methods

```python
# objects in python have built in methods
# methods are functions inside the object that can perform actions on object itself
# methods are in the form:

object.method(parameters)

# parameters are the extra arguments we can pass into the method
```

```python
# uppercase function

x = 'Hello World'
x.upper()
# 'HELLO WORLD'

# this method is not "in place"
# doesnt affect the original string
```

```python
# lowercase function

x = 'Hello World'
x.lower()
# 'hello world'
```

```python
# split string function

x.split()
# ['Hello','World']

# split() will take a string and split it based on the white space
```

```python
x = 'Hi this is a string'
x.split()
# ['Hi','this', 'is', 'a', 'string']
```

```python
# you can also split on specific letters

x.split('i')
# ['H', ' th', 's ', 's a str', 'ng']
```

Print Function

```python
print ("hello world")
# hello world

# prints everything within the parathesis
```

<a name="string_format"></a>
### String Formatting (String Interporlation)

```python
# allows you to inject items into a string rather than trying to chain items
# together using commas or concatenation
# 3 methods:
# 1) placeholders using % (oldest)
# 2) .format() method (improved technique)
# 3) f-string literals (newer)
```

<a name="string_percent"></a>
### % Placeholder

```python

print("I'm going to inject %s here." %'something')
# I'm going to inject something here

# uses %s as a placeholder
# referred to as string formatting operator
```

```python
# can pass multiple items by placing them inside tuple

print("I'm going to inject %s text here, and %s text here." %('some','more'))
# I'm going to inject some text here, and more text here.
```

```python
# can also pass variable names

x, y = 'some', 'more'
print("I'm going to inject %s text here, and %s text here."%(x,y))
# I'm going to inject some text here, and more text here
```

<a name="string_percent_e"></a>
### %s Method

```python
# %s Method

print('He said his name was %s.' %'Fred')
# He said his name was Fred.

# %s doesn't include the ' ' 
# converts whatever it sees into a string (including int and float)

print('I wrote %s programs today.' %3.75)
# i wrote 3.75 programs today.

# converted float 3.75 into a string
```

<a name="string_percent_e"></a>
### %d Method

```python
# %d operator converts numbers to ints first, without rounding

print('I wrote %d programs today.' %3.75)  
# I wrote 3 programs today.

# converts float 3.75 to int (no rounding)
```

<a name="string_percent_r"></a>
### %r Method

```python
# %r Method

print('He said his name was %r.' %'Fred')
# He said his name was 'Fred'.

# %r includes the 'quotes'
```
<a name="string_float"></a>
### Float Precision

```python
# floats use format %5.2f
# 5 = min number of chars in string
# .2f = how many number to show past decimal point
```

```python
# %5.2f Example

print('Floating point numbers: %5.2f' %(13.144))
# Floating point numbers: 13.14

# converts 13.144 to a string
# the .2f = 2 numbers past decimal
```

```python
# %1.0f Example

print('Floating point numbers: %1.0f' %(13.144))
# Floating point numbers: 13

# .0f = 0 places past decimal
```

```python
# 1.5f Example

print('Floating point numbers: %1.5f' %(13.144))
# Floating point numbers: 13.14400
```

```python
# 10.2f Example

print('Floating point numbers: %10.2f' %(13.144))
# Floating point numbers:      13.14

# notice all the whitespace before the float
```

```python
# 25.2f Example

print('Floating point numbers: %25.2f' %(13.144))
# Floating point numbers:                     13.14

# notice all the whitespace before the float
```

<a name="string_percent_multiple"></a>
### Multiple % Placeholder Formatting

```python
# can have multiple different conversion tools

print('First: %s, Second: %5.2f, Third: %r' %('hi!',3.1415,'bye!'))
# First: hi!, Second:  3.14, Third: 'bye!'

# %s & 'hi!' = First: hi!
# %5.2f & 3.1415 = Second:  3.14
# %r & 'bye!' = Third: 'bye!'
```
<a name="string_.format"></a>
### .format() Method

```python
print('this is a string {} '.format('INSERTED'))
# this is a string INSERTED

# .format() takes string 'INSERTED' and places it in {}
```

```python
# .format takes strings and replaces {} in sequential order

print ('the {} {} {}'.format('fox','brown','quick'))
# the fox brown quick
```
<a name="string_.format_index"></a>
### .format() Indexing

```python
# inserted objects can be called by index position

print ('the {2} {1} {0}'.format('fox','brown','quick'))
# the quick brown fox
```

```python
# can call same object multiple times

print ('the {0} {0} {0}'.format('fox','brown','quick'))
# the fox fox fox
```

```python
# inserted objects can be assigned keywords

print ('the {q} {b} {f}'.format(f='fox',b='brown',q='quick'))
```

```python
result = 100/777
# 0.128700

print ('the result was {}'.format(result))
# the result was 0.128700
```

```python
print ('the result was {r}'.format(r = result))
# the result was 0.128700

# same thing as above
# assigned keywords to inserted objects
```
<a name="string_.format_float"></a>
### .format() Float Formatting 

```python
# float formatting follows "{value:width.precision f}"

print ('the result was {r:1.3f}'.format(r=result))
# the result was 0.129

# r = value
# 1 = width = how "wide" the entire result will be (whitespace) 
# .3 = level of precision = places past decimal point
# 0.129

print ('the result was {r:10.3f}'.format(r=result))
# the result was       0.129

# so by changing the width to 10, you add whitespace
```

```python
print('{0:8} | {1:9}'.format('Fruit', 'Quantity'))
print('{0:8} | {1:9}'.format('Apples', 3.))
print('{0:8} | {1:9}'.format('Oranges', 10))

Fruit    | Quantity 
Apples   |       3.0
Oranges  |        10

```

```python
print('{0:<8} | {1:^8} | {2:>8}'.format('Left','Center','Right'))
print('{0:<8} | {1:^8} | {2:>8}'.format(11,22,33))

Left     |  Center  |    Right
11       |    22    |       33

# can use < ^ > to set alignment
```
<a name="string_.fstring"></a>
### f String Literal

```python
name = "Jose"
print(f'Hello, his name is {name}')
# Hello, his name is Jose

# allows you to bring outside variables immediately into string 
```

```python
name = "Jose"
print(f'Hello, his name is {name!r}')
# Hello, his name is 'Jose'

# allows you to bring outside variables immediately into string 
```

```python
name = "Sam"
age = 3
print(f'{name} is {age} years old')
# same is 3 years old
```

<a name="lists"></a>
## 🔴 3. Lists
[Top](#top)


```python
# Lists are ordered sequences that can hold a variety of object types
# use [ ] brackets and commas to separate objects in list
# lists support indexing and slicing
# lists have no fixed size (don't have to specify how big a list will be)
# lists have no fixed type (can have multiple data types)
# lists can be nested
```

```python
# list of int

my_list = [1,2,3]
```

```python
# list of string, int, float

my_list = ['STRING',100,23.2]
```

```python
# how many items in list? use len()

len(my_list)
# 3

# 3 items in list
```

<a name="list_index_slice"></a>
### Indexing and Slicing

```python
mylist = ['one','two','three']
mylist[0]
# 'one'
```

```python
mylist = ['one','two','three']
mylist[1:]
# 'two','three'

# grab index 1 and everything past it
```

```python
mylist = ['one','two','three']
mylist[:2]
# 'one','two'

# grab everything UP, but not including index 2
```

<a name="list_con"></a>
### Lists Concatenation

```python
mylist = ['one','two,'three']
another_list = ['four','five']

new_list = mylist + another_list
new_list
# ['one','two','three','four','five']

# this doesn't actually change the original list
# have to reassign the list to make it permanent

mylist = mylist + another_list
mylist
# ['one','two','three','four','five']

```

<a name="list_dup"></a>
### Duplicating Strings

```python
list = ['alpha','bravo']
list * 2
# ['alpha', 'bravo', 'alpha', 'bravo']
```

<a name="list_append"></a>
### Amend / Append

```python
new_list[0] = 'ONE ALL CAPS'
new_list
# ['ONE ALL CAPS', 'two','three','four','five']
```

Lists - Append Elements

```python
new_list = ['ONE ALL CAPS', 'two','three','four','five']
new_list.append('six')
new_list
# ['ONE ALL CAPS', 'two','three','four','five','six']

# adds element to end of list
# appends in place, which means it permanently changes the list
```

<a name="list_remove"></a>
### Remove

```python
new_list = ['ONE ALL CAPS', 'two','three','four','five','six']
new_list.pop()
# 'six'

new_list
# ['ONE ALL CAPS', 'two','three','four','five']

# popped off 'six', removed from end of list
```

```python
# to save the popped item, save it as a varaible

popped_item = new_list.pop()
popped_item
# 'six'

# by default, will pop off -1 index position
```

```python
# can also use index position to remove elements

new_list.pop(0)
new_list
# ['two','three','four','five']

# removes element 0 = 'ONE ALL CAPS'
```

<a name="list_sort"></a>
### Sort

```python
new_list = ['a','e','x','b','c']
num_list = [4,1,8,3]

new_list.sort() 
new_list
# ['a', 'b', 'c', 'e', 'x']
# doesnt return anything, simply sorts list in place
```

You cannot assign sorted list as a variable

```python
new_sorted_list = new_list.sort()

# this doesnt work because .sort doesnt return anything
# so nothing gets assigned to your new variable
```

To assign a sorted list, need to do this:

```python
new_list.sort()
my_sorted_list = new_list
my_sorted_list
# ['a', 'b', 'c', 'e', 'x']

# sort list first
# then assign the sorted list to a new variable
# now when you call the new variable, the list will be sorted
```

```python
num_list = [4,1,8,3]

num_list.sort()
sorted_num_list = num_list
sorted_num_list
# [1,3,4,8]
```

<a name="list_reverse"></a>
### Reverse

```python
num_list.reverse()
num_list
# [8,4,3,1]
```

<a name="list_nested"></a>
### Nested Lists

```python
list_1=[1,2,3]
list_2=[4,5,6]
list_3=[7,8,9]

# Make a list of lists to form a matrix
matrix = [list_1,list_2,list_3]
# [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

```python
# indexing nested lists

matrix[0]
# [1,2,3]

# grabs first element/row of matrix
```

```python
matrix[0][0]
# 1

# grab the first element of the first row
```
<a name="list_comp"></a>
### List Comprehensions

```python
# advanced feature which allow for quick construction of lists
# build a list comprehension by deconstructing a for loop within a [ ]

first_col = [row[0] for row in matrix]
first_col
# [1,4,7]

# used list comprehension to grab first element of every row in matrix
```

<a name="dictionaries"></a>
## 🔴 4. Dictionaries
[Top](#top)

```python
# dictionaries are unordered mappings for storing objects to keys
# use a key-value pairing instead
# allows users to quickly grab objects without index location
# also known as hash tables
# objects retrieved by key name
# unordered and cannot be sorted
```

```python
# difference between lists and dictionaries?

# lists are objects retrieved by index location
# lists are ordered sequence; can be indexed or sliced
```

<a name="dict_retrieve"></a>
### Retrieving Values

```python
my_dict = {'key1':'value1','key2':'value2'}
my_dict['key1']
# 'value1'

# calling a key retrieves its value
``` 

```python
prices_lookup = {'apple':2.99,'oranges':1.99,'milk':5.80}
prices_lookup['apple']
# 2.99

# without knowing index location, can lookup price of an apple
# this is the power of dictionaries
```

<a name="dict_retrieve_nest"></a>
### Retrieving Nested Values

```python
d = {'k1':123,'k2':[0,1,2],'k3':{'insidekey':100}}

# dict can contain int, a list, and another dict

d['k2']
# [0,1,2]

d['k2'][2]
# 2

d['k3']['insidekey']
# 100
```

Dictionary - Affecting Values

```python
my_dict = {'key1':100,'key2': 200,'key3':300}
my_dict['key1'] - 50
# 50

# retrieved the value for key1 and subtracted 50
```

```python
my_dict['key1'] -= 100
my_dict['key1']
# 0

# -= is the same as key1 = key1 - 100
```

<a name="dict_key_assign"></a>
### Creating Keys by Assignment

```python
# lets say you have an empty dictionary
d = {}

# create a new key through assignement
d['animal'] = 'Dog'

# you've now appended animal (key) with dog (value)

# can do this with any object
d['num'] = 42
d
# {'animal': 'Dog', 'answer': 42}
```

<a name="dict_append"></a>
### Append

```python
d = {'k1': 100,'k2':200}
d['k3'] = 300
d
# {'k1': 100, 'k2': 200, 'k3': 300}

# added key/value pair of k3/300
```

<a name="dict_upsert"></a>
### Upsert

```python
d = {'k1': 100,'k2':200}
d['k1'] = 'NEW ITEM'
d
# {'k1': 'NEW ITEM', 'k2': 200, 'k3': 300}
```

Dictionary - Extract all keys

```python
d.keys()
# dict_keys(['k1', 'k2', 'k3'])
```

Dictionary - Extract all values

```python
d.values()
# dict_values(['NEW ITEM', 200, 300])
```

<a name="tuples"></a>
## 🔴 5. Tuples
[Top](#top)

```python
# very simliar to lists, except they are immutable
# immutable = cannot be changed
# once element is inside tuple, cannot be reassigned
# useful for things like days of the week, or dates on a calendar
# tuples use parathesis (1,2,3)
```

```python
t = (1,2,3)

# this is a tuple
```

```python
# can use indexing

t[0]
# 1

# can also use slicing
t[-1]
# 3
```

Basic Tuple Methods

```python
# .index to enter a value and return the index position

t.index(2)
# 1

# value 2 is located in index position 1
```

```python
# .count to count number of times a value appears

t = (1, 1, 1, 2, 2, 2, 3, 3, 3)
t.count(1)
# 3

# 1 appears 3x in the tupple
```

<a name="Sets"></a>
## 🔴 6. Sets
[Top](#top)


```python
# sets are unordered collection of unique elements
# use set() function
```

```python
# create empty set

x = set()
```

```python
# add 1 to the set

x.add(1)
x
# {1}

# used the .add() method to add 1 to the set
```

```python
# now try to add 1 again to the set

x.add(1)
x
# {1}

# doesn't duplicate since only saves unique elements
```

```python
# cast a list of duplicates as a set to retain only unique elements

list1 = [1,1,2,2,3,4,5,5]
set(list1)
# {1, 2, 3, 4, 5}

# set now only contains unique elements
```

<a name="files"></a>
## 🔴 7. Files
[Top](#top)

```python
# python uses file objects to interact with external files on your computer
# python has built in open function that allows us to open file types
# 1) need to first OPEN file
# 2) then can READ file
```

<a name="files_opening"></a>
### Opening and Reading

```python
# create simple test.txt file

# open txt files

myfile = open('test.txt')

# now the test.txt file is "opened"
```

```python
# read the txt file

myfile.read()
# 'Hello, this is a quick test file.'
```

```python
# what happens if you try to read it again?

myfile.read()
''

# this is because the reading "cursor" is at end of file after having read it
# need to reset the cursor

myfile.seek(0)
# 0

# seek to the start of file (index 0)
```

```python
# now, you can read it again

myfile.read()
# 'Hello, this is a quick test file.'
```

<a name="files_readlines"></a>
### Readlines Method

```python
# readlines returns a list of the lines in the file

myfile.seek(0) # resets cursor to beginning
myfile.readlines()
# ['Hello, this is a quick test file.']
```

```python
# close file after you're finished with it
myfile.close()
```

<a name="files_writing"></a>
### Writing to File

```python
# by default, the open() function only allows us to read the file
# need to pass argument 'w' to write over file

myfile = open('test.txt','w+')

# adding a second argument to function, 'w' stands for write
# 'w+' = read and write to the file
```

```python
# careful! opening a file with 'w' or 'w+' truncates original, meaning
# anything in the original file is deleted!

myfile = open('test.txt','w+') # opens + writes file
myfile.write('this is a new line') # overwrites file
myfile.seek(0) # resets cursor
myfile.read() # reads file
# 'this is a new line'

myfile.close() # good habit to close files when finished
```

<a name="files_append"></a>
### Appending to File

```python
# passing argument 'a' opens the file and puts the pointer at the end
# so anything written is appended
# a+ lets us read and write to a file
# if the file does not exist, one will be created
```

```python
myfile = open('test.txt','a+')
myfile.write('\n this text is being appended')
myfile.write('\nAnd another line here')

myfile.seek(0) # since a+ moves cursor to end, need to reset cursor
myfile.read()
# 'this is a new line\n this text is being appended\nAnd another line here

# printing the .txt file is cleaner

print(myfile.read())

# this is a new line
#  this text is being appended
# And another line here

myfile.close()
```

<a name="comp_operator"></a>
## 🔴 8. Comparison Operators
[Top](#top)

```python
# allows us to compare variables and output a boolean (True or False)
```

<a name="comp_equals"></a>
### Equals

```python
2 == 2
# True
```

<a name="comp_notequals"></a>
### Does not Equal

```python
2 != 3
# True. 2 does not equal 3. Statement is true.

2 != 2
# False. 2 does not equal 2. Statement is false.
```

<a name="comp_chain"></a>
### Chained Comparison Operators

```python
1 < 2 < 3
# True
```

```python
1 < 2 and 2 < 3
# True

# AND = both statements HAVE to be true for it to be true
```

```python
1 == 2 or 2 < 3
# True

# OR = only one of the statements need to be true
```

<a name="if"></a>
## 🔴 9. if, elif, else Statements
[Top](#top)

```python
# if = if this happens, perform this action

# elif = if this happens, perform A. Else, if something else happens, perform B. Else, if none of the above cases happen, perform C.

if case1:
    perform action1
elif case2:
    perform action2
else:
    perform action3
```

Examples

```python
x = False

if x:
    print('x was True!')
else:
    print('I will be printed in any case where x is not true')
# I will be printed in any case where x is not true

# since x is not true, first action is skipped, goes to 2nd action
```

```python
loc = 'Bank'

if loc == 'Auto Shop':
    print('Welcome to the Auto Shop!')
elif loc == 'Bank':
    print('Welcome to the bank!')
else:
    print('Where are you?')

# Welcome to the bank!
```

```python
person = 'Sammy'

if person == 'Sammy':
    print('Welcome Sammy!')
else:
    print("Welcome, what's your name?")
  
# Welcome Sammy!
```

```python
person = 'George'

if person == 'Sammy':
    print('Welcome Sammy!')
elif person =='George':
    print('Welcome George!')
else:
    print("Welcome, what's your name?")
  
# Welcome George!
```

<a name="for_loops"></a>
## 🔴 10. for Loops
[Top](#top)

```python
# for loops act as an iterator in python
# it goes through items that are in a sequence or any other iterable item

for item in object:
    statements to do stuff

# variable name used for the item is up to coder
```

<a name="for_loop"></a>
### for Loop

```python
list1 = [1,2,3,4]

for num in list1:
    print(num)

# 1
# 2
# 3
# 4
```

<a name="for_if"></a>
### for Loop, if Statements

```python
# print only even numbers

list1 = [1,2,3,4]

for num in list1:
    if num % 2 == 0:  # mod = 0 means even number
        print(num)

# 2
# 4
```

<a name="for_if_else"></a>
### for Loop, if, else Statements

```python
list1 = [1,2,3,4]

for num in list1:
    if num % 2 == 0:  # mod = 0 means even number
        print(num)
    else:
        print('Odd number')

# Odd number
# 2
# Odd number
# 4
```

<a name="running_tally"></a>
### Running Tally

```python
list1 = [1,2,3,4,5,6,7,8,9,10]

# running tally starts at zero
list_sum = 0

for num in list1:
    list_sum = list_sum + num

print(list_sum)

# 55

# iterate through every element in list1
# add element to list_sum (starting as 0)
```

```python
# another form of syntax (using +=)

list1 = [1,2,3,4,5,6,7,8,9,10]

list_sum = 0

for num in list1:
    list_sum += num

print(list_sum)

# 55
```

<a name="for_strings"></a>
### for Loop with Strings

```python

for letter in 'hello':
    print(letter)

# h
# e
# l
# l
# o
    
# for every element (variable = letter) in string 'hello'
# print out each element
```

<a name="for_tuple"></a>
### for Loop with Tuples

```python
tup = (1,2,3,4,5)

for t in tup:
    print(t)

# 1    
# 2
# 3   
# 4
# 5

# for every element in tuple (defined above)
# print the element
```

<a name="for_tuple"></a>
### Tuple Unpacking

```
# tuples have a special quality when it comes to for loops
# if you are iterating through a tuple, the item can be tuple itself
# this is called tuple unpacking
# doing so can access the individual items inside that tuple
```

```python
list2 = [(2,4),(6,8),(10,12)]

for tup in list2:
    print(tup)

# (2,4)
# (6,8)
# (10,12)

# for every element in list2 (3 elements)
# print each element
```

```python
# now using tuple unpacking

for (t1,t2) in list2:
    print(t1)

# 2
# 6
# 10

# for each tuple in list, print first element of the tuple
```

<a name="for_dict"></a>
### for Loop with Dictionaries

```python

d = {'k1':1,'k2':2,'k3':3}

for item in d:
    print(item)
    
# k1
# k2
# k3

# for each element (key/value) in d (dictionary)
# notice this only prints the keys
```

<a name="for_dict_methods"></a>
### Dictionary methods

```python
# .items() method

d = {'k1':1,'k2':2,'k3':3}

d.items()

# dict_items([('k1', 1), ('k2', 2), ('k3', 3)])

# .items() returns all items in dictionary
```

```python
# iteration through .items() method

d = {'k1':1,'k2':2,'k3':3}

for k, v, in d.items():
    print(k)
    print(v)
    
# k1
# 1
# k2
# 2
# k3
# 3
```

```python
# .keys() method

d = {'k1':1,'k2':2,'k3':3}

d.keys()
# dict_keys(['k1', 'k2', 'k3'])

# .keys() retrieves the keys from dictionary d

list(d.keys())
# ['k1', 'k2', 'k3']

# cast result of .keys() as a list
```

```python
# sorted() method on .values() method

d = {'k1':1,'k2':2,'k3':3}

sorted(d.values())
# [1, 2, 3]

# using the sorted() method to obtain a sorted list
```

<a name="while_loops"></a>
## 🔴 11. while Loops
[Top](#top)

```python
# while statement will repeatedly execute as long as condition is true
# loop because code will continue looping until condition is no longer met
```

```python
x = 0

while x < 5:
    print('x is currently: ',x)
    print(' x is still less than 5, adding 1 to x')
    x+=1

# x is currently:  0
#  x is still less than 5, adding 1 to x
# x is currently:  1
#  x is still less than 5, adding 1 to x
# x is currently:  2
#  x is still less than 5, adding 1 to x
# x is currently:  3
#  x is still less than 5, adding 1 to x
# x is currently:  4
#  x is still less than 5, adding 1 to x

# so the while loop keeps running until x isnt < 5
```

same thing, but adding an else statement

```python
x = 0

while x < 5:
    print('x is currently: ',x)
    print(' x is still less than 5, adding 1 to x')
    x+=1
else:
    print('All done!')

# x is currently:  0
#  x is still less than 5, adding 1 to x
# x is currently:  1
#  x is still less than 5, adding 1 to x
# x is currently:  2
#  x is still less than 5, adding 1 to x
# x is currently:  3
#  x is still less than 5, adding 1 to x
# x is currently:  4
#  x is still less than 5, adding 1 to x
# All done!

# while loop keeps running until x isnt < 5
# then it executes the else statement
```

<a name="while_break"></a>
### break, continue, pass

```python
# break - breaks out of the current loop
# continue - goes to the top of current loop
# pass - does nothing at all
```

```python
x = 0

while x < 5:
    print('x is currently: ',x)
    print(' x is still less than 5, adding 1 to x')
    x+=1
    if x==3:
        print('x==3')
    else:
        print('continuing...')
        continue
        
x is currently:  0
 x is still less than 5, adding 1 to x
continuing...
x is currently:  1
 x is still less than 5, adding 1 to x
continuing...
x is currently:  2
 x is still less than 5, adding 1 to x
x==3
x is currently:  3
 x is still less than 5, adding 1 to x
continuing...
x is currently:  4
 x is still less than 5, adding 1 to x
continuing...

# so once x+=1 becomes 3
# prints x==3
# continues the outer while loop
# and since 3 < 5, prints x is less than 5, etc.
```

<a name="while_if"></a>
### while Loop, if, else

```python
x = 0

while x < 5:
    print('x is currently: ',x)
    print(' x is still less than 5, adding 1 to x')
    x+=1
    if x==3:
        print('Breaking because x==3')
        break
    else:
        print('continuing...')
        continue
        
x is currently:  0
 x is still less than 10, adding 1 to x
continuing...
x is currently:  1
 x is still less than 10, adding 1 to x
continuing...
x is currently:  2
 x is still less than 10, adding 1 to x
Breaking because x==3

# once x+=1 is 3, prints 'breaking bc x==3
# then breaks out of this loop (stops executing)
```

<a name="useful_operators"></a>
## 🔴 12. Useful Operators
[Top](#top)

<a name="op_range"></a>
### Range

```python
# range() allows you to quickly generate a list of integers
# start, stop, and step parameter
```

```python
range(0,11)
# range(0,11)

# range() is a generator function
# to get a list out of it, we need to cast it to a list()
# generator functions generate info but does not save to memory

list(range(0,11))
# [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# so generates from 0 up to, but not including 11
# and is cast as a list()
```

```python
# third parameter is step size

list(range(0,11,2))
# [0, 2, 4, 6, 8, 10]
```

<a name="op_enumerate"></a>
### Enumerate

```python
index_count = 0

for letter in 'abcde':
    print("At index {} the letter is {}".format(index_count,letter))
    index_count +=1

At index 0 the letter is a
At index 1 the letter is b
At index 2 the letter is c
At index 3 the letter is d
At index 4 the letter is e

# for every element in string 'abcde', use indexing to insert objects into {} 
# then index_count becomes +1, and iterates through again
```

```python
# enumerate()
# keeping track of how many loops you've gone through is so common 
# that enumerate was created so you don't have to keep creating
# the index_count variable

enumerate('abcde')
# <enumerate object at 0x0000027FC8B4BD00>
# to see what you actually enumerated, cast as list

list(enumerate('abcde'))
[(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd'), (4, 'e')]

# enumerate creates list of tuples from your string!
# so you can use tuple unpacking method!
```

```python
for num,letter in enumerate('abcde'):
    print("At index {} the letter is {}".format(num,letter))

At index 0 the letter is a
At index 1 the letter is b
At index 2 the letter is c
At index 3 the letter is d
At index 4 the letter is e

# enumerate turns string 'abcde' into a list of tuples (index position, letter)
# then use for loop for tuple unpacking! (num,letter) 
```

<a name="op_zip"></a>
### Zip

```python
# zip() function allows you to create a list of tuples by "zipping" together 2 lists

mylist1 = [1,2,3,4,5]
mylist2 = ['a','b','c','d','e']

zip(mylist1,mylist2)
# <zip at 0x1d205086f08>

# generates your zipped list, to view, need to cast as list

list(zip(mylist1,mylist2))

# [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd'), (5, 'e')]
```

```python
for item1, item2 in zip(mylist1,mylist2):
    print('For this tuple, first item was {} and second item was {}'.format(item1,item2))

For this tuple, first item was 1 and second item was a
For this tuple, first item was 2 and second item was b
For this tuple, first item was 3 and second item was c
For this tuple, first item was 4 and second item was d
For this tuple, first item was 5 and second item was e
```

<a name="op_in"></a>
### in/not in operator

```python

'x' in ['x','y','z']
# True

'x' in [1,2,3]
# False
```

not in

```python

'x' not in ['x','y','z']
# False

'x' not in [1,2,3]
# True
```

<a name="op_min"></a>
### Min and Max

```python
mylist = [10,20,30,40,100]
min(mylist)
# 10

max(mylist)
# 100
```

<a name="op_shuffle"></a>
### Random - Shuffle

```python
# python comes with built in random library

from random import shuffle

# this shuffles the list "in place" so it wont
# return anything, inistead it will effect the list passed

shuffle(mylist)

mylist
# [40, 10, 100, 30, 20]
```

<a name="op_randint"></a>
### Random - Randint

```python
from random import randint

# return random integer in range [a,b], including both end points

randint(0,100)
# 25
```

<a name="op_input"></a>
### Input

```python

input('Enter something in this box: ')
# Enter something in this box: []
# Enter something in this box: [hello]
# 'hello'
```

<a name="list_comprehension"></a>
## 🔴 13. List Comprehensions
[Top](#top)


```q
# list comprehensions allow us to build lists using different notation
# essentially a one line for loop built inside brackets
```

```python
# grab every letter in string

list1 = [x for x in 'word']
list1
# ['w','o','r','d']

# return x for every x in string 'word'
```

<a name="list_comp_sq"></a>
### Square Numbers in Range

```python
list2 = [x**2 for x in range(0,11)]
list2
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# return x**2 for every x in range 0-10
```

<a name="list_comp_even"></a>
### Check for even numbers

```python
# check for even numbers in a range

list3 = [x for x in range(11) if x % 2 == 0]
list3
# [0,2,4,6,8,10]

# return x for every x in range 0-10, if x % 2 = 0
# ie, return every even number
```

<a name="list_comp_convert"></a>
### Converting Celsius to Fahrenheit

```python
# convert celsius to fahrenheit

celsius = [0,10, 20.1, 34.5]
fahrenheit = [((9/5) * temp + 32) for temp in celsius]

fahrenheit
# [32.0, 50.0, 68.18, 94.1]

# first you define a list celsius
# return variable 'temp' for every 'temp' in list celsius
```

<a name="list_comp_nested"></a>
### Nested List Comprehensions

```python
list4 = [x**2 for x in [x**2 for x in range(11)]]
list4
# [0, 1, 16, 81, 256, 625, 1296, 2401, 4096, 6561, 10000]

# start with inside bracket
# return x**2 for every x in range of 0-10
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
# then go to outside bracket
# return x**2 for every element in [ ]
# 0, 1, 16, 81, 256, 625, 1296, 2401, 4096, 6561, 10000
```

<a name="list_comp_split"></a>
### Print words that start with S

```python
# Use for, .split(), and if to create a Statement that will print out words that start with 's':

st = 'Print only the words that start with s in this sentence'

for word in st.split()
    if word[0] == 's':
        print(word)
     
# start
# s
# sentence
```

<a name="list_comp_even_print"></a>
### Print all even numbers in range

```python
list(range(0,11,2))
# [0,2,4,6,8,10]

# step 2 will automatically go from 0 to 2 and include all even numbers
```

<a name="list_comp_range_three"></a>
### Return multiples of 3 in range

```python
[x for x in range(1,51) if x%3 == 0]
# [3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48]

# return x for every x in range 1-50
# x % 3 = 0 means every multiple of 3
```

<a name="list_comp_even_word"></a>
### Return words with even lengths

```python
st = 'Print every word in this sentence that has an even number of letters'

for word in st.split():
    if len(word)%2 == 0:
        print(word+" <-- has an even length!")
   
word <-- has an even length!
in <-- has an even length!
this <-- has an even length!
sentence <-- has an even length!
that <-- has an even length!
an <-- has an even length!
even <-- has an even length!
number <-- has an even length!
of <-- has an even length!  

# need to split string.
# for every element (word) in string st
# if the length of word is even (length mod 2 = 0)
# print element (word) + string
```

<a name="list_comp_three_word"></a>
### Return words for multiples of 3

```python
# print integers from 1 to 100
# for multiples of 3, print "Fizz" instead of the number
# for multiples of 5, print "Buzz"
# for multiples of both 3 and 5, print "Fizzbuzz"

for num in range(1,101):
    if num % 3 == 0 and num % 5 == 0:
        print("Fizzbuzz")
    elif num % 3 == 0:
        print("Fizz")
    elif num % 5 == 0:
        print("Buzz")
    else:
        print(num)  
```

<a name="list_comp_first_letter"></a>
### Return first letter of every word in string

```python

st = 'Create a list of the first letters of every word in this string'
[word[0] for word in st.split()]

# ['C', 'a', 'l', 'o', 't', 'f', 'l', 'o', 'e', 'w', 'i', 't', 's']

# split the string st
# return variable index position 0 (word) for every variable (word) in split string
# whole thing is encased with [ ] because you are returning a list
```

<a name="guessing_game"></a>
## 🔴 14. Guessing Game Challenge
[Top](#top)

```python
# picks random integer from 1 to 100

# rules:
# 1) if guess is <1 or > 100, say "OUT OF BOUNDS"
# 2) on players first guess, if guess is within 10 of a number, return "WARM!"
# 2b) if further than 10 away, return "COLD!"
# 3) on all subsequent turns, if closer to number than prev guess, return "WARMER!"
# 3b) if farther away from prev guess, return "COLDER!"
# 4) when guess = number, tell them they've guessed correctly and how many guesses it took
```
1. Pick random integer

```python
# first, load the random module
# then pick random integer and assign to variable
# syntax = random.randint(a,b) returns a random int in range [a,b]

import random
num = random.randint(1,100)
```

2. Create a list to store guesses

```python
guesses = [0]

# 0 is a good placeholder because it evaluates to "False"
```

3. Write while loop that asks for a valid guess

```python

while True

    guess = int(input("I'm thinking of a number between 1 and 100.\n What is your guess? " ))
    
    if guess < 1 or guess > 100:
        print('Out of bounds! Please try again: ')
        continue
        
    break
    
# input() allows user to input something
# inputs are strings, so you need to cast input as an int()
# store this as variable guess
# if variable (guess) is out of bounds, print "out of bounds"
# then continue back to input while loop
```

4. Write while loop that compares the players guess to our number. If guess correctly, break from loop. Otherwise tell player if warmer or colder, and continue asking for guesses

```python
# load random module
import random

# generate random int from 1-100 and save as variable num
num = random.randint(1,100)

# our guess counter
guesses = [0]

while True:

    # we can copy the code from above to take an input
    guess = int(input("I'm thinking of a number between 1 and 100.\n  What is your guess? "))
    
    if guess < 1 or guess > 100:
        print('OUT OF BOUNDS! Please try again: ')
        continue # continue back up to while loop to run again
    
    # here we compare the player's guess to our number
    if guess == num:
        print(f'CONGRATULATIONS, YOU GUESSED IT IN ONLY {len(guesses)} GUESSES!!')
        break
        
    # if guess is incorrect, add guess to the list
    guesses.append(guess)
    
    # when testing the first guess, guesses[-2]==0, which evaluates to False
    # and brings us down to the second section
    
    if guesses[-2]:  
        if abs(num-guess) < abs(num-guesses[-2]):
            print('WARMER!')
        else:
            print('COLDER!')
   
    else:
        if abs(num-guess) <= 10:
            print('WARM!')
        else:
            print('COLD!')
```

<a name="methods"></a>
## 🔴 15. Methods
[Top](#top)

```python
# methods are functions built into objects
# perform specific actions on an object and can also take arguments (like a function)
# can see all methods available via tab or . 

list1 = [1,2,3,4]
list1

# once you type list1., you'll see list of possible methods
# append, cout, extend, insert, etc.
```

append

```python
list1 = [1,2,3,4]
list1.append(5)
# [1,2,3,4,5]

# append allows us to add elements to end of a list
```

count

```python
list1 = [1,2,3,4]
list1.append(2)
# 1

# count() will check number of occurences of element in list
```

<a name="functions"></a>
## 🔴 16. Functions
[Top](#top)

<a name="func_intro"></a>
### Intro to Functions

```python
# functions group together statements so they can be run more than once
# allow us to specify parameters that serrve as inputs to the functions
# functions allow you to call the same block of code multiple times
```

```python

def name_of_function():
    '''
    docstring explains function
    '''
    
# arguments or parameters go into ()
# must end with : then has to be indented
```    

```python
def say_hello():
    print('hello')

# call function

say_hello()
# hello

# to call function, need to remember to include the ()
# def = defines the name of your function
# say_hello is the NAME of your function
# arguments would go inside () - if any
# arguments = inputs for your function
# MUST INDENT - python takes whitespace seriously
```

<a name="func_arg"></a>
### Functions with Arguments

```python
def greeting(name):
    print(f'Hello {name}')

greeting('Allen')
# Hello Allen

# greeting is name of your function
# name = argument you can input
# will insert argument (name) in the { } in function
# you want to print 'hello + insert argument' 
# to CALL function, use greeting()
# and enter your name as the argument
```

<a name="func_return"></a>
### Return vs Print

```python
# in general, use return instead of print to send back reesult of function
# allows us to assign output of function to new variable
# return allows a function to return a result that can then be STORED as a variable

def add_num(num1,num2):
    return num1+num2

# call function

add_num(2,3)
# 5

# can also save as variable thanks to return

result = add_num(2,3)
print(result)
# 5

# what happens if we enter 2 strings?

add_num('one','two')
# 'onetwo'
```

What's the diff btwn return and print?

```python
# return = allows you to SAVE result of function output as a variable
# print = simply displays output to you (but doesnt save for future use)
```
 
<a name="func_num_even"></a>
### Check if number is even

```python
def even_check(number):
    return number % 2 == 0

# call function

even_check(10)
True

even_check(11)
False

# you essentialy use the mod logic to output TRUE or FALSE
# since num mod 2 = 0 means nothing leftover = even
```

<a name="func_num_list_even"></a>
### Check if any number in list is even

```python
# lets return TRUE if any number in list is even
# if no even numbers, return FALSE
# return breaks out of the loop and exits the function
```


```python
# WRONG example first

def check_even_list(num_list):
    
    for number in num_list:
        # Go through each number in num_list
        # the first time we hit an even num, we return TRUE
        if number % 2 == 0:
            return True
        
        else:
            return False
            # This is WRONG! This returns False at the very first odd number!
            # It doesn't end up checking the other numbers in the list!

# UH OH! It is returning False after hitting the first 1
check_even_list([1,2,3])

# doesn't go through full list!
```

```python
# CORRECT approach
# need to initiate a return FALSE after running through entire loop

def check_even_list(num_list):
    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we return True
        if number % 2 == 0:
            return True
        # Don't do anything if its not even
        else:
            pass
            # pass means don't do anything (if odd, do nothing)
            # pass allows us to run through entire loop
    
    return False
    
    # Notice the indentation! lines up with above for loop
    # This ensures we run through the entire for loop first
    # before we break out, and return False

```

<a name="func_return_num"></a>
### Return all even numbers in list

```python
# no longer returning TRUE or FALSE
# instead, returning list of even numbers

def check_even_list(num_list):

    even_numbers = []
    # empty placeholder list for even numbers
    
    # Go through each number
    for number in num_list:
        
        # Once we get a "hit" on an even number, we append the even number
        if number % 2 == 0:
            even_numbers.append(number)
        
        # Don't do anything if not even
        else:
            pass
            # pass = if not even, do nothing
            # return to top of loop, runs through entire loop
    
    return even_numbers
    # notice the indention. 
    # this ensures we run thru entire for loop BEFORE returning list
    # once entire loop is finished, return the even_numbers list  
    
    
check_even_list([1,2,3,4,5,6])
# [2, 4, 6]
```

Tuple Unpacking

```python
# refresher on Tuples

stock_prices = [('AAPL',200),('GOOG',300),('MSFT', 400)]
# list of tuples

for item in stock_prices:
    print(item)

# ('AAPL', 200)
# ('GOOG', 300)
# ('MSFT', 400)
```

```python
# only print first element of each tuple

for stock, price in stock_prices:
    print(stock)

# AAPL
# GOOG
# MSFT
```

```python
# only print second element of each tuple

for stock, price in stock_prices:
    print(price)

# 200
# 300
# 400
```

Employee of Month Case Study

```python
# employee of the month function
# return both name and number of hours
# winner = most number of hours worked

work_hours = [('Abby',100),('Billy',400),('Cassie',800)]

def employee_check(work_hours):

    # set some max value to initially beat, like 0 hours
    current_max = 0
    
    # set some empty value before the loop
    employee_of_mmonth = ''
    
    for employee, hours in work_hours
        if hours > current_max: # value in tuple > value in tally
            current_max = hours # override hours to max hours
            employee_of_month = employee # override employee to name
        else:
            pass # do nothing, go back to top of for loop
  
    
    return (employee_of_month, current_max)
    # notice indentation here

employee_check(work_hours)
('Cassie',800)
```

3 Card Monty Case Study

```python
# 3 positions in list, one of which is 'O'
# a function will shuffle list
# another will take players guess
# last one will check to see if it is correct

# how to shuffle a list 

example = [1,2,3,4,5]

from random import shuffle

shuffle(example)
example
# [3,1,4,5,2]

# you've successfully shuffled the list
```

```python
# 1. Create list, and shuffle it.

mylist = [' ','O',' ']

def shuffle_list(mylist):
    shuffle(mylist)
    
    return my list

# takes in list, and returns shuffled version
# shuffle is only in place, so will need to save
# to new variable if want to save output

# call function to shuffle list

shuffle_list(mylist)
# [' ',' ', 'O']
```

```python

#2. Create function for player guess
# if out of bounds, have them guess again

def player_guess():

    guess = ' '
    # create placeholder for player's guess
    
    while guess not in ['0','1','2']:
    # if guess is out of bounds
    # guess = variable
    
        guess = input("Pick a number: 0, 1, or 2: ")
        # input() allows players to enter a string
        # guess becomes, pick again
        
    return int(guess)
    # otherwise if the guess is within bounds, return it

# call function
player_guess()

# Pick a number: 0, 1, or 2: [1]
1
```

```python
# 3. check user's guess

def check_guess(mylist, guess):
    if mylist[guess] == 'O':
        print('Correct Guess!')
    else:
        print('Wrong! Better luck next time')
        print(mylist)
        
# mylist = your original list [' ','O',' ']
# guess = players' input on index location (0, 1, or 2)
```

```python
# 4. Combined your functions together!

# initial list
mylist = [' ','O',' ']

# shuffle list
mixedup_list = shuffle_list(mylist)

# shuffle list, and save to new variable
# shuffle is only in place (doesnt save)

# players guess
guess = player_guess()

# check user's guess
# notice this function takes in the input
# based on the output of other functions

check_guess(mixedup_list, guess)

# Pick a number: 0, 1 or 2: 1
# Wrong! Better luck next time
# [' ', ' ', 'O']
```

Function Example: Lesser of 2 evens

```python

# write func that returns lesser of 2 given numbers
# if both are even, but returns the greater one
# if one or both numbers are odd

# expected output:

lesser_of_two(2,4) --> 2
lesser_of_two(2,5) --> 5
```

```python
def lesser_of_two(a,b):
    
    # check if both even
    if a%2 == 0 and b%2 == 0:
        
        # return the lesser of the 2 evens
        return min(a,b)
    
    # otherwise if 1 even 1 odd
    else:
        
        # return the greater of the two
        return max(a,b)

# call function to check   
    
lesser_of_two(2,4)
# 2

lesser_of_two(2,5)
# 5
```

Function Example: Checks if both strings start with same letter

```python
# write func that takes 2 word string
# and returns TRUE if both words begin with same letter

# expected output:
animal_crackers('levelheaded llama') --> True
animal_crackers('Crazy Kangaroo') --> False
```

```python
def animal_crackers(text):
    wordlist = text.split()
    # input text, split it, and save to new variable wordlist
    
    return wordlist[0][0] == wordlist[1][0]
    
    # checks first word, first letter = second word, first letter
    # checks using index position

# call function to check
animal_crackers('levelheaded llama')
# True

animal_crackers('Crazy Kangaroo')
# False
```

Functions Example: Makes Twenty

```python
# given 2 ints, return TRUE if sum = 20
# return TRUE if one of int = 20
# if not, return FALSE

def makes_twenty(n1,n2):
    return (n1+n2)==20 or n1==20 or n2==20
    
    # since you are returning an equality, output
    # will be either true or false
    
# 3 possible scenarios
# num 1 is 20, num 2 is 20, or their sum is 20
# by setting each of 3 == TRUE, if not true, will output FALSE

# call func to check

makes_twenty(20,10)
# True

makes_twenty(2,3)
# False
```

Function Example: Old Macdonald

```python
# write func that capitalizes the 1st and 4th letters of a name

def old_mac(name):
    if len(name) > 3:
    # check if length is enough to capitalize 1st and 4th letter

        return name[:3].capitalize() + name[3:].capitalize()
        # return name, but capitalize index 0, keep returning until 3rd index
        # Mac (up to, but not including 3rd element)
        # concatenate with name, capitalize 3rd index position (D)
        # and return rest of word
        
    else:
        return 'Name too short"
 
# call func to check

old_mac('macdonald')
# MacDonald
```

Function Example: Master Yoda

```python
# given sentence, verse the words 

def master_yoda(text):
    return ' '.join(text.split()[::-1])

# input string, then split it
# [::-1] means using string slicing, -1 step to reverse string
# then you need to join these individual strings together
# and return it

# call func to check

master_yoda('i am home')
# 'home am i'
```

Function Example: Almost there

```python
# given int, return TRUE if n is within 10 or either 100 or 200

def almost_there(n):
    return ((abs(100 - n) <= 10) or (abs(200 - n) <= 10))
    
    # returning a comparison operator means you will return TRUE or FALSE
    # need abs in case number is greater than 100 or 200, like 102 or 203

# call func to check

almost_there(103)
# True
```

Function Example: 3 next to 3

```python

# given a list of ints, return TRUE if array contains 3 next to a 3
# an array is a data structure that stores same data type (for ex, a list storing ints)


def has_33(name):
    for i in range(0, len(nums)-1):
    
        # if nums[i] == 3 and nums [i+1] == 3:
        # essentially, if index position i = 3, and the next position also = 3
        
        if nums[i:i+2] == [3,3]:
            return True
    
    return False
    
# call func to check

has_33([1,3,3])
# True
```

Function Example: Duplicate Strings

```python

# given a string, return a string where every char is repeated 3x

def paper_doll(text):
    
    result = ''
    # placeholder list
    
    for char in text:
        result += char *3
    
    # for every element in input string
    # the result = result + char x 3
    # loop through entire string
    
    return result
    
    # return the result list
    
# call func

paper_doll('hello')
# 'hhheeellllllooo'

```

Function Example: Blackjack

```python
# given 3 ints between 1 and 11, if sum <=21, return sum
# if sum > 21 and there's an 11, reduce total sum by 10
# if sum exceeds 21, return BUST

def blackjack(a,b,c):

    if sum((a,b,c)) <= 21:
        return sum((a,b,c))
    elif sum((a,b,c)) <= 31 and 11 in (a,b,c):
        return sum(a,b,c)) - 10
    else:
        return 'BUST'

# call func to check

blackjack(5,6,7)
# 18

blackjack(9,9,9)
# 'BUST

blackjack(9,9,11)
# 19
```

Function Example: Summer of 69

```python
# return sum of numbers in array
# but ignore sections starting with 6 and ending in 9

def summer_69(arr):
    total = 0
    # placeholder for sums
    
    add = True
    for num in arr:
        while add:
            if num!=6:
                total += num
                break
            else:
                add = False
        while not add:
            if num !=9:
                break
            else:
                add = True 
                break
    return total

```






