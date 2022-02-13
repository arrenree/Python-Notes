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

my_dogs = 2

my_dogs = ['Alpha', 'Bravo']

# initially assigned an int
# reassigned as string
```



