
### Module 0 - Syntax
- In a single word, **Syntax is Grammar** in coding.
---

### Module 1 - Comment
- Use the `#` symbol at the beginning of a line to make it a comment about code
	- #example 
	- `# this is a comment`
---

### Module 2 - Print
- Use `print()` to **show messages** or **results** on the screen.
- Whatever you put inside `"` or `'` will be shown **exactly as it is**.
	- #example 
	- `print("Hello World")`
	- `" "` is used to show the exact text that you gave
---

### Module 3 - Variables
- A **variable** is like a **label** or **name** that stores a value in memory.
- Think of it like a **container** that holds something you can use later.
	- #example
	- `name = "Khalid"`
	- Here, `name` is the **variable**, and `"Khalid"` is the **value** (a string) assigned to it using `=`.
	- to print this run `print(name)`
	- to print this with a message run `print("Hi," + name)`
	- or `print("Hi,",name)`
	- or `print(f"Hello, {name}")`
	- The `f` before the string means it's a **formatted string**, allowing you to include the value of `name` inside the message.
---

### Module 4 - Data Types
- When you give a value to Python, it has a **type** — it helps Python understand what the value is and how to treat it.
- we'll see how to assign Data Types in '**Module 4 - User Input**'
- Don't forget quotes `" "` on strings.
	- #example 

| **Code Example**   | **Type** | **Full Form / Description**               |
| ------------------ | -------- | ----------------------------------------- |
| `name = "Khalid"`  | `str`    | String — used for text                    |
| `age = 25`         | `int`    | Integer — used for whole numbers          |
| `price = 10.25`    | `float`  | Floating-point — used for decimal numbers |
| `is_active = True` | `bool`   | Boolean — used for True/False values      |

---

### Module 5 - Operators
- operators are basically the signs that you use to do math
	- #example 

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

---

### Module 6 - User Input
- **User input** lets your program **ask the user** to type something when it runs.
- This makes your code **interactive**.
- Whatever the user types is taken in as a **string**, so if you need numbers, you often convert it as below.
	- #example 
	- `weight = float(input("Enter your weight in kg: "))`
---

### Module 7 - Use of colon (:)
- Whenever the next line is indented, the current line must end with `:`
- use case --> `if`, `elif`, `else`, `for`, `while`, `def` (function definitions), `class` (class definitions)
---

### Module 8 -  If....Else (conditional statements)
- It basically means If **this** is true, then **do this**, else (if it’s not true), **do something else**.
- Use `if` & `else` for two arguments.
- Use `if`, `elif` & `else` for more than two arguments.
- #example 
- score = 75
	if score >= 90:
	    print("Grade: A")
	elif score >= 75:
	    print("Grade: B")
	else:
	    print("Grade: C")
---

### Module 9 - Loops
- `while` loops --> It keeps running **as long as** the condition stays `True`.
	- #example 
	- count = 1
	  while count <= 5:
		    print(count)
		    count = count + 1
	
- `for` loops --> Used when you **already know** how many times to loop.
	- #example 
	- for number in range(1, 6):
	    print(number)
---

### Module 10 - List, Tuple & Range
- **`list`** --> A **list is a collection** of many items stored in one place, it uses **square brackets `[ ]`**.
- Lists are **mutable**, meaning you can **change** the items inside the list.
	- #example 
	- `fruits = ["apple", "banana", "cherry"]`
	- `my_list = [1, 2, 3]`

- `tuple` --> A **list is a value** that stores **many items** in one place using `()` parenthesis
- `( )` means unchangeable/ immutable, so `tuple` is a immutable list
	- #example 
	- `my_tuple = (1, 2, 3)`

- `range()` --> gives you a list of numbers **in order**
- use with `for` loops
	- #example 
	- for i in `range(2, 6)`:
	    print(i)
---
### Module 11 – `def` (Define Function)
- `def` is used to define a function.
- Inside `()`, write a variable (called a **parameter**).
- When calling the function, give a value (called an **argument**).

#example 

```python
def greet_person(name):
    print(f"Hello, {name}!")

greet_person("Afrid")```
```

### Module 12 - Modify a List
- Lists are **changeable (mutable)** — you can update the items anytime.
- You can **modify** one item, **multiple items**, or even **replace the entire list**.
	- `[index]` = change one
	- `[start:end]` = change some
	- `[:]` = change all

	- #example 
	- `fruits = ["apple", "banana", "cherry"]`
	
	**1. Modify One Item**
	- `fruits[0] = "orange"`  --> (changes "apple" to "orange")

	**2. Modify Multiple Items**
	- `fruits[1:3] = ["grape", "kiwi"]` --> (replaces "banana" and "cherry")

	**3. Replace the Whole List**
	- `fruits[:] = ["kiwi", "orange", "pear"]` --> (replaces the whole list with a new one)
---

### Projects (Module 1 - 11)

| **Project Name**                   | **Skills Used**                                       | **Description**                                                              |
| ---------------------------------- | ----------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Simple Calculator**              | `input()`, variables, operators, if-else              | A calculator that takes two numbers and an operation, then shows the result. |
| **Grade Checker**                  | `input()`, float/int, if-elif-else                    | Ask for a score and display the corresponding grade (A/B/C).                 |
| **Even or Odd Checker**            | `input()`, int conversion, `%` operator, if-else      | Check whether a number is even or odd based on user input.                   |
| **Favorite Fruits App**            | List, user input, list modification                   | Allow the user to update a list of fruits and display the modified list.     |
| **Number Guessing Game**           | `while` loop, `if` statements, user input, comparison | User guesses a number until they get it right.                               |
| **Shopping Cart**                  | List, user input, loop                                | User adds items to a cart, then shows the final list when done.              |
| **Multiplication Table Generator** | `input()`, `for` loop, formatted strings              | Generate and display the multiplication table for a given number.            |
| **Basic Login System**             | Variables, user input, `if-else`                      | Simple login system with a stored username and password.                     |

