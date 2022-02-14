# Python-Notes

## Arithmetic

Floor Division

```p
7 // 4
# 1
# // = floor division. truncates decimal without rounding
# should be 1.75, but rounds to 1
```

Modulo

```p
7 % 3
# 3
# % is mod = the remainder after division
# useful in checking if number is even or odd
# if returns anything other than 0 = odd
```

Powers

```p
2 ** 3
# 8
```

Square Root

```p
4 ** 0.5
# 2.0
# 4 to the power of 0.5 = square root
# returns a float
```

## Variable Assignments

General guidelines

```p
# cannot start with number
# cannot have spaces
# cannot use special symbols
# best practices all lowercase
# avoid special python phrases like 'list' and 'str'
# avoid single characters
```

Variable Assignment

```p
# create object called 'a' and assign it number 5
a = 5

# name = object
# we've assigned int object 5 to variable name a
```

Variable Reassignment

```p
a = 10

a = a + a
# 20

# another way of saying this
a += 10
# 30
# same as a = a + 10
```

Dynamic Typing

```p
# python uses dynamic typing, which means you can reassign variables to different data types
# initially assigned an int
# reassigned as string
```

Datatypes

```p
# int (for integer)
# float
# str (for string)
# list
# tuple
# dict (for dictionary)
# set
# bool (for Boolean True/False)
```

## Strings

```p
# strings are a sequence of characters using single or double qoutes
# 'hello' "hello"
# since its a sequence, can use indexing
```

Types of Strings

```p
'hello' # single word
'this is also a string' # entire phrase
"string with double quotes" # double quotes
```

Print()

```p
print("hello")
# hello
# print will export the results, removing the parathesis

print("hello \n world")
# hello
#  world
# the \n is a break sequence that starts new line

print("hello \t world")
# hello   world
# \t is another break sequence that is the same as tab
```

len()

```p
len('hello world')
# 11
# use len to check length of a string
```

Indexing

```p
# strings are ordered sequences, which means we can use indexing or slicing to grab sub-sections
# indexing starts at 0
# indexing uses [ ] and allows you to grab single characters
# can also do reverse indexing -1
```

```p
mystring = "Hello World"
mystring[0]
# H

len(mystring)
# 11
# calc how many elements in string

mystring[-2]
# 'l'
# negative indexing
```

Slicing

```p
# slicing
# slicing allows you to grab multiple characters
# syntax [ start:stop:step]
# stop = index you go up to, but NOT include
# step = size of the jump you take
```

```p
mystring[0:3:1]
# 'Hel'
# starts at 0, goes up to, but NOT include index 4 (l), 1 step

mystring[ :3]
# 'Hel'

mystring[::]
# 'Hello World'
# take everything from string

mystring[::2]
# 'HloWrd'
# take all elements in step sizes of 2 
```

```p
# how do you reverse a string?
mystring[::-1]
# 'dlroW olleH'
# using -1 step reverses the string
```

immutability

```p
# strings are immutable. you cannot grab an element in string
# and re-assign it to something else

name = "Sam"
name[0] = 'P'
# error. you can't reassign the S to a P in a string
```

String Concatention

```p
name = "Sam"
last_letters = name[1:]
last_letters
# 'am'

'P' + last_letters
# 'Pam'
# can use + to concatenate strings
```

```p
x = 'Hello World'
x + ' it is a good day'
# 'Hello World it is a good day'
```

```p
letter = 'z'
letter * 10
# 'zzzzzzzzzz'
```

Concatenating Numbers with strings

```p
# you will get an error if concatenate numbers with string
2 + 3
# 5

'2' + '3'
'23'
# 2 and 3 are strings, so if you add them together, becomes 23
# and not 5
```

String - Capitalization 

```p
x = 'Hello World'
x.upper()
# 'HELLO WORLD'

# this method is not "in place"
# doesnt affect the original string
```

String - Lowercase

```p
x = 'Hello World'
x.lower()
# 'hello world'
```

Splitting Strings

```p
x.split()
# ['Hello','World']

# split() will take a string and split it based on the white space
```

```p
x = 'Hi this is a string'
x.split()
# ['Hi','this', 'is', 'a', 'string']
```

```p
# you can also split on specific letters

x.split('i')
# ['H', ' th', 's ', 's a str', 'ng']
```

Print Function

```p
print ("hello world")
# hello world

# prints everything within the parathesis
```

String Interporlation

```p
# injects variables into strings for printing
# 2 methods: .format() and f string literal
```

.format() method

```p
print('this is a string {} '.format('INSERTED'))
# this is a string INSERTED

# .format takes string 'INSERTED' and places it in {}
```

```p
print ('the {} {} {}'.format('fox','brown','quick'))
# the fox brown quick

# .format takes strings and replaces {} in sequential order
```

Indexing for multiple string interprolations

```p
print ('the {2} {1} {0}'.format('fox','brown','quick'))
# the quick brown fox
```

```p
print ('the {0} {0} {0}'.format('fox','brown','quick'))
# the fox fox fox
```

```p
# using varibles for string interpolation
print ('the {q} {b} {f}'.format(f='fox',b='brown',q='quick'))
```

Float formatting with .format()

```p
result = 100/777
result
# 0.128700

print ('the result was {}'.format(result))
# the result was 0.128700
```

```p
print ('the result was {r}'.format(r = result))
# the result was 0.128700

# same thing as above
```

```p
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

F String Literal (another format for string interpolation)

```p
name = "Jose"
print(f'Hello, his name is {name}')
# Hello, his name is Jose

# so need f ' + {variable} 
```

```p
name = "Sam"
age = 3
print(f'{name} is {age} years old')
# same is 3 years old
```

## Lists

```p
# Lists are ordered sequences that can hold a variety of object types
# use [ ] brackets and commas to separate objects in list
# lists support indexing and slicing
# lists can be nested
```

```p
# list of int

my_list = [1,2,3]
```

```p
# list of string, int, float

my_list = ['STRING',100,23.2]
```

```p
len(my_list)
# 3

# 3 items in list
```

List - Indexing

```p
mylist = ['one','two','three']
mylist[0]
# 'one'

mylist[1:]
# 'two','three'
```

Lists - Concatenating 2 Lists

```p
another_list = ['four','five']
new_list = mylist + another_list
new_list
# ['one','two','three','four','five']
```

Lists - Indexing to amend elements

```p
new_list[0] = 'ONE ALL CAPS'
new_list
# ['ONE ALL CAPS', 'two','three','four','five']
```

Lists - Append Elements

```p
new_list.append('six')
new_list
# ['ONE ALL CAPS', 'two','three','four','five','six']

# adds element to end of list
# appends in place, which means it permanently changes the list
```

Lists - Remove Elements

```p
new_list.pop()
# 'six'
new_list
# ['ONE ALL CAPS', 'two','three','four','five']

# popped off 'six', removed from list
# remove element from end of list
```

```p
# to save the popped item, save it as a varaible

popped_item = new_list.pop()
popped_item
# 'six'

# by default, will pop off -1 index position
```

```p
# can also use index position to remove elements

new_list.pop(0)
new_list
# ['two','three','four','five']

# removes element 0 = 'ONE ALL CAPS'
```

Lists - Sorting

```p
new_list = ['a','e','x','b','c']
num_list = [4,1,8,3]

new_list.sort() 
new_list
# ['a', 'b', 'c', 'e', 'x']
# doesnt return anything, simply sorts list in place
```

You cannot assign sorted list as a variable

```p
new_sorted_list = new_list.sort()

# this doesnt work because .sort doesnt return anything
# so nothing gets assigned to your new variable
```

To assign a sorted list, need to do this:

```p
new_list.sort()
my_sorted_list = new_list
my_sorted_list
# ['a', 'b', 'c', 'e', 'x']

# sort list first
# then assign the sorted list to a new variable
# now when you call the new variable, the list will be sorted
```

```p
num_list = [4,1,8,3]

num_list.sort()
sorted_num_list = num_list
sorted_num_list
# [1,3,4,8]
```

Lists - Reverse

```p
num_list.reverse()
num_list
# [8,4,3,1]
```

## Dictionaries

```p
# dictionaries are unordered mappings for storing objects
# use a key-value pairing instead
# allows users to quickly grab objects without index location
# objects retrieved by key name
# unordered and cannot be sorted
```

```p
# lists
# objects retrieved by location
# ordered sequence; can be indexed or sliced
```

```p
my_dict = {'key1':'value1','key2':'value2'}
my_dict['key1']
# 'value1'

# calling a key retrieves its value
``` 

```p
prices_lookup = {'apple':2.99,'oranges':1.99,'milk':5.80}
prices_lookup['apple']
# 2.99

# without knowing index location, can lookup price of an apple
# this is the power of dictionaries
```

Dictionary - Retrieving Items in nested dictionary

```p
d = {'k1':123,'k2':[0,1,2],'k3':{'insidekey':100}}

# dict can contain int, a list, and another dict

d['k2']
# [0,1,2]

d['k2'][2]
# 2

d['k3']['insidekey']
# 100
```

Dictionary - Appending Items

```p
d = {'k1': 100,'k2':200}
d['k3'] = 300
d
# {'k1': 100, 'k2': 200, 'k3': 300}

# added key/value pair of k3/300
```

Upserting items to dict

```p
d = {'k1': 100,'k2':200}
d['k1'] = 'NEW ITEM'
d
# {'k1': 'NEW ITEM', 'k2': 200, 'k3': 300}
```

Dictionary - Extract all keys

```p
d.keys()
# dict_keys(['k1', 'k2', 'k3'])
```

Dictionary - Extract all values

```p
d.values()
# dict_values(['NEW ITEM', 200, 300])
```

## Tuples

```p
# very simliar to lists, except they are immutable
# immutable = cannot be changed
# once element is inside tuple, cannot be reassigned
# tuples use parathesis (1,2,3)
```
