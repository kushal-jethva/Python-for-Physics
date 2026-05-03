
## The Ritual
---
Before starting any programming language, it is an unsaid rule to say hello to the programming world. ' print() ' function takes input and prints to the console/screen.

```python
print('Hello World!')
```
## Comments
---
Comments are used by programmers for personal use case and they are not part of the code. They are used to explain code blocks or as personal notes.
```python
# this is a comment

'''
this
is
also
a comment (multiline)
'''

"""
this
also
"""
```
## Variables
---

A variable is a container used to store data.

```python
abc = 1 # variable named as 'abc' with value 1
```

Valid characters to name a variable are " abc.. ABC.. 123.. and \_"
* NOTE: Name cannot start with numbers! 
* You cannot name a variable which is a keyword in python. [click here](https://www.w3schools.com/PYTHON/python_ref_keywords.asp)

Common variable naming convections:

```python
likeThis = 123 # Camel case (starting of second word captal)
LikeThis = 123 # Pascal case (starting of each word capital)
Like_This = 123 # Snake case (words separated by underscore)
likethis1 = 123 # name followed by no.
likethis_2 = 123 # also valid
_ = 123          # used as "throwaway variable"
print = 123   # invalid, it is reserved keyword in python
```

Naming a variable correctly is very important to help in debugging and to avoid confusion.
NOTE: Name the variable according to what value it stores.

```python
velocity = 50
x_speed = 30
y_speed = 40
```

## Data Types
---
Consider types of number: Integer , complex , natural etc. Similarly python has different data types:

* Integer 
* Float      (for decimals)
* Complex  
* Boolean (True and False)
* String    (for alphabets)

```python
speed = 20 # integer
years = 10_000 # use underscore for better readability 
speed_2 = 20.001  # float
value = 20 + 1j # complex (always ends with j else invalid)
value2 = True # boolean, NOTE: first capital
value3 = False # NOTE: first capital
name = 'Isaac' # string
name2 = "Enstein" # also string
name3 = 'J. J. Thomson'
name4 = ' abc ABC 123 !@# ' # string can have all characters

# when to use:  
# int → counting (age, quantity)  
# float → measurements (temperature, speed)  
# string → text (name, sentence)  
# boolean → conditions (True/False decisions)


# use type() function to see data type
print(type(speed))
print(type(speed_2))
print(type(value))
print(type(value2))
print(type(name))

# format: type(data)
```

Other data type includes:
* List
* Dictionary
* Tuple
* Set
To be covered in Data Structures.

## Operations
---
Same as Mathematics, we can perform various operations in python.
```python
add = 1 + 2
subtract = 1 - 2
multiply = 1*2
divide = 1/2
get_remainder = 1%2  # divides 1 by 2 and returns remainder
divide_and_get_integer = 1//2 # called floor division
''' 
floor division returns 
largest integer less than or equal to the exact division result
'''
# try -1//2

exponents = 1**2 # 1 raise to 2

# use brackets to build complex expressions
# brackets are solved first under BODMAS
# only valid bracket is ()

expression = ((1/2) * 3**2 + 4) ** 0.5
```


### Comparison (Relational) Operators
---
Comparison operator return Boolean values (True/False). They are also called conditional operators as used in codes to check conditions.
```python
#consider a and b are two variables
a,b = 1,2   # you can assign multiple variables in this format
print(a==b) # to check equality
'''
NOTE: 
single equal is used to assing value to variable
while double equal is used to compare values (equality)
'''
print(a!=b) # a not equal to b, remember as ≠ , line is !
print(a<b) #less than
print(a>b) # greater than
print(a<=b) # less than equal to
print(a>=b) # greater than equal to
```

There are also some logical operators:
```python
and
or
not

# similar to our electronic gate system
# compares two boolean values and returns result(boolean) accordingly
# and → True only if both are True  
# or → True if at least one is True  
# not → reverses value
```

try to explore results of different conditions on logical operator yourself.
```python
#example

print(True and False)
print(False or False)
print((True and False) and True) #nested condition
print(not True)
```

### Assignment Operators
---
```python
# consider variable a
a=5
a += 1 # same as 'a = a + 1'

'''
takes a, adds 1 and re-assign value to a
'''

a -= 1 # a = a - 1
a *= 1 # a = a * 1
a /= 1 # a = a / 1
a //= 1 # a = a // 1
a %= 2 # a = a % 2
a **=2 # a = a ** 2

# you can also do
a += a # a = a + a
b = 2
a *= b # valid
```

### Bitwise Operators
---
These operates on binary level. look up yourself how do they work, its very simple...
Though you are rarely gonna use these operators.
* & 
* |
* ^
* ~
* <<
* \>>
```python
print(5 & 3)
print(5 | 3)
```
Usually used in cryptography and for optimization in algorithm.

### Note
---
Some operations between different data types are allowed due to type conversion, but not all (e.g., int + string is invalid).
```python
a = 1
b = 1.3
print(a + b) #internally python converts a to float type (implicit)
# let us check
print(type(a))
print(type(b))
print(type(a + b))
#explicit type conversion
print(b + float(a))

#try print(int(b))

c = 1 + 8j
print(type(c))

print(a + c)
```

Operation on strings is different case:
```python
a = '1'
b = '2'
print(a + b)
print(a * 3)
print(a + 2) # error: cannot add string and integer
```
Explore Operation with Strings yourself, We are not going to work with this a lot, as we only deal with numbers right now.

## Taking input
---
Lets start building something using user input.
there is function 'input()' which takes values from user.
```python
user_input = input('Enter value :')
print(user_input)
print(type(user_input))

# format to use input() function
# input('msg for user')

"""
NOTE: by default it returns string
to perform operation we must convert string to relevant data type
"""

# we can convert data types using functions
# int() converts value inside to integer
# float() converts value inside to float
# complex('1+2j') gives complex no. 1+2j out of string '1+2j'.
# NOTE: no whitespace in srting shld be present

number = int(input('Enter no. :'))
# int(input()) → converts to integer
print(number)
print(type(number))
```

```python
number1 = float(input('Enter number 1:'))
number2 = float(input('Enter number 2:'))
print('addition:',number1+number2) # use , to print multiple values
print('subtration:',number1-number2)
print('multiplication:',number1*number2)
print('division:',number1/number2)
```
## Things to Remember

> [!NOTE]
>
>---
>* Python is case sensitive. ex: True is not same as true
>* variable name cannot start with numbers
>* variable name cannot be python keyword. [click here](https://www.w3schools.com/PYTHON/python_ref_keywords.asp)
>* = is for assigning and == is to check equality.
>* input() gives string by default.
>* '1' + 1 , will throw error as string + int/float/complex/bool is not allowed.

## Best Practices
---
>Use type hints to improve readability and debugging (they are not enforced at runtime).

```python
velocity : int = 100
name : str = 'Abdul Kalam'
```

>Use meaningful variable names (avoid vague names like `x`, `a1`)

>Use underscores for large numbers to improve readability.

```python
population = 1_400_000_000
```

>Use uppercase for constants (by convention).

```python
PI = 3.14
C = 2_99_792_458 # m/s
```

> Initialize variables with `None` when value is not yet known.

```python
result = None
```
