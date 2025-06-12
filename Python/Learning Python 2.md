### Lesson 2

1. **Expressions**
    
    - Made up of values and operators
        
    - Produces a single result  
        **Example:**  
        `2 + 2` → **4**
        

---

2. **Data Types**  
    _(Covered in earlier notes)_
    

---

3. **String Concatenation**
    
    - Combines multiple strings into one  
        **Example:**  
        `'Alice' + ' ' + 'Max'` → **'Alice Max'**
        

---

4. **String Replication**
    
    - Repeats a string multiple times  
        **Example:**  
        `'Alice' * 3` → **'AliceAliceAlice'**
        

---

5. **Variables**  
    _(Covered in earlier notes)_
    

---

6. **Statement**
    
    - An instruction in a program
        
    - Examples: assignment, print, etc.  
        **Example:**
        
    
    ```python
    x = 5          # Assignment statement  
    print('Hello') # Print statement
    ```
    

---

### Lesson 3

1. **Function**
    
    - Has a name and `()`
        
    - Acts like a mini-program  
        **Example:**
        
    
    ```python
    print('Hello world')  # 'print' is the function name, 'Hello world' is the argument
    ```
    

---

2. **Comment**  
    _(Covered in earlier notes)_
    

---

3. **Converting Data Types**
    
    - Convert one type to another  
        **Example:**  
        `str(26)` → **'26'**
        

---

### Lesson 4

1. **Boolean Data Type**
    
    - Only two values: `True`, `False`  
        **Example:**  
        `42 == 42` → **True**
        

---

2. **Comparison Operators**  
    _(Covered in earlier notes)_
    
    - `==` checks equality
        
    - `=` is for assignment
        

---

3. **Boolean Operators**
    
    - `and`, `or`, `not`
        
    
    `and` Truth Table:
    
    |A|B|A and B|
    |---|---|---|
    |True|True|True|
    |True|False|False|
    |False|True|False|
    |False|False|False|
    
    `or` Truth Table:
    
    |A|B|A or B|
    |---|---|---|
    |True|True|True|
    |True|False|True|
    |False|True|True|
    |False|False|False|
    
    `not` Truth Table:
    
    |A|not A|
    |---|---|
    |True|False|
    |False|True|
    
    **Example:**
    
    ```python
    myAge = 26
    myPet = 'cat'
    print(myAge > 20 and myPet == 'cat')  # True
    ```
    

---

### Lesson 5

1. **`if` Statement**
    
    - Runs code only if the condition is true  
        **Example:**
        
    
    ```python
    if name == 'Alice':
        print('Hello Alice')
    ```
    

---

2. **Flowchart Diagram**
    
    - Helps understand code logic
        
    - Use [pythontutor.com](https://pythontutor.com/) to visualize
        

---

3. **Truthy & Falsey Values**
    
    - `Falsey`: empty string, 0, `None`, empty list, etc.
        
    - `Truthy`: everything else
        
    - Use `bool(value)` to test
        
    
    **Example:**
    
    ```python
    name = input('Enter your name: ')
    if name:
        print('Thank you for entering a name')
    else:
        print('You did not enter a name')
    ```
    

---

### Lesson 6

1. **`while` Loop**
    
    - Keeps running as long as the condition is true  
        **Example:**
        
    
    ```python
    spam = 0
    while spam < 5:
        print('Hi')
        spam += 1
    ```
    

---

2. **Infinite Loop**
    
    - Never ends unless interrupted
        
    - Stop with `Ctrl + C`  
        **Example:**
        
    
    ```python
    while True:
        print('Hello')
    ```
    

---

3. **`break` and `continue` Statements**
    
    - `break`: exits the loop
        
    - `continue`: skips to next iteration
        
    
    **Example:**
    
    ```python
    spam = 0
    while spam < 5:
        spam += 1
        if spam == 3:
            continue
        print(f'spam is {spam}')
    ```
    

---

### Lesson 7

1. **`range()` Function**
    
    - Creates a sequence of numbers
        
    - `range(start, stop, step)`  
        **Example:**
        
    
    ```python
    total = 0
    for num in range(101):
        total += num
    print(total)  # 5050
    ```
    

---

### Lesson 8

1. **Standard Library Modules**
    
    - Use `import module_name`
        
    - Example modules: `math`, `random`, `sys`, `os`
        
    - To avoid using `random.` every time:  
        `from random import *` → then use `randint()`
        

---

2. **`sys` Module**
    
    - Use `sys.exit()` to end program early  
        **Example:**
        
    
    ```python
    import sys
    print('Hello')
    sys.exit()
    print('This will not run')
    ```
    

---

3. **Third-Party Modules**
    
    - Must be installed first  
        **Example:** `pyperclip` module
        

---

### Lesson 9

1. **`def` Statement (Defining Functions)**
    
    - `def` creates a function
        
    - Arguments go inside `()`  
        **Example:**
        
    
    ```python
    def hello():
        print('Hey man')
        print('What to do man!')
    hello()
    
    def greet(name):
        print(f"Hello {name}")
    greet("Alice")
    ```
    

---

2. **Return Statement**
    
    - Sends a value back when function is called  
        **Example:**
        
    
    ```python
    def plusOne(number):
        return number + 1
    print(plusOne(5))  # 6
    ```
    

---

3. **Keyword Arguments**
    
    - `end=` avoids newline
        
    - `sep=` changes separator  
        **Examples:**
        
    
    ```python
    print('Hello', end=' ')
    print('World')  # Hello World
    
    print("cat", "dog", "mouse", sep="ABC")  # catABCdogABCmouse
    ```
    

---

### Lesson 10

1. **Global vs Local Scope**
    

|Rule|
|---|
|Global code **can’t access** local variables.|
|Local code **can read** global variables.|
|Local variables in one function **aren’t visible** in another.|
|Same variable name can exist in **different scopes** without conflict.|

- Use `global` inside a function to modify a global variable.
    

**Example:**

```python
def example():
    global name
    name = "Alice"
```

### Lesson 11

1. **Try & except statement**

- Keeps code running even if an error occurs  
- Define error type to handle it  
- Prevents program from crashing  
- Useful for input validation  

**Example:**  
```python
def div42by(divideBy):
    try:
        return 42 / divideBy
    except ZeroDivisionError:
        print("Error: you tried to divide by zero.")
```

### Lesson 13

1. **List**

- A list holds multiple values inside square brackets `[]`, separated by commas.  
- Each value in the list is called an *item*.  
- List items are indexed starting at 0 (not 1). For example, if `spam = ['cat', 'rat']`, then `spam[0]` is `'cat'`.  
- Lists can contain other lists (nested lists). For example,  
  `spam = [['cat', 'rat'], [10, 20]]`  
  To access `'rat'`, use `spam[0][1]`.  
- Negative indexing counts from the end: `-1` is the last item, `-2` the second last, and so on.  
- You can get a single item by index (`spam[1]`), or multiple items by slice (`spam[1:3]` gets items at index 1 and 2).  
- Indexing returns one item, slicing returns a list of items.  
- You can change a list item by assigning a new value:  
  `spam[1] = 'hey'` will change the second item.  
- Slices can also be open-ended:  
  `spam[:2]` means items from start up to (but not including) index 2,  
  `spam[1:]` means items from index 1 to the end.  
- Use `del spam[2]` to delete the item at index 2.  
- The `list()` function converts an iterable (like a string or tuple) into a list.  
- Use `in` and `not in` to check if a value exists in the list, for example:  
  `42 in ['hey', 'man']` returns `False`.  

**Example:**  
```python
spam = ['cat', 'rat', 'bat']
print(spam[0])      # Output: cat
print(spam[-1])     # Output: bat
print(spam[1:3])    # Output: ['rat', 'bat']

spam[1] = 'hey'
print(spam)         # Output: ['cat', 'hey', 'bat']

del spam[2]
print(spam)         # Output: ['cat', 'hey']

print(42 in spam)   # Output: False
```

### Lesson 14

1. **`range` vs `list`**
    

- `range()` is a list-like function. For example:  
    `range(4)` → `[0, 1, 2, 3]`
    
- `list(range(0, 10, 2))` → `[0, 2, 4, 6, 8]`
    

**Example:**

```python
supplies = ['pen', 'binders', 'staplers']
for i in range(len(supplies)):
    print(f"Index {str(i)} in supplies is {supplies[i]}")
```

---

2. **Multiple Assignment Trick**
    

- Assign multiple list values to variables in one line
    

**Example:**

```python
cat = ['fat', 'orange']
size = cat[0]
color = cat[1]

# Instead of above, use:
size, color = cat
# Or:
size, color = 'fat', 'orange'
print(size)
```

---

3. **Swap Variables**
    

- Swap two variable values easily
    

**Example:**

```python
a = 'AAA'
b = 'BBB'
a, b = b, a
```

---

4. **Augmented Assignment Operators**  
    _(Covered in earlier notes)_
    

**Example:**

```python
spam = spam + 1
spam += 1
```

---

### Lesson 15

1. **Methods**
    

- Methods are functions that are _called on_ values
    
- `spam.insert(1, 'hola')` → adds `'hola'` at index 1
    
- `spam.append('bye')` → adds `'bye'` at the end
    
- `spam.remove('hi')` → removes first occurrence of `'hi'`
    
- `spam.sort()` → sorts list in ASCII-betical order
    
- `spam.sort(key=str.lower)` → true alphabetical sort
    
- `spam.sort(reverse=True)` → reverses the list order
    
- Lists can’t be sorted if they contain both strings and integers
    
- Methods like `append()` work only on specific data types (e.g., list)
    

**Example:**

```python
spam = ['hello', 'hi']
print(spam.index('hello'))  # Output: 0
```