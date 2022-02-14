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
