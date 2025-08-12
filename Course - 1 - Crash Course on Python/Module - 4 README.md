# Python Looping Concepts for Automation

---

## What Are Loops?

A **loop** is a programming structure that repeats a block of code multiple times, either while a condition is true (`while` loop) or for every item in a sequence (`for` loop).

They are essential for:

- Repeating tasks
- Processing sequences
- Automating repetitive operations

---

## While Loops – Core Components

A **while loop** repeatedly executes a block of code **as long as a condition is true**. It has three main parts:

### 1. Initialization
Set starting values of variables **before** the loop begins.

### 2. Condition
A **boolean expression** checked **before** each loop iteration.

### 3. Update
Modify variables **inside** the loop to eventually make the condition false.

---

### Example in Python

```python
# Initialization
count = 1

# While loop with condition
while count <= 3:
    print("Count is:", count)
    
    # Update
    count += 1
```

**Output:**
```
Count is: 1  
Count is: 2  
Count is: 3
```

This loop starts with `count = 1`, runs while `count <= 3`, and increases `count` by 1 each time. When `count` becomes 4, the loop stops.

---

### More Example

```python
x = 0
while x < 5:
    print("Not there yet, x=" + str(x))
    x += 1
print("x=" + str(x))
```

**Output:**
```
Not there yet, x=0
Not there yet, x=1
Not there yet, x=2
Not there yet, x=3
Not there yet, x=4
x=5
```

---

## Common Pitfalls in While Loops

### Infinite Loop

Occurs when the loop condition **never becomes false**, often due to **missing update**.

```python
count = 1
while count <= 3:
    print("Count is:", count)
    # Missing: count += 1
```

**Output:**
```
Count is: 1  
Count is: 1  
Count is: 1  
... (infinite)
```

---

### Uninitialized Variables

Using a variable **before assigning a value** causes an error.

```python
while num < 3:
    print(num)
    num += 1
```

**Output:**
```
NameError: name 'num' is not defined
```

---

### Use `break` to Exit Early

```python
count = 1
while True:
    print("Count is:", count)
    if count == 2:
        break
    count += 1
```

**Output:**
```
Count is: 1  
Count is: 2
```

---

## Use Cases of While Loops

### Retrying Failed Operations

```python
attempts = 0
success = False

while not success and attempts < 3:
    print("Trying...")
    # Simulate failure
    success = False
    attempts += 1
```

**Output:**
```
Trying...  
Trying...  
Trying...
```

---

### Waiting for User Input

```python
user_input = ""
while user_input != "exit":
    user_input = input("Type 'exit' to stop: ")
```

**Example run output:**
```
Type 'exit' to stop: hello  
Type 'exit' to stop: try again  
Type 'exit' to stop: exit
```

---

### Background Monitoring Tasks

```python
import time

counter = 0
while counter < 3:
    print("Monitoring...")
    time.sleep(1)
    counter += 1
```

**Output:**
```
Monitoring...  
(wait 1s)  
Monitoring...  
(wait 1s)  
Monitoring...
```

---

These examples help clarify how to properly use `while` loops and avoid common mistakes.

---

## For Loops in Python

A **for loop** is used to iterate over a **sequence** (like a list, string, range, or file).

**Basic Syntax**
```python
for item in sequence:
    # do something
```

---

### Iterates Over:

#### 1. Lists
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**Output:**
```
apple  
banana  
cherry
```

---

#### 2. Strings
```python
word = "hi"
for char in word:
    print(char)
```

**Output:**
```
h  
i
```

---

#### 3. Ranges
```python
for i in range(3):
    print(i)
```

**Output:**
```
0  
1  
2
```

---

#### 4. Files
```python
# Assuming a file named 'data.txt' contains:
# Line 1
# Line 2

with open('data.txt', 'r') as file:
    for line in file:
        print(line.strip())
```

**Output:**
```
Line 1  
Line 2
```

---

### Summary
- Use `for` loops when **know how many times** or **what to loop over**.
- It's great for **collections**, **strings**, **numeric ranges**, and **file reading**.

---

### With Indexing (`range()` + `len()`)
```python
greeting = "Hello"
for i in range(len(greeting)):
    print(greeting[i])
```

**Output:**
```
H
e
l
l
o
```

---

### While Loop with Index
```python
greeting = "Hello"
index = 0
while index < len(greeting):
    print(greeting[index])
    index += 1
```

**Output:**
```
H
e
l
l
o
```

---

### While Loop with Slicing
```python
greeting = "Hello"
index = 0
while index < len(greeting):
    print(greeting[index:index+1])
    index += 1
```

**Output:**
```
H
e
l
l
o
```

---

## Nested Loops

### Domino Example
```python
for left in range(7):
    for right in range(left, 7):
        print(f"[{left}|{right}]", end=" ")
    print()
```

**Output:**
```
[0|0] [0|1] [0|2] [0|3] [0|4] [0|5] [0|6] 
[1|1] [1|2] [1|3] [1|4] [1|5] [1|6] 
[2|2] [2|3] [2|4] [2|5] [2|6] 
[3|3] [3|4] [3|5] [3|6] 
[4|4] [4|5] [4|6] 
[5|5] [5|6] 
[6|6]
```

---

### Team Matchups Example
```python
teams = ['Dragons', 'Wolves', 'Pandas', 'Unicorns']
for home_team in teams:
    for away_team in teams:
        if home_team != away_team:
            print(f"{home_team} vs {away_team}")
```

**Output:**
```
Dragons vs Wolves
Dragons vs Pandas
Dragons vs Unicorns
Wolves vs Dragons
Wolves vs Pandas
Wolves vs Unicorns
Pandas vs Dragons
Pandas vs Wolves
Pandas vs Unicorns
Unicorns vs Dragons
Unicorns vs Wolves
Unicorns vs Pandas
```

---

## Looping for Math

### Sum and Average
```python
values = [23, 52, 59, 37, 48]
sum = 0
length = 0
for value in values:
    sum += value
    length += 1
print("Total sum:", sum, "- Average:", sum / length)
```

**Output:**
```
Total sum: 219 - Average: 43.8
```

---

### Product (Factorial)
```python
product = 1
for n in range(1, 10):
    product *= n
print(product)
```

**Output:**
```
362880
```

---

## List Comprehensions

### Example: Squared Numbers
```python
numbers = [1, 2, 3, 4, 5]
squared = [x ** 2 for x in numbers]
print(squared)
```

**Output:**
```
[1, 4, 9, 16, 25]
```

---

## Common Pitfalls & Performance

- **Infinite loops**: Always update loop variables!
- **Large data**: Avoid deep nested loops unless necessary.
- **Missing initialization**: Always initialize your sum, count, index, etc.

Performance estimates:
- Looping over 10,000 items = ~10 seconds (1ms/item)
- Nested loop 10,000 x 10,000 = 100 million iterations = ~27+ hours!

Use tools like:
- `break`, `continue`
- `enumerate()`, `zip()`, `map()` for efficiency

---

## Slicing Strings

```python
s = "Greetings, Earthlings"
print(s[0])         # G
print(s[4:8])       # ting
print(s[11:])       # Earthlings
print(s[:5])        # Greet
print(s[-10:])      # Earthlings
print(s[0::2])      # Getns atlns
print(s[::-1])      # sgnilhtraE ,sgniteerG
print(s[55:])       # (empty string)
```

**Output:**
```
G
ting
Earthlings
Greet
Earthlings
Getns atlns
sgnilhtraE ,sgniteerG
```

---

## Joining Strings

```python
print("Hello" + " " + "world")
print(" ".join(["Hello", "world"]))

name = "Alice"
print("Hello, " + name + "!")
```

**Output:**
```
Hello world
Hello world
Hello, Alice!
```

---

## Combine Slice + Join: Phone Formatter

```python
def format_phone(p):
    return "(" + p[:3] + ") " + p[3:6] + "-" + p[-4:]

print(format_phone("2025551212"))
```

**Output:**
```
(202) 555-1212
```

---

## Summary

- Use `for`, `while`, and `range()` to loop through strings and lists.
- Use `[start:end:step]` for slicing.
- Use `+` or `.join()` for combining strings.
- Avoid nested loops with huge data sizes.
- Use list comprehensions for concise list creation.
- Always initialize variables and update loop counters.

---

## Recursion

**Recursion** is a programming technique where a function calls itself to solve a smaller version of the original problem.

It’s useful for problems that can be broken down into similar sub-problems (like **factorials**, **Fibonacci sequences**, etc.).

---

##### Example: Factorial Function Using Recursion
```python
def factorial(n):
    if n < 2:
        return 1
    return n * factorial(n - 1)
```

**Example usage**
```python
print(factorial(5))
```

**Output:**
```
120
```

**Step-by-step recursion for factorial(5):**
```
# factorial(5)
# = 5 × factorial(4)
# = 5 × (4 × factorial(3))
# = 5 × (4 × (3 × factorial(2)))
# = 5 × (4 × (3 × (2 × factorial(1))))
# = 5 × (4 × (3 × (2 × 1)))
# = 120
```

- This function returns `1` if `n < 2` (**base case**).
- Otherwise, it returns `n * factorial(n-1)` (**recursive case**).
- This continues until it reaches the base case.

---

### With Print Statements for Clarity

```python
def factorial(n):
  print("Factorial called with " + str(n))
  if n < 2:
    print("Returning 1")
    return 1
  result = n * factorial(n-1)
  print("Returning " + str(result) + " for factorial of " + str(n))
  return result
```

**Calling `factorial(4)` Produces:**
```
Factorial called with 4  
Factorial called with 3  
Factorial called with 2  
Factorial called with 1  
Returning 1  
Returning 2 for factorial of 2  
Returning 6 for factorial of 3  
Returning 24 for factorial of 4  
```

**Final Output:**
```
24
```

---

## **Recursion for Hierarchical Structures**

```python
def count_files(dir_structure):
    if dir_structure is None:
        return 0
    total = len(dir_structure.get("files", []))
    for sub in dir_structure.get("subdirs", []):
        total += count_files(sub)
    return total
```

**Example**
```python
filesystem = {
    "files": ["a.txt", "b.txt"],
    "subdirs": [
        {"files": ["c.txt"], "subdirs": []}
    ]
}
print(count_files(filesystem))
```

**Output:**
```
3
```

---

## Key Takeaway

Recursion solves problems by breaking them into smaller subproblems, with each recursive call approaching a **base case** that ends the loop. It's powerful but must include a proper base case to avoid **infinite recursion**.

---
