### 2. Variables

#### Index

1. [Introduction to Variables](#introduction-to-variables)
2. [Casting](#21-casting)
3. [Variable Names](#22-variable-names)
4. [Assigning Multiple Variables](#assigning-multiple-variables)
5. [Unpacking Variables](#unpacking-variables)
6. [Printing Variables](#printing-variables)
7. [Global and Local Variables](#global-and-local-variables)

---

#### Introduction to Variables

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

---

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

---

#### 2.2. Variable Names

- A variable name must start with a letter or the underscore character.
- A variable name **cannot start with a number**.
- A variable name can only contain alphanumeric characters and underscores (A-z, 0-9, and _).
- Variable names are **case-sensitive** (age, Age, and AGE are three different variables).
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

- Techniques for readable variable names:

```python
# Camel Case
myVariableName = "John"

# Pascal Case
MyVariableName = "John"

# Snake Case
my_variable_name = "John"
```

---

#### Assigning Multiple Variables

- Python allows you to assign values to multiple variables in one line:

```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

- You can also assign the same value to multiple variables in one line:

```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

---

#### Unpacking Variables

- If you have a collection of values in a list, tuple, etc., Python allows you to extract the values into variables. This is called **unpacking**.

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```

---

#### Printing Variables

- The Python **print()** function is often used to **output variables**.

```python
# Single Variable
x = "Python is awesome"
print(x)

# Multiple variables
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)

# Using the + operator to concatenate strings
x = "Python"
y = "is"
z = "awesome"
print(x + " " + y + " " + z) # Adds space manually between words
```

- For numbers, the `+` character works as a mathematical operator:

```python
x = 5
y = 10
print(x + y)
```

- If you try to combine a string and a number with the `+` operator, Python will give an error:

```python
x = 5
y = "John"
print(x + y)  # This will raise a TypeError
```

- The **best way** to output multiple variables in the `print()` function is to separate them with **commas**, which supports different data types:

```python
x = 5
y = "John"
print(x, y)
```

---

#### Global and Local Variables

- Python allows variables to have a **global** or **local** scope.

```python
x = "Global awesome"  # Global variable

def myfunc():
  x = "Local fantastic"  # Local variable
  print("Python is " + x)

myfunc()

print("Python is " + x)
```
