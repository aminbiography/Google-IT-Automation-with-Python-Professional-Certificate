# Python Looping Concepts for Automation

---

## What Are Loops?

A **loop** is a programming structure that repeats a block of code multiple times, either while a condition is true (`while` loop) or for every item in a sequence (`for` loop).

They are essential for:

- Repeating tasks
- Processing sequences
- Automating repetitive operations

---

## While Loops

### Core Components

- **Initialization**: Set starting values.
- **Condition**: Evaluated before each iteration.
- **Update**: Change variables inside the loop.

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

Strings are sequences of characters, and you can loop over each character.

### For Loop

```python
greeting = "Hello"
for c in greeting:
    print(c)
```

### With Indexing

```python
for i in range(len(greeting)):
    print(greeting[i])
```

### While Loop with Index

```python
index = 0
while index < len(greeting):
    print(greeting[index])
    index += 1
```

### While Loop with Slicing

```python
index = 0
while index < len(greeting):
    print(greeting[index:index+1])
    index += 1
```

---

## Nested Loops

Use when comparing or combining elements in two sequences.

### Domino Example

```python
for left in range(7):
    for right in range(left, 7):
        print(f"[{left}|{right}]", end=" ")
    print()
```

### Team Matchups Example

```python
teams = ['Dragons', 'Wolves', 'Pandas', 'Unicorns']
for home_team in teams:
    for away_team in teams:
        if home_team != away_team:
            print(f"{home_team} vs {away_team}")
```

### Performance Warning

A nested loop of 10,000 x 10,000 = **100 million iterations** (may take hours!). Use carefully.

---

## Looping for `Math`

### Sum & Average

```python
values = [23, 52, 59, 37, 48]
sum = 0
length = 0
for value in values:
    sum += value
    length += 1
print("Total sum:", sum, "- Average:", sum / length)
```

### Product (Factorial)

```python
product = 1
for n in range(1, 10):
    product *= n
print(product)  # Output: 362880
```

---

## List Comprehensions

Concise way to create new lists using loops.

### Example

```python
numbers = [1, 2, 3, 4, 5]
squared = [x ** 2 for x in numbers]
print(squared)  # [1, 4, 9, 16, 25]
```

### Supports:

- Conditions
- Nested loops
- Function calls

---

## Common Pitfalls & Performance Tips

- **Infinite Loops**: Always update loop variables
- **Large Data**: Be cautious with nested loops
- **Missing Initializations**: Always set starting values
- **Loop Complexity**:
  - Single loop over 10,000 items = ~10 seconds (1ms/item)
  - Nested loop over 10,000 items = ~27+ hours!

Use `break`, `continue`, and alternative tools (`map()`, `zip()`, `enumerate()`) for better efficiency.

---
