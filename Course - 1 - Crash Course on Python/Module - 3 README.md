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

---

### 1. Initialization  
Set starting values of variables **before** the loop begins.

### 2. Condition  
A **boolean expression** checked **before** each loop iteration.

### 3. Update  
Modify variables **inside** the loop to eventually make the condition false.

---

### Example in Python:

```python
# Initialization
count = 1

# While loop with condition
while count <= 3:
    print("Count is:", count)
    
    # Update
    count += 1
```

---

### Output:
```
Count is: 1  
Count is: 2  
Count is: 3
```

---

This loop starts with `count = 1`, runs while `count <= 3`, and increases `count` by 1 each time. When `count` becomes 4, the loop stops.

### Example

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

### Common Pitfalls

- **Infinite loop**: Forgetting to update the loop variable
- **Uninitialized variables**
- Use `break` to exit early

### Use Cases

- Retrying failed operations
- Waiting for user input
- Background monitoring tasks

---

## For Loops

### Basic Syntax

```python
for item in sequence:
    # do something
```

Iterates over:

- Lists
- Strings
- Ranges
- Files

### Example with `range()`

```python
for x in range(5):
    print(x)
```

**Output:**

```
0
1
2
3
4
```

---

## Range Parameters

```python
range(start, stop, step)
```

- `start` – default is 0
- `stop` – exclusive
- `step` – default is 1

### Example

```python
for i in range(2, 10, 2):
    print(i)
```

**Output:**

```
2
4
6
8
```

---

## Looping Over Strings

### For Loop
```python
greeting = "Hello"
for c in greeting:
    print(c)
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
- Nested loop 10,000 x 10,000 = 100 million iterations = ! ~27+ hours!

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
