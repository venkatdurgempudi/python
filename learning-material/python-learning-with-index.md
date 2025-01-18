# Index

- [1. Introduction](#1-introduction)
  - [1.1. Commands for Windows](#11-commands-for-windows)
  - [1.2. Commands for Mac/Linux](#12-commands-for-mac/linux)
  - [1.3. Writing your First Code](#13-writing-your-first-code)
  - [1.4.Comments](#14comments)
- [2. Variables](#2-variables)
  - [2.1. Casting](#21-casting)
  - [2.2. Variable Names](#22-variable-names)
- [3. Data Types](#3-data-types)
  - [3.1 Numbers](#31-numbers)
  - [3.2 Strings](#32-strings)
    - [Escape Character](#escape-character)
  - [3.3 Booleans](#33-booleans)
  - [3.4 Lists](#34-lists)
    - [len()](#len())
    - [Access List Items](#access-list-items)
    - [Change List Items](#change-list-items)
    - [Add List Items](#add-list-items)
    - [Remove List Items](#remove-list-items)
    - [Loop Lists](#loop-lists)
    - [List Comprehension](#list-comprehension)
    - [Sort Lists](#sort-lists)
    - [Copy Lists](#copy-lists)
    - [Join Lists](#join-lists)
    - [List Methods](#list-methods)
- [4. Operators](#4-operators)
  - [4.1 Arithmetic operators](#41-arithmetic-operators)
  - [4.2 Assignment operators](#42-assignment-operators)
  - [4.3 Comparison operators](#43-comparison-operators)
  - [4.4 Logical operators](#44-logical-operators)
  - [4.5 Identity operators](#45-identity-operators)
  - [4.6 Membership operators](#46-membership-operators)
  - [4.7 Bitwise operators](#47-bitwise-operators)
  - [4.8 Operator Precedence](#48-operator-precedence)

---

# Python Learning

<a id="1-introduction"></a>
## 1. Introduction

<a id="11-commands-for-windows"></a>
### 1.1. Commands for Windows


```python
# Check Python Location
!where python

# Check Python Version
!python --version

# Check Installed Libraries
!pip list
!conda list  # If using Conda

# Install New Libraries
!pip install <package_name>  # Replace <package_name> with the library name
!conda install <package_name>  # For Conda environments

# Check Current Working Directory
!cd

# List Files in Current Directory
!dir

# Restart Kernel
from IPython.display import display, Javascript
display(Javascript('Jupyter.notebook.kernel.restart()'))

# Check Environment Variables
import os
print(os.environ)

# Run a Shell Command
!echo "Hello from the shell!"

# Enable Debugging
%debug
```

<a id="12-commands-for-mac/linux"></a>
### 1.2. Commands for Mac/Linux


```python
# Check Python Location
!which python

# Check Python Version
!python --version

# Check Installed Libraries
!pip list
!conda list  # If using Conda

# Install New Libraries
!pip install <package_name>  # Replace <package_name> with the library name
!conda install <package_name>  # For Conda environments

# Check Current Working Directory
!pwd

# List Files in Current Directory
!ls

# Restart Kernel
from IPython.display import display, Javascript
display(Javascript('Jupyter.notebook.kernel.restart()'))

# Check Environment Variables
import os
print(os.environ)

# Run a Shell Command
!echo "Hello from the shell!"

# Enable Debugging
%debug

```

<a id="13-writing-your-first-code"></a>
### 1.3. Writing your First Code


```python
# Any of the below will work
print('Hello World!')
print("Hello World!")
```

<a id="14comments"></a>
### 1.4.Comments


```python
# This is how we can write Single Line comments with "#" at the beginning
print("Comments")

"""
This is how
multi-line comments can be written
in the python
"""
```

---

<a id="2-variables"></a>
## 2. Variables

- Python has no command for declaring a variable.
- A variable is created the moment you first assign a value to it.


```python
x = 5
y = "John"
print(x)
print(y)
```

- Variables do not need to be declared with any particular type, and can even change type after they have been set.


```python
x = 4       # x is of type int
x = "Sally" # x is now of type str
print(x)
```

<a id="21-casting"></a>
### 2.1. Casting

- If you want to specify the data type of a variable, this can be done with casting.


```python
x = str(3)    # x will be '3'
print(x)
y = int(3)    # y will be 3
print(y)
z = float(3)  # z will be 3.0
print(z)
```

<a id="22-variable-names"></a>
### 2.2. Variable Names

- A variable name must start with a letter or the underscore character
- A variable name **cannot start with a number**
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are **case-sensitive** (age, Age and AGE are three different variables)
- A variable name cannot be any of the [Python keywords](https://www.w3schools.com/python/python_ref_keywords.asp).


```python
# Legal variable names
myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"

# Illegal variable names
2myvar = "John"
my-var = "John"
my var = "John"
```

- Variable names with more than one word can be difficult to read.
- There are several techniques you can use to make them more readable:


```python
# Camel Case
myVariableName = "John"

# Pascal Case
MyVariableName = "John"

# Snake Case
my_variable_name = "John"

```

- Python allows you to assign values to multiple variables in one line:


```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

- And you can assign the same value to multiple variables in one line:


```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

- If you have a collection of values in a list, tuple etc. Python allows you to extract the values into variables. This is called **unpacking**.


```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```

- The Python **print()** function is often used to **output variables**.


```python
# Single Variable
x = "Python is awesome"
print(x)

# multiple variables
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)

# + operator can be used to output multiple variables
x = "Python"
y = "is"
z = "awesome"
print(x + y + z) # Notice the space character after "Python " and "is ", without them the result would be "Pythonisawesome".

```

- For numbers, the + character works as a mathematical operator:


```python
x = 5
y = 10
print(x + y)
```

- print() function, when you try to combine a string and a number with the + operator, Python will give you an error:


```python
x = 5
y = "John"
print(x + y)
```

- The **best way** to output multiple variables in the print() function is to separate them with **commas**, which even **support different data types**:


```python
x = 5
y = "John"
print(x, y)
```

- Global and Local variables


```python
x = "Gloal awesome" # global variable

def myfunc():
  x = "Local fantastic"  # local variable
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

---

<a id="3-data-types"></a>
## 3. Data Types

##### Built-in Data Types

- Variables in Python can store data of different types, and each type comes with its own set of capabilities.
- Python provides the following built-in data types, categorized as follows:

| **Category**        | **Types**                          |
|----------------------|------------------------------------|
| **Text Type**        | `str`                             |
| **Numeric Types**    | `int`, `float`, `complex`         |
| **Sequence Types**   | `list`, `tuple`, `range`          |
| **Mapping Type**     | `dict`                            |
| **Set Types**        | `set`, `frozenset`                |
| **Boolean Type**     | `bool`                            |
| **Binary Types**     | `bytes`, `bytearray`, `memoryview`|
| **None Type**        | `NoneType`                        |

---


- You can get the data type of any object by using the type() function:


```python
x = 5
print(type(x))
```

##### Python Data Types with Examples and Their Types

- In Python, the data type is set when you assign a value to a variable:


| **Example**                                    | **Data Type**         | **Code**                                           | **Output**              |
|------------------------------------------------|------------------------|---------------------------------------------------|-------------------------|
| `x = "Hello World"`                            | `str`                 | `print(type(x))`                                  | `<class 'str'>`         |
| `x = 20`                                       | `int`                 | `print(type(x))`                                  | `<class 'int'>`         |
| `x = 20.5`                                     | `float`               | `print(type(x))`                                  | `<class 'float'>`       |
| `x = 1j`                                       | `complex`             | `print(type(x))`                                  | `<class 'complex'>`     |
| `x = ["apple", "banana", "cherry"]`            | `list`                | `print(type(x))`                                  | `<class 'list'>`        |
| `x = ("apple", "banana", "cherry")`            | `tuple`               | `print(type(x))`                                  | `<class 'tuple'>`       |
| `x = range(6)`                                 | `range`               | `print(type(x))`                                  | `<class 'range'>`       |
| `x = {"name": "John", "age": 36}`              | `dict`                | `print(type(x))`                                  | `<class 'dict'>`        |
| `x = {"apple", "banana", "cherry"}`            | `set`                 | `print(type(x))`                                  | `<class 'set'>`         |
| `x = frozenset({"apple", "banana", "cherry"})` | `frozenset`           | `print(type(x))`                                  | `<class 'frozenset'>`   |
| `x = True`                                     | `bool`                | `print(type(x))`                                  | `<class 'bool'>`        |
| `x = b"Hello"`                                 | `bytes`               | `print(type(x))`                                  | `<class 'bytes'>`       |
| `x = bytearray(5)`                             | `bytearray`           | `print(type(x))`                                  | `<class 'bytearray'>`   |
| `x = memoryview(bytes(5))`                     | `memoryview`          | `print(type(x))`                                  | `<class 'memoryview'>`  |
| `x = None`                                     | `NoneType`            | `print(type(x))`                                  | `<class 'NoneType'>`    |



```python
# Text Type: str
x = "Hello World"
print(type(x))  # <class 'str'>

# Numeric Type: int
x = 20
print(type(x))  # <class 'int'>

# Numeric Type: float
x = 20.5
print(type(x))  # <class 'float'>

# Numeric Type: complex
x = 1j
print(type(x))  # <class 'complex'>

# Sequence Type: list
x = ["apple", "banana", "cherry"]
print(type(x))  # <class 'list'>

# Sequence Type: tuple
x = ("apple", "banana", "cherry")
print(type(x))  # <class 'tuple'>

# Sequence Type: range
x = range(6)
print(type(x))  # <class 'range'>

# Mapping Type: dict
x = {"name": "John", "age": 36}
print(type(x))  # <class 'dict'>

# Set Type: set
x = {"apple", "banana", "cherry"}
print(type(x))  # <class 'set'>

# Set Type: frozenset
x = frozenset({"apple", "banana", "cherry"})
print(type(x))  # <class 'frozenset'>

# Boolean Type: bool
x = True
print(type(x))  # <class 'bool'>

# Binary Type: bytes
x = b"Hello"
print(type(x))  # <class 'bytes'>

# Binary Type: bytearray
x = bytearray(5)
print(type(x))  # <class 'bytearray'>

# Binary Type: memoryview
x = memoryview(bytes(5))
print(type(x))  # <class 'memoryview'>

# None Type: NoneType
x = None
print(type(x))  # <class 'NoneType'>

```

##### Python Data Types with Constructors

- If you want to specify the data type, you can use the following constructor functions:


| **Example**                            | **Data Type**       | **Constructor**                          |
|----------------------------------------|---------------------|------------------------------------------|
| `x = str("Hello World")`               | Text Type           | `str`                                    |
| `x = int(20)`                          | Numeric Type        | `int`                                    |
| `x = float(20.5)`                      | Numeric Type        | `float`                                  |
| `x = complex(1j)`                      | Numeric Type        | `complex`                                |
| `x = list(("apple", "banana", "cherry"))` | Sequence Type     | `list`                                   |
| `x = tuple(("apple", "banana", "cherry"))` | Sequence Type    | `tuple`                                  |
| `x = range(6)`                         | Sequence Type       | `range`                                  |
| `x = dict(name="John", age=36)`        | Mapping Type        | `dict`                                   |
| `x = set(("apple", "banana", "cherry"))` | Set Type          | `set`                                    |
| `x = frozenset(("apple", "banana", "cherry"))` | Set Type      | `frozenset`                              |
| `x = bool(5)`                          | Boolean Type        | `bool`                                   |
| `x = bytes(5)`                         | Binary Type         | `bytes`                                  |
| `x = bytearray(5)`                     | Binary Type         | `bytearray`                              |
| `x = memoryview(bytes(5))`             | Binary Type         | `memoryview`                             |

---

##### Notes:
- Each example shows the use of a specific type constructor.
- The `bool(5)` evaluates to `True` as any non-zero value in Python is considered `True`.
- This table provides a structured view of Python data types and their respective constructors.



```python
# Text Type: str
x = str("Hello World")
print(type(x))  # <class 'str'>

# Numeric Type: int
x = int(20)
print(type(x))  # <class 'int'>

# Numeric Type: float
x = float(20.5)
print(type(x))  # <class 'float'>

# Numeric Type: complex
x = complex(1j)
print(type(x))  # <class 'complex'>

# Sequence Type: list
x = list(("apple", "banana", "cherry"))
print(type(x))  # <class 'list'>

# Sequence Type: tuple
x = tuple(("apple", "banana", "cherry"))
print(type(x))  # <class 'tuple'>

# Sequence Type: range
x = range(6)
print(type(x))  # <class 'range'>

# Mapping Type: dict
x = dict(name="John", age=36)
print(type(x))  # <class 'dict'>

# Set Type: set
x = set(("apple", "banana", "cherry"))
print(type(x))  # <class 'set'>

# Set Type: frozenset
x = frozenset(("apple", "banana", "cherry"))
print(type(x))  # <class 'frozenset'>

# Boolean Type: bool
x = bool(5)  # Any non-zero value evaluates to True
print(type(x))  # <class 'bool'>

# Binary Type: bytes
x = bytes(5)
print(type(x))  # <class 'bytes'>

# Binary Type: bytearray
x = bytearray(5)
print(type(x))  # <class 'bytearray'>

# Binary Type: memoryview
x = memoryview(bytes(5))
print(type(x))  # <class 'memoryview'>

```

<a id="31-numbers"></a>
### 3.1 Numbers

##### There are three numeric types in Python:

- **int** : Int, or integer, is a whole number, positive or negative, without decimals, of unlimited length.
- **float** : Float, or "floating point number" is a number, positive or negative, containing one or more decimals. Float can also be scientific numbers with an "e" to indicate the power of 10.
- **complex** : Complex numbers are written with a "j" as the imaginary part.


```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex

print(type(x))
print(type(y))
print(type(z))
```


```python
# Integers
x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))



```


```python
# Float
x = 1.10
y = 1.0
z = -35.59

print(type(x))
print(type(y))
print(type(z))
```


```python
# Float Scientific Notation
x = 35e3
y = 12E4
z = -87.7e100

print(type(x))
print(type(y))
print(type(z))

```


```python
# Complex
x = 3+5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```

<a id="32-strings"></a>
### 3.2 Strings


```python
# Multipline Strings

aDoubleQuote = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(aDoubleQuote)


aSingleQuote = '''Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.'''
print(aSingleQuote)
```


```python
# Arrays

a = "Hello, World!"
print(a[4])
```


```python
# Looping Through a String

for x in "banana":
  print(x)
```


```python
# String Length

a = "Hello, World!"
print(len(a))
```


```python
# Check String (similar to INSTR in oracle)

txt = "The best things in life are free!"
print("free" in txt)

if "free" in txt:
  print("Yes, 'free' is present.")
```


```python
# Slicing a String

b = "Hello, World!"

print(b[2:5]) # Index starts from 0
print(b[:5]) # Slicing from Start
print(b[2:]) # Slice to the End
print(b[-5:-2]) # Slicing using Negitive Index
```


```python
# Modify Strings

a = "      Hello, World!     "

print(a.upper()) # Upper Case
print(a.lower()) # Lower Case
print(a.strip()) # Remove Whitespace
print(a.replace("H", "J")) # Replace String
print(a.split(",")) # Split String
```


```python
# String Concatenation

a = "Hello"
b = "World"
print(a + b)


a = "Hello"
b = "World"
c = a + " " + b
print(c)
```


```python
# Format - Strings

age = 36
txt = "My name is John, I am " + age
print(txt) 

# TypeError: can only concatenate str (not "int") to str


```

- A placeholder can contain variables, operations, functions, and modifiers to format the value. example : **{age}** below


```python
# F-Strings

age = 36
txt2 = f"My name is John, I am {age}" # F-Strings 
print(txt2)
```


```python
# Display the price with 2 decimals
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)

# A placeholder can contain Python code, like math operations
txt = f"The price is {20 * 59} dollars"
print(txt)
```

<a id="escape-character"></a>
#### Escape Character

- An escape character is a backslash `\` followed by the character you want to insert.


```python
# Below will throw Error 
txt = "We are the so-called "Vikings" from the north."
```


```python
# But this will work fine
txt = "We are the so-called \"Vikings\" from the north."
print(txt)
```

##### Other escape characters used in Python:

| **Code** | **Result**       | **Try it** |
|----------|------------------|------------|
| `\'`     | Single Quote     |            |
| `\\`     | Backslash        |            |
| `\n`     | New Line         |            |
| `\r`     | Carriage Return  |            |
| `\t`     | Tab              |            |
| `\b`     | Backspace        |            |
| `\f`     | Form Feed        |            |
| `\ooo`   | Octal value      |            |
| `\xhh`   | Hex value        |            |

---


<a id="33-booleans"></a>
### 3.3 Booleans

- Booleans represent one of two values: `True` or `False`


```python
# When you compare two values, the expression is evaluated and Python returns the Boolean answer

print(10 == 9)

# When you run a condition in an if statement, Python returns True or False:

a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

- The **bool()** function allows you to evaluate any value, and give you `True` or `False` in return,


```python
print(bool("Hello"))
print(bool(15))
```

- Most Values are True, except empty values, such as `()`, `[]`, `{}`, `""`, the number `0`, and the value `None`. And of course the value `False` evaluates to False


```python
bool(False)
bool(None)
bool(0)
bool("")
bool(())
bool([])
bool({})
```

<a id="34-lists"></a>
### 3.4 Lists

##### There are **four collection data types(built-in)** in the Python programming language:

- `List` is a collection which is `ordered` and `changeable`. `Allows duplicate` members.
- `Tuple` is a collection which is `ordered` and `unchangeable`. `Allows duplicate` members.
- `Set` is a collection which is `unordered`, `unchangeable`*, and `unindexed`. `No duplicate` members.
- `Dictionary` is a collection which is `ordered`** and `changeable`. `No duplicate` members.

> *`Set` items are unchangeable, but you can remove and/or add items whenever you like.

> **As of Python version 3.7, `dictionaries` are ordered. In Python 3.6 and earlier, dictionaries are unordered.


Lists are created using `square brackets`:


```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
```

- List items are **ordered**, changeable, and allow duplicate values.
- List items are indexed, the first item has index [0], the second item has index [1] etc.


- The list is **changeable**, meaning that we can change, add, and remove items in a list after it has been created.

<n>  



Since lists are indexed, lists can have **Duplicate** items:


```python
thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)
```

<a id="len()"></a>
#### len()

To determine how many items a list has, use the `len()` function:


```python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
```


```python
# List can contains different data type items
list1 = ["abc", 34, True, 40, "male"]
print(list1)

print(type(list1)) # type() function wil print <class 'list'> as output
```

<a id="access-list-items"></a>
#### Access List Items


```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]

print(thislist[2]) # Prints 3rd eliment from the Start
print(thislist[2:4]) # Prints 3rd & 4th eliments Note: The search will start at index 2 (included) and end at index 5 (not included).
print(thislist[:4]) # returns the items from the beginning to, but NOT including, "kiwi"
print(thislist[2:]) # returns the items from "cherry" to the end
print(thislist[-4:-1]) # returns the items from "orange" (-4) to, but NOT including "mango" (-1)
```


```python
# Check if Item Exists

if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")

if "garpe" in thislist:
  print("Yes, 'garpe' is in the fruits list")
```

<a id="change-list-items"></a>
#### Change List Items


```python
# change the value of a specific item by using the index number
thislist = ["apple", "banana", "cherry"]
thislist[1] = "watermelon" 
print(thislist)

# Change the values "banana" and "cherry" with the values "watermelon" and "muskmelon"
thislist[1:3] = ["watermelon", "muskmelon"] 
print(thislist)

# inserting more items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly
thislist = ["apple", "banana", "cherry"]
thislist[1:2] = ["watermelon", "muskmelon"] 
print(thislist) 

# nserting less items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly
thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"] 
print(thislist) 

# To insert a new list item, without replacing any of the existing values, we can use the insert() method
thislist = ["apple", "banana", "cherry"]
thislist.insert(len(thislist), "watermelon")
print(thislist)
thislist.insert(1, "muskmelon")
print(thislist)
```

<a id="add-list-items"></a>
#### Add List Items


```python
# To add an item to the end of the list, use the append() method
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)

# To insert a list item at a specified index, use the insert() method
thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange")
print(thislist)

# To append elements from another list to the current list, use the extend() method
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)

# The extend() method does not have to append lists, you can add any iterable object (tuples, sets, dictionaries etc.).
thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")
thislist.extend(thistuple)
print(thislist)
```

<a id="remove-list-items"></a>
#### Remove List Items


```python
# REMOVE
# The remove() method removes the specified item
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)

# If there are more than one item with the specified value, the remove() method removes the first occurrence
thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)

# POP
# The pop() method removes the specified index.
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)

# If you do not specify the index, the pop() method removes the last item
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)

# DEL
# The del keyword also removes the specified index
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)

# The del keyword can also delete the list completely.
thislist = ["apple", "banana", "cherry"]
del thislist # print(thislist) -- Will lead to error: "NameError: name 'thislist' is not defined"

# CLEAR
# The clear() method empties the list.The list still remains, but it has no content.

thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)

```

<a id="loop-lists"></a>
#### Loop Lists


```python
# For Loop
thislist = ["for", "banana", "cherry"]
for x in thislist:
  print(x)

print('----------------------------------')

# Loop Through the Index Numbers
thislist = ["forIndex", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])

print('----------------------------------')

# While Loop
thislist = ["while", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1

print('----------------------------------')

# List Comprehension
thislist = ["listComprehension", "banana", "cherry"]
[print(x) for x in thislist]
```

<a id="list-comprehension"></a>
#### List Comprehension

- `List comprehension` offers a shorter syntax when you want to create a new list based on the values of an existing list


```python
# Regular method
fruits = ["apple","banana","cherry"]
new_list=[]

for x in fruits:
    if "a" in x:
       new_list.append(x)

print(new_list)
```


```python
# Using List Comprehension
fruits = ["apple","banana","cherry"]
new_list=[]

new_list = [x for x in fruits if "a" in x]
print(new_list)
```


```python
newlist = [x for x in range(10)]
print(newlist)
```


```python
print(fruits)
newlist = [x if x != "banana" else "orange" for x in fruits]
print(newlist)
```

<a id="sort-lists"></a>
#### Sort Lists


```python
# Sort List Alphanumerically
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)

# Sort the list numerically
thislist = [100, 50, 65, 82, 23]
thislist.sort()
print(thislist)

#To sort descending, use the keyword argument reverse = True
thislist.sort(reverse = True)
print(thislist)

# Customize Sort Function
# You can also customize your own function by using the keyword argument key = function

def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc) # key = myfunc
print(thislist)

# Case Insensitive Sort
# By default the sort() method is case sensitive, resulting in all capital letters being sorted before lower case letters

thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort()
print(thislist)

# for a case-insensitive sort function, use str.lower as a key function
thislist.sort(key=str.lower)
print(thislist)

# Reverse Order
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.reverse()
print(thislist)
```

<a id="copy-lists"></a>
#### Copy Lists

- You cannot copy a list simply by typing list2 = list1, because: list2 will only be a reference to list1, and changes made in list1 will automatically also be made in list2.


```python
# Copy() method
list1 = ["apple","banana"]
list2 = list1
list2.append("dummy")
print(list1)
print(list2)

print('---------------------------')

# copy() method
list1 = ["apple","banana"]
list2 = list1.copy()
list2.append("dummy")
print(list1)
print(list2)

print('---------------------------')

# list() method
list1 = ["apple","banana"]
list2 = list(list1)
list2.append("dual")
print(list1)
print(list2)

print('---------------------------')

# Slicing method
list1 = ["apple","banana"]
list2 = list1[:]
list2.append("temp")
print(list1)
print(list2)

```

<a id="join-lists"></a>
#### Join Lists


```python
# + Operator 
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)


# append() 
for x in list2:
    list1.append(x)

print(list1)

# extend()
list1.extend(list2)
print(list1)


```

    ['a', 'b', 'c', 1, 2, 3]
    ['a', 'b', 'c', 1, 2, 3]
    ['a', 'b', 'c', 1, 2, 3, 1, 2, 3]
    

<a id="list-methods"></a>
#### List Methods


| Method     | Description                                                         |
|------------|---------------------------------------------------------------------|
| append()   | Adds an element at the end of the list                               |
| clear()    | Removes all the elements from the list                              |
| copy()     | Returns a copy of the list                                           |
| count()    | Returns the number of elements with the specified value             |
| extend()   | Adds the elements of a list (or any iterable), to the end of the current list |
| index()    | Returns the index of the first element with the specified value     |
| insert()   | Adds an element at the specified position                           |
| pop()      | Removes the element at the specified position                       |
| remove()   | Removes the item with the specified value                           |
| reverse()  | Reverses the order of the list                                      |
| sort()     | Sorts the list                                                      |

---

<a id="4-operators"></a>
## 4. Operators

##### Python divides the operators in the following groups:

- Arithmetic operators  
- Assignment operators  
- Comparison operators  
- Logical operators  
- Identity operators  
- Membership operators  
- Bitwise operators  



<a id="41-arithmetic-operators"></a>
### 4.1 Arithmetic operators


| Operator | Name            | Example  |
|----------|-----------------|----------|
| +        | Addition        | x + y    |
| -        | Subtraction     | x - y    |
| *        | Multiplication  | x * y    |
| /        | Division        | x / y    |
| %        | Modulus         | x % y    |
| **       | Exponentiation  | x ** y   |
| //       | Floor division  | x // y   |

---

<a id="42-assignment-operators"></a>
### 4.2 Assignment operators

| Operator | Example        | Same As     |
|----------|----------------|-------------|
| =        | x = 5          | x = 5       |
| +=       | x += 3         | x = x + 3   |
| -=       | x -= 3         | x = x - 3   |
| *=       | x *= 3         | x = x * 3   |
| /=       | x /= 3         | x = x / 3   |
| %=       | x %= 3         | x = x % 3   |
| //=      | x //= 3        | x = x // 3  |
| **=      | x **= 3        | x = x ** 3  |
| &=       | x &= 3         | x = x & 3   |
| |=       | x |= 3         | x = x | 3   |
| ^=       | x ^= 3         | x = x ^ 3   |
| >>=      | x >>= 3        | x = x >> 3  |
| <<=      | x <<= 3        | x = x << 3  |
| :=       | print(x := 3)  | x = 3       |

---


<a id="43-comparison-operators"></a>
### 4.3 Comparison operators


| Operator | Name                       | Example  |
|----------|----------------------------|----------|
| ==       | Equal                      | x == y   |
| !=       | Not equal                  | x != y   |
| >        | Greater than               | x > y    |
| <        | Less than                  | x < y    |
| >=       | Greater than or equal to   | x >= y   |
| <=       | Less than or equal to      | x <= y   |

---


<a id="44-logical-operators"></a>
### 4.4 Logical operators


| Operator | Description                            | Example                      |
|----------|----------------------------------------|------------------------------|
| and      | Returns True if both statements are true | x < 5 and x < 10             |
| or       | Returns True if one of the statements is true | x < 5 or x < 4              |
| not      | Reverses the result, returns False if the result is true | not(x < 5 and x < 10)       |

---


<a id="45-identity-operators"></a>
### 4.5 Identity operators


| Operator | Description                                  | Example     |
|----------|----------------------------------------------|-------------|
| is       | Returns True if both variables are the same object | x is y     |
| is not   | Returns True if both variables are not the same object | x is not y |

---

<a id="46-membership-operators"></a>
### 4.6 Membership operators


| Operator | Description                                                          | Example     |
|----------|----------------------------------------------------------------------|-------------|
| in       | Returns True if a sequence with the specified value is present in the object | x in y     |
| not in   | Returns True if a sequence with the specified value is not present in the object | x not in y |

---

<a id="47-bitwise-operators"></a>
### 4.7 Bitwise operators


| Operator | Name                  | Description                                                                 | Example   |
|----------|-----------------------|-----------------------------------------------------------------------------|-----------|
| &        | AND                   | Sets each bit to 1 if both bits are 1                                       | x & y     |
| \|       | OR                    | Sets each bit to 1 if one of two bits is 1                                  | x \| y    |
| ^        | XOR                   | Sets each bit to 1 if only one of two bits is 1                             | x ^ y     |
| ~        | NOT                   | Inverts all the bits                                                        | ~x        |
| <<       | Zero fill left shift  | Shift left by pushing zeros in from the right and let the leftmost bits fall off | x << 2    |
| >>       | Signed right shift    | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2    |

---

<a id="48-operator-precedence"></a>
### 4.8 Operator Precedence


| Operator                                   | Description                                                    |
|-------------------------------------------|----------------------------------------------------------------|
| ()                                        | Parentheses                                                    |
| **                                        | Exponentiation                                                 |
| +x  -x  ~x                                | Unary plus, unary minus, and bitwise NOT                       |
| *  /  //  %                               | Multiplication, division, floor division, and modulus          |
| +  -                                      | Addition and subtraction                                       |
| <<  >>                                    | Bitwise left and right shifts                                  |
| &                                         | Bitwise AND                                                    |
| ^                                         | Bitwise XOR                                                    |
| |                                         | Bitwise OR                                                     |
| ==  !=  >  >=  <  <=  is  is not  in  not in | Comparisons, identity, and membership operators                |
| not                                       | Logical NOT                                                    |
| and                                       | AND                                                            |
| or                                        | OR                                                             |

---

> ⚠️ **Note:** If two operators have the same precedence, the expression is evaluated from left to right.
