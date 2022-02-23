# Python Notes by Allen
<a name="top"></a>

# Contents

### 1. [Basic Math & Variable Assignments](#basic_math)
1. [Floor Division](#floor)
2. [Modulo](#modulo)
3. [Powers](#powers)
4. [Square Root](#square_root)
5. [Variable Assignment](#var_assign)
6. [Variable Reassignment](#var_reassign)
7. [Dynamic Typing](#dynamic_typing)
8. [Datatypes](#datatypes)

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
### 6. [Files](#files)
### 7. [Comparison Operators](#comp_operator)
### 8. [if, elif, else Statements](#if)
### 9. [for Loops](#for_loops)
### 10. [while Loops](#while_loops)
### 11. [Useful Operators](#useful_operators)
### 12. [List Comprehensions](#list_comprehension)
### 13. [Guessing Game Challenge](#guessing_game)
### 14. [Methods](#methods)

<hr>

<a name="basic_math"></a>
## 🔴 1. Basic Math & Variable Assignments
[Top](#top)

<a name="floor"></a>
### Floor Division

```python
7 // 4
# 1
# // = floor division. truncates decimal without rounding
# should be 1.75, but rounds to 1
```
<a name="Modulo"></a>
### Modulo

```python
7 % 3
# 3
# % is mod = the remainder after division
# useful in checking if number is even or odd
# if returns anything other than 0 = odd
```
<a name="powers"></a>
### Powers

```python
2 ** 3
# 8
```
<a name="square_root"></a>
### Square Root

```python
4 ** 0.5
# 2.0
# 4 to the power of 0.5 = square root
# returns a float
```
<a name="var_assign"></a>
### Variable Assignments

```python
# cannot start with number
# cannot have spaces
# cannot use special symbols
# best practices all lowercase
# avoid special python phrases like 'list' and 'str'
# avoid single characters
```

Variable Assignment

```python
# create object called 'a' and assign it number 5
a = 5

# name = object
# we've assigned int object 5 to variable name a
```

<a name="var_reassign"></a>
### Variable reassignments

```python
a = 10

a = a + a
# 20

# another way of saying this
a += 10
# 30
# same as a = a + 10
```
<a name="dynamic_typing"></a>
### Dynamic Typing

```python
# python uses dynamic typing, which means you can reassign variables to different data types
# initially assigned an int
# reassigned as string
```
<a name="datatypes"></a>
### Datatypes

```python
# int (for integer)
# float
# str (for string)
# list
# tuple
# dict (for dictionary)
# set
# bool (for Boolean True/False)
```

<a name="strings"></a>
## 🔴 2. Strings
[Top](#top)

```python
# strings are a sequence of characters using single or double qoutes
# 'hello' "hello"
# since its a sequence, can use indexing
```
<a name="string_type"></a>
### Types of Strings

```python
'hello' # single word
'this is also a string' # entire phrase
"string with double quotes" # double quotes
```

<a name="string_print"></a>
### Printing a String

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
### len()

```python
len('hello world')
# 11
# use len to check length of a string
```

<a name="string_indexing"></a>
### String Indexing

```python
# strings are ordered sequences, which means we can use indexing or slicing to grab sub-sections
# indexing starts at 0
# indexing uses [ ] and allows you to grab single characters
# can also do reverse indexing -1
```

```python
mystring = "Hello World"
mystring[0]
# H
```

```python
len(mystring)
# 11

# calc how many elements in string
```

```python
mystring[-2]
# 'l'

# negative indexing
```

<a name="string_slicing"></a>
### String Slicing

```python
# slicing
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
### Reversing a String

```python
# how do you reverse a string?

mystring[::-1]
# 'dlroW olleH'

# using -1 step reverses the string
```

<a name="string_immut"></a>
### String Immutability

```python
# strings are immutable. 
# once a string is created, the elements within it cannot be changed or replaced
# nor can it be re-assigned to something else

name = "Sam"
name[0] = 'P'

# error. you can't reassign the S to a P in a string
```

<a name="string_con"></a>
### String Concatention

```python
name = "Sam"
last_letters = name[1:]
last_letters
# 'am'

'P' + last_letters
# 'Pam'

# can use + to concatenate strings
# extracted 'am' from the original 'Sam'
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
### Concatenating Numbers with strings

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
### String Methods

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
## Sets

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
## 🔴 6. Files
[Top](#top)

```python
# python uses file objects to interact with external files on your computer
# python has built in open function that allows us to open file types
# 1) need to first OPEN file
# 2) then can READ file
```

Files - Opening + Reading

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

Readlines Method

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

Writing to a File

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
Appending to a File

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
## 🔴 7. Comparison Operators
[Top](#top)

```python
# allows us to compare variables and output a boolean (True or False)
```

Equals

```python
2 == 2
# True
```

Does not equal

```python
2 != 3
# True. 2 does not equal 3. Statement is true.

2 != 2
# False. 2 does not equal 2. Statement is false.
```

Chained Comparison Operators

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

## if, elif, else Statements

<a name="if"></a>
## 🔴 8. if, elif, else Statements
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
## 🔴 9. for Loops
[Top](#top)

```python
# for loops act as an iterator in python
# it goes through items that are in a sequence or any other iterable item

for item in object:
    statements to do stuff

# variable name used for the item is up to coder
```

for loop

```python
list1 = [1,2,3,4]

for num in list1:
    print(num)

# 1
# 2
# 3
# 4
```

for loop + if 

```python
# print only even numbers

list1 = [1,2,3,4]

for num in list1:
    if num % 2 == 0:  # mod = 0 means even number
        print(num)

# 2
# 4
```

for loop  + if + else

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

for loop running tally

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

for loop with strings

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

for loop with tuple

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

Tuple unpacking

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

for loop with dictionaries

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

Dictionary methods

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
## 🔴 10. while Loops
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

break, continue, pass

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
while loop + if + else + break

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
## 🔴 11. Useful Operators
[Top](#top)

range

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

enumerate

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
zip

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

in operator

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

min and max

```python
mylist = [10,20,30,40,100]
min(mylist)
# 10

max(mylist)
# 100

```

random - shuffle

```python
# python comes with built in random library

from random import shuffle

# this shuffles the list "in place" so it wont
# return anything, inistead it will effect the list passed

shuffle(mylist)

mylist
# [40, 10, 100, 30, 20]
```

random - randint

```python
from random import randint

# return random integer in range [a,b], including both end points

randint(0,100)
# 25
```

input

```python

input('Enter something in this box: ')
# Enter something in this box: []
# Enter something in this box: [hello]
# 'hello'
```

<a name="list_comprehension"></a>
## 🔴 12. List Comprehensions
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

square numbers in range and turn into list

```python
list2 = [x**2 for x in range(0,11)]
list2
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# return x**2 for every x in range 0-10
```

if statement example

```python
# check for even numbers in a range

list3 = [x for x in range(11) if x % 2 == 0]
list3
# [0,2,4,6,8,10]

# return x for every x in range 0-10, if x % 2 = 0
# ie, return every even number
```
converting celsius to fahrenheit

```python
# convert celsius to fahrenheit

celsius = [0,10, 20.1, 34.5]
fahrenheit = [((9/5) * temp + 32) for temp in celsius]

fahrenheit
# [32.0, 50.0, 68.18, 94.1]

# first you define a list celsius
# return variable 'temp' for every 'temp' in list celsius
```

nested list comprehensions

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

Statements Assessment

Use for, .split(), and if to create a Statement that will print out words that start with 's':

```python
st = 'Print only the words that start with s in this sentence'

for word in st.split()
    if word[0] == 's':
        print(word)
     
# start
# s
# sentence
```

use range() to print all the even numbers from 0 to 10.

```python
list(range(0,11,2))
# [0,2,4,6,8,10]

# step 2 will automatically go from 0 to 2 and include all even numbers
```

use list comprehension to create a list of all numbers between 1 and 50 that are divisble by 3

```python
[x for x in range(1,51) if x%3 == 0]
# [3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48]

# return x for every x in range 1-50
# x % 3 = 0 means every multiple of 3
```

if the length of a word is even, print "even!"

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

print integers from 1 to 100
for multiples of 3, print "Fizz" instead of the number
for multiples of 5, print "Buzz"
for multiples of both 3 and 5, print "Fizzbuzz"

```python
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

use list comprehension to create a list of the first letter of every word in the string below

```python

st = 'Create a list of the first letters of every word in this string'
[word[0] for word in st.split()]

# ['C', 'a', 'l', 'o', 't', 'f', 'l', 'o', 'e', 'w', 'i', 't', 's']

# split the string st
# return variable index position 0 (word) for every variable (word) in split string
# whole thing is encased with [ ] because you are returning a list
```
<a name="guessing_game"></a>
## 🔴 13. Guessing Game Challenge
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
## 🔴 14. Methods
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

<a name="Functions"></a>
## 🔴 15. Functions
[Top](#top)

```python
# functions group together statements so they can be run more than once
# allow us to specify parameters that serrve as inputs to the functions
# functions allow you to call the same block of code multiple times
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

Functions with Arguments

```python
def greeting(name):
    print(f'Hello {name}')

greeting('Allen')
# Hello Allen

# greeting is name of your function
# name = argument you can input
# you want to print 'hello + insert argument' 
# to CALL function, use greeting()
# and enter your name as the argument
```

Return

```python
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

Check if number is even

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

Check if any number in list is even

```python
# lets return boolean if any number is even
# return breaks out of the loop and exits the function
```


```python
# WRONG example first

def check_even_list(num_list):
    # Go through each number
    for number in num_list:
        # Once we get a "hit" on an even number, we return True
        if number % 2 == 0:
            return True
        # This is WRONG! This returns False at the very first odd number!
        # It doesn't end up checking the other numbers in the list!
        else:
            return False
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
    # Notice the indentation! This ensures we run through the entire for loop    
    return False
```

