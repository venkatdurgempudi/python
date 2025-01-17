# Python Learning

### 1. Introduction

#### 1.1. Commands for Windows


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

#### 1.2. Commands for Mac/Linux


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

#### 1.3. Writing your First Code


```python
# Any of the below will work
print('Hello World!')
print("Hello World!")
```

#### 1.4.Comments


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

### 2. Variables

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

#### 2.1. Casting

- If you want to specify the data type of a variable, this can be done with casting.


```python
x = str(3)    # x will be '3'
print(x)
y = int(3)    # y will be 3
print(y)
z = float(3)  # z will be 3.0
print(z)
```

#### 2.2. Variable Names

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

    Python is awesome
    Python is awesome
    Pythonisawesome
    

- For numbers, the + character works as a mathematical operator:


```python
x = 5
y = 10
print(x + y)
```

    15
    

- print() function, when you try to combine a string and a number with the + operator, Python will give you an error:


```python
x = 5
y = "John"
print(x + y)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[57], line 3
          1 x = 5
          2 y = "John"
    ----> 3 print(x + y)
    

    TypeError: unsupported operand type(s) for +: 'int' and 'str'


- The **best way** to output multiple variables in the print() function is to separate them with **commas**, which even **support different data types**:


```python
x = 5
y = "John"
print(x, y)
```

    5 John
    

- Global and Local variables


```python
x = "Gloal awesome" # global variable

def myfunc():
  x = "Local fantastic"  # local variable
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

    Python is Local fantastic
    Python is Gloal awesome
    

---

### 3. Data Types

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

### Notes:
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


```python
echo %PATH%
```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```
