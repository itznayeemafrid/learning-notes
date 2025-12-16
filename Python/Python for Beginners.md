# Syntax
```Text
Syntax is Grammar in coding.
```
---
# Statement
```Text
Statement is a line of code.
```
---
# Comment
- Use the `#` symbol at the **beginning of a line** to comment
- Use `ctrl + /` to comment quickly in vscode
```Python
# This is a comment

'''
This is a multi-line comment
'''

"""
This is a multi-line comment
"""
```
---
# Print
- Use `print()` to **display results** on the screen
```python
print(20+5)
```
---
# Variables
- A **variable** is like a **container** that stores a value in memory
```Python
age = 20        # 'age' is a variable, '20' is the value
name = "Afrid"
```
#### Rules for Naming Variables
- Variables must start with a **letter** or **underscore** (`_`), not a number
- Case-sensitive (`age` ≠ `Age`)
- Avoid Python keywords like `for`, `if`, `while` etc.
#### Different ways to print a variable and a message
```python
name = "Afrid"

# 1. Print the variable directly
print(name)

# 2. Print with string concatenation (+)
print("Hi," + name)

# 3. Print using a comma (adds a space automatically)
print("Hi,", name)

# 4. Print using an f-string (formatted string)
print(f"Hello, {name}")  # The 'f' lets you embed variables directly inside the string
```
---
# Data Types

- Every variable has a **data type** that tells Python what kind of data it is.

**Basic Data Types:**

| Data Type | Description                     | Example               |
| --------- | ------------------------------- | --------------------- |
| `int`     | Integer (whole number)          | `20`, `-5`, `0`       |
| `float`   | Decimal number (floating point) | `3.14`, `0.5`, `-1.0` |
| `str`     | String (text)                   | `"Afrid"`, `'Hello!'` |
| `bool`    | Boolean (True or False)         | `True`, `False`       |

---
# Operators
- operators are basically the signs that you use to do math

| **Operator** | **Operation Name**  | **Example** | **Result** |
| ------------ | ------------------- | ----------- | ---------- |
| `+`          | Addition            | `2 + 2`     | `4`        |
| `-`          | Subtraction         | `5 - 2`     | `3`        |
| `*`          | Multiplication      | `"$" * 5`   | `$$$$$`    |
| `/`          | Division            | `25 / 5`    | `5.0`      |
| `**`         | Exponent (Power)    | `2 ** 3`    | `8`        |
| `%`          | Modulus (Remainder) | `22 % 8`    | `6`        |
| `//`         | Floor Division      | `22 // 8`   | `2`        |
#### Comparison Operators

| **Operator** | **Meaning**           | **Example** |
| ------------ | --------------------- | ----------- |
| `==`         | Equal to              | `5 == 5`    |
| `!=`         | Not equal to          | `5 != 3`    |
| `>=`         | Greater than or equal | `8 >= 5`    |
| `<=`         | Less than or equal    | `3 <= 8`    |
#### Assignment Operators

| **Operator** | **Usage**    | **Instead of**      |
| ------------ | ------------ | ------------------- |
| `+=`         | `count += 1` | `count = count + 1` |
| `-=`         | `x -= 2`     | `x = x - 2`         |
| `*=`         | `total *= 3` | `total = total * 3` |
| `/=`         | `score /= 2` | `score = score / 2` |
#### Logical Operators

| **Operator** | **Meaning**                                      | **Example**       | **Result** |
| ------------ | ------------------------------------------------ | ----------------- | ---------- |
| `and`        | True if **both conditions** are True             | `5 > 2 and 3 < 4` | `True`     |
| `or`         | True if **at least one condition** is True       | `5 > 2 or 3 > 5`  | `True`     |
| `not`        | Reverses the result (True → False, False → True) | `not(5 > 2)`      | `False`    |

---
# User Input
- User input is taken as **string**, but can be converted
```python
name = input("Enter your name: ")
weight = float(input("Enter your weight: "))
```
---
# Importing Modules

- **Modules** let you use code written by others
- **Built-in modules**: `math`, `random`, `datetime`
- **External libraries** (installed separately): `numpy`, `pandas` — commonly used in AI and data science
```python
import math
print(math.sqrt(16))
```
---
# Use of colon (:)
- Whenever the next line is indented, the current line must end with `:`
- use case --> `if`, `elif`, `else`, `for`, `while`, `def` (function definitions), `class` (class definitions)
---
# Control Flow (If....Else conditional statements)
- It basically means If **this** is true, then **do this**, else (if it’s not true), **do something else**.
- Use `if` & `else` for two arguments.
- Use `if`, `elif` & `else` for more than two arguments.
```python
score = 75

if score >= 90:
    print("Grade: A")
elif score >= 75:
    print("Grade: B")
else:
    print("Grade: C")
```
---
# Loops
- `while` loops --> It keeps running **as long as** the condition stays `True`.
```python
count = 1
while count <= 5:
    print(count)
    count = count + 1
```

- `for` loops --> Used when you **already know** how many times to loop.
```python
for number in range(1, 6):
	print(number)
```
#### `break` and `continue`
- Used inside loops (`for` or `while`) to control the flow.
- `break` → exits the loop completely.
```python
 for num in range(1, 6):
	 if num == 3:
		 break
	 print(num)
```

- `continue` → skips the current iteration and moves to the next one.
```python
for num in range(1, 6):
    if num == 3:
        continue
    print(num)
```
---
# Data Structures
#### List (Sequence Types)
- List can store many items of same data types in one place using **square brackets `[ ]`**
- Lists are **mutable**, meaning you can **change** the items after creation
```python
fruits = ["apple", "banana", "cherry"]
my_list = [1, 2, 3]
```

- You can **modify** one item, **multiple items**, or even **replace the entire list**.

| **Action**            | **Syntax**        | **Example**           |                       | **Result**     |
| --------------------- | ----------------- | --------------------- | --------------------- | -------------- |
| Change **one** item   | `list[index]`     | `nums = [1, 2, 3]`    | `nums[1] = 9`         | `[1, 9, 3]`    |
| Change **some** items | `list[start:end]` | `nums = [1, 2, 3, 4]` | `nums[1:3] = [8, 9]`  | `[1, 8, 9, 4]` |
| Replace **all** items | `list[:]`         | `nums = [1, 2, 3]`    | `nums[:] = [4, 5, 6]` | `[4, 5, 6]`    |
#### Tuple (Sequence Types)
- Tuple can store many items of any data types in one place using **parenthesis `()`
- Tuples are **immutable**, meaning you cannot **change** the items after creation
 ```python
 my_tuple = ("hello", 123, 3.14, True, [1, 2, 3])
 ```

#### Set
- `set()` or `{}` is used to create a set.
- Sets store **unique items** and are **unordered**. **Duplicates are not allowed**.
```python
fruits = {"apple", "banana", "cherry"}
fruits.add("orange")     # Add an item
fruits.remove("banana")  # Remove an item
```
---
#### Dictionary

- `dict` stores **key-value pairs** in a single variable.
- Keys must be **unique** and **immutable**; values can be **any type**.
```python
person = {"name": "Afrid", "age": 20, "city": "Dhaka"}
print(person["name"])         # Access value by key → Afrid
person["age"] = 21             # Update value
person["country"] = "BD"   # Add new key-value pair
```
---
#### Range (Sequence Types)
- `range()` --> gives you a list of numbers **in order** (mostly used with `for` loops)
```python
for i in range(2, 6):
	print(i)
```
---
# Function Definition (`def`)
- `def function_name(parameters):` is a function declaration
- **parameter** → placeholder; **argument** → actual value passed while calling
- **`return`** → sends a value back from the function so it can be used later
```python
# Function without return
def greet_person(name):
    print(f"Hello, {name}!")

greet_person("Afrid")  # Output: Hello, Afrid!

# Function with return
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3)
print(result)  # Output: 8
```
#### Calling a Function
- To run the function, just call its name with parentheses:
```Python
greet_person("Afrid")  # Output: Hello, Afrid!
```
#### Attributes
- **Attributes** are **properties or characteristics** of something.
- They **store information** and **do not need parentheses**.
```python
object.color    # the color of the object
object.size     # the size of the object
```
#### Methods
- **Methods** are **actions or things an object can do**.
- They **require parentheses** because you are calling a function.
```python
object.move()   # tells the object to move
object.show()   # tells the object to display itself
```

>[!tip]
> **Attributes = “what it has”** → properties, details
> **Methods = “what it can do”** → actions, behaviors

---
# Returning Values
- Functions can send back a value using `return`
- It lets you **use the result** later in your program.
- Without `return`, functions just do something but don’t send a result back.
```Python
def add(a, b):
	return a + b
result = add(5, 3)
	print(result)    # 8
```
---
# Classes
- `class` --> groups related data and methods.
- **self** --> represents the instance of the class. Used to access attributes and methods.
- **Methods** are functions defined inside a class
- Methods can use and modify **attributes** (data stored in `self`)
```python
class Student:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        print(f"Hello, {self.name}!")

s = Student("Afrid")
s.greet()  # Output: Hello, Afrid!
```
---
# Basic Error Handling

- Used to **handle runtime errors** without crashing the program
- `try` --> code that might cause an error
- `except` --> handles the error if it occurs
- `finally` --> optional, runs no matter what
```python
try:
	x = 5 / 0
	
except ZeroDivisionError:
	print("Cannot divide by zero!")
	
finally:
	print("Done")
```
---
# File I/O (Input & Output)

- Used to **read from** and **write to** files.
- Modes:
    - `"r"` → read (file must exist)
    - `"w"` → write (overwrites existing content)
    - `"a"` → append (adds to the end of the file)
    - `"x"` → create (fails if file already exists)
- The `with open()` statement automatically **closes the file** after use.
```python
# Read
with open("data.txt", "r") as file:
    content = file.read()
    print(content)

# Write (overwrite)
with open("data.txt", "w") as file:
    file.write("Hello, Afrid!")

# Append
with open("data.txt", "a") as file:
    file.write("\nWelcome back!")

# Create new file (error if it already exists)
with open("newfile.txt", "x") as file:
    file.write("This file was just created.")
```
---
# List Comprehensions

- A **compact way** to create lists using a single line of code.
- Combines **loop** and **expression** inside `[]`.
- Often used for **cleaner, faster** list creation.
```python
squares = [x * x for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```
---
