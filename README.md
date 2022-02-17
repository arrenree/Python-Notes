# Python Notes by Allen

## Arithmetic

Floor Division

```python
7 // 4
# 1
# // = floor division. truncates decimal without rounding
# should be 1.75, but rounds to 1
```

Modulo

```python
7 % 3
# 3
# % is mod = the remainder after division
# useful in checking if number is even or odd
# if returns anything other than 0 = odd
```

Powers

```python
2 ** 3
# 8
```

Square Root

```python
4 ** 0.5
# 2.0
# 4 to the power of 0.5 = square root
# returns a float
```

## Variable Assignments

General guidelines

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

Variable Reassignment

```python
a = 10

a = a + a
# 20

# another way of saying this
a += 10
# 30
# same as a = a + 10
```

Dynamic Typing

```python
# python uses dynamic typing, which means you can reassign variables to different data types
# initially assigned an int
# reassigned as string
```

Datatypes

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

## Strings

```python
# strings are a sequence of characters using single or double qoutes
# 'hello' "hello"
# since its a sequence, can use indexing
```

Types of Strings

```python
'hello' # single word
'this is also a string' # entire phrase
"string with double quotes" # double quotes
```

Printing a String

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

len()

```python
len('hello world')
# 11
# use len to check length of a string
```

String Indexing

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

String Slicing

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

Reversing a String

```python
# how do you reverse a string?

mystring[::-1]
# 'dlroW olleH'

# using -1 step reverses the string
```

String Immutability

```python
# strings are immutable. 
# once a string is created, the elements within it cannot be changed or replaced
# nor can it be re-assigned to something else

name = "Sam"
name[0] = 'P'

# error. you can't reassign the S to a P in a string
```

String Concatention

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

Concatenating Numbers with strings

```python
# you will get an error if concatenate numbers with string
2 + 3
# 5

'2' + '3'
'23'
# 2 and 3 are strings, so if you add them together, becomes 23
# and not 5
```

String Methods

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

String Formatting (String Interporlation)

```python
# allows you to inject items into a string rather than trying to chain items
# together using commas or concatenation
# 3 methods:
# 1) placeholders using % (oldest)
# 2) .format() method (improved technique)
# 3) f-string literals (newer)
```

Formatting with % Placeholder

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

%s Method

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

%d Method

```python
# %d operator converts numbers to ints first, without rounding

print('I wrote %d programs today.' %3.75)  
# I wrote 3 programs today.

# converts float 3.75 to int (no rounding)
```

%r Method

```python
# %r Method

print('He said his name was %r.' %'Fred')
# He said his name was 'Fred'.

# %r includes the 'quotes'
```

Padding and Precision of Floating Point Numbers

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

Multiple % Placeholder Formatting

```python
# can have multiple different conversion tools

print('First: %s, Second: %5.2f, Third: %r' %('hi!',3.1415,'bye!'))
# First: hi!, Second:  3.14, Third: 'bye!'

# %s & 'hi!' = First: hi!
# %5.2f & 3.1415 = Second:  3.14
# %r & 'bye!' = Third: 'bye!'
```

.format() method

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

Indexing for multiple string interprolations

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

Float formatting with .format()

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

F String Literal (another format for string interpolation)

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

## Lists

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

List - Indexing & Slicing

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

Lists - Concatenating 2 Lists

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

Lists - Duplicating Strings

```python
list = ['alpha','bravo']
list * 2
# ['alpha', 'bravo', 'alpha', 'bravo']
```

Lists - Indexing to amend elements

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

Lists - Remove Elements

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

Lists - Sorting

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

Lists - Reverse

```python
num_list.reverse()
num_list
# [8,4,3,1]
```

Lists - Nested Lists / Matrix

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

List - Comprehensions

```python
# advanced feature which allow for quick construction of lists
# build a list comprehension by deconstructing a for loop within a [ ]

first_col = [row[0] for row in matrix]
first_col
# [1,4,7]

# used list comprehension to grab first element of every row in matrix
```

## Dictionaries

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

Dictionary - Retrieving Items in nested dictionary

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

Dictionary - Creating Keys by Assignment

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

Dictionary - Appending Items

```python
d = {'k1': 100,'k2':200}
d['k3'] = 300
d
# {'k1': 100, 'k2': 200, 'k3': 300}

# added key/value pair of k3/300
```

Upserting items to dict

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

## Tuples

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

## Files

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

## Comparison Operators

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

## for Loops

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

## while Loops

```python



