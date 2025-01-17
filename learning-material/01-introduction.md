### 01. Introduction

#### Index

1. [Commands for Windows](#11-commands-for-windows)
2. [Commands for Mac/Linux](#12-commands-for-maclinux)
3. [Writing your First Code](#13-writing-your-first-code)
4. [Comments](#14comments)

---

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

---

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

---

#### 1.3. Writing your First Code

```python
# Any of the below will work
print('Hello World!')
print("Hello World!")
```

---

#### 1.4. Comments

```python
# This is how we can write Single Line comments with "#" at the beginning
print("Comments")

"""
This is how
multi-line comments can be written
in the python
"""
```
