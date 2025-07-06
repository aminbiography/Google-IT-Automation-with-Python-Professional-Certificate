# Python Key Concepts for Automation Part-02          

---

## Expressions & Variables

- **Expression**: A combination of values and operators that produces a result.  
  _Example_: `2 + 3`

- **Variable**: A named container that stores a value.  
  _Example_: `x = 10`

- **Data Types**:  
  - `int` – Integer  
  - `float` – Decimal number  
  - `str` – String  
  - `bool` – Boolean (`True`/`False`)

- **Keywords** are reserved words in programming languages that have special meanings and specific purposes.  
They **cannot be used** as variable or function names.

  Common Keywords and Their Uses:

  - **`in`** – Checks if a value exists in a sequence.  
  - **`not`** – Negates a condition (logical NOT).  
  - **`or`** – Returns `True` if at least one condition is `True`.  
  - **`for`** – Used to create a loop over a sequence.  
  - **`while`** – Starts a loop that runs while a condition is true.  
  - **`return`** – Exits a function and returns a value.

These keywords help control the **flow and logic** of a program.

- **Variable names** are identifiers used to store data in programming. Choosing effective variable names is essential for writing **readable, understandable, and maintainable** code.
  - Use **letters, digits, and underscores**, but **start with a letter** – not a digit or special character.
  - Avoid **special characters** (like `&`, `%`, `-`).
  - Use **camelCase** or **snake_case** consistently.
  - Make names **descriptive** and meaningful.

---

## Type Conversion

- **Implicit Conversion**:  
  Python automatically converts types.                    
  _Example_: `7 + 2.0 = 9.0`

- **Explicit Conversion**:  
  Use functions to convert types manually:
  ```python
  str(25)   # '25'
  int(3.7)  # 3
  float(5)  # 5.0
  ```

## Type Annotation  
```
name: str = "Alice"
age: int = 25
score_list: list[int] = [90, 85, 78]
```

## Arithmetic Operators

| Operator | Meaning            | Example  | Result |
| -------- | ------------------ | -------- | ------ |
| `+`      | Addition           | `2 + 3`  | `5`    |
| `-`      | Subtraction        | `5 - 2`  | `3`    |
| `*`      | Multiplication     | `2 * 3`  | `6`    |
| `**`     | Exponentiation     | 2 ** 3  | `8`    |
| `**`     | Exponentiation     | number ** 0.5  | `sqrt`|
| `**`     | Exponentiation     | number ** (1/3) | `cube_root`|
| `/`      | Division           | `5 / 2`  | `2.5`  |
| `//`     | Floor Division     | `5 // 2` | `2`    |
| `//`     | Floor Division     | `-5 // 2` | `-3`   |
| `//`     | Floor Division     | `5 // -2` | `-3`   |
| `%`      | Modulo (Remainder) | `5 % 2`   | `1`    |
| `> `     | Greater than       | `5 > 2`   | `True` |
| `< `     | Less than          | `5 < 2`   | `False`|
| `==`     | Equal to          | `5 == 5`   | `True` |
                                   
                                  
                                     


## Common Errors
- TypeError: Adding incompatible types
Fix: Use str() to convert number to string before concatenation.

- ZeroDivisionError: Division by zero
Fix: Validate the denominator before dividing.

## Built-in Functions
| Function   | Purpose                                  |
|------------|------------------------------------------|
| `print()`  | Displays output to the console           |
| `type()`   | Shows the data type of an object         |
| `str()`    | Converts values to string                |
| `sorted()` | Sorts iterables and returns a new list   |
| `max()`    | Finds the highest value in a set or list |
| `min()`    | Finds the lowest value in a set or list  |

### `print()`

**Purpose:** Displays one or more values to the console.         

**Example:**
```python
name = "Python"
print("Welcome to", name)

Output: Welcome to Python
```
### `type()`
**Purpose:** Returns the data type of a given object.

**Example:**
```python
value = 42
print(type(value))

Output: <class 'int'>
```

### `str()`
**Purpose:** Converts a value to a string data type.  
**Example:**
```python
age = 30
print("I am " + str(age) + " years old.")

Output: I am 30 years old.
```

### `sorted()`
**Purpose:** Sorts elements in an iterable and returns a new list.  
**Example:**
```python
numbers = [5, 2, 9, 1]
print(sorted(numbers))

Output: [1, 2, 5, 9]
```

### `max()`
**Purpose:** Returns the largest value from a list or multiple arguments.  
**Example:**
```python
scores = [85, 92, 78]
print(max(scores))

Output: 92
```

### `min()`
**Purpose:** Returns the smallest value from a list or multiple arguments.  
**Example:**
```python
temperatures = [13, 18, 9, 21]
print(min(temperatures))

Output: 9
```

---
## Returning Values in Python

### What are Return Values?
Return values allow a function to send a result back to the part of the code that called it.  
Instead of just printing output, functions can return data for reuse or further processing.

---

### Using `return` in a Function

```python
def area_triangle(base, height):
    return base * height / 2

area_a = area_triangle(5, 4)
area_b = area_triangle(7, 3)
sum = area_a + area_b
print("The sum of both areas is: " + str(sum))
```

**Output:**
```
The sum of both areas is: 20.5
```

---

### Returning Multiple Values

```python
def convert_seconds(seconds):
    hours = seconds // 3600
    minutes = (seconds - hours * 3600) // 60
    remaining_seconds = seconds - hours * 3600 - minutes * 60
    return hours, minutes, remaining_seconds

hours, minutes, seconds = convert_seconds(5000)
print(hours, minutes, seconds)
```

**Output:**
```
1 23 20
```

---

### Functions That Return Nothing

```python
def greeting(name):
    print("Welcome, " + name)

result = greeting("Christine")
print(result)
```

**Output:**
```
Welcome, Christine
None
```

> `None` is a special data type that represents “no value.”

---

## Key Style Principles in Python

- **Self-documenting code**: Use meaningful variable and function names to make the code explain itself.
- **Refactoring**: Improve unclear code by renaming and reorganizing for clarity.
- **Comments**: Use `#` to add helpful notes or explain complex parts. Good comments clarify *why*, not just *what*.
- **Consistency**: Follow a style guide to keep code clean and predictable.
- **Be a good neighbor**: Write code that others can understand and build on.

**Well-styled code = easier to read, fewer errors, and happier developers.**

---

## Functions

- Key Terms
  - **Return value:** Result sent back from a function  
  - **Parameter:** Input passed into a function  
  - **Refactoring:** Improving code readability without changing functionality  

- Skills Practiced
  - Writing functions with multiple parameters  
  - Returning calculated results  
  - Performing conversions and calculations  
  - Combining text with return values in `print()` statements  
  - Converting types with `str()`  

- Example

```python
def greet(name, age):
    return "Hello, " + name + "! You are " + str(age) + " years old."

print(greet("Amein", "8-80"))
Output:
Hello, Amein! You are 8-80 years old.
```

---

## Basic Comparisons and Logical Operators in Python

Basic comparisons:  
```> (greater than), == (equal to), != (not equal), < (less than)```

**Example:**  
`print(10 > 1) -> True`

Type mismatches cause errors:  
Comparing different types like `1 < "1"` raises a `TypeError`

Logical operators:  
`and`, `or`, and `not` combine or reverse logical expressions

- The `and` operator returns True only if all conditions are True.

**Example:**  
`print(25 > 50 and 1 != 2) -> False`

- `or` operator returns True if any one of the conditions is True.

**Example:**  
`print(25 > 50 or 1 != 2) -> True`

- The `not` operator reverses the truth value of an expression.
  
| Expression  | Result  |
| ----------- | ------- |
| `not True`  | `False` |
| `not False` | `True`  |

```print(25 > 50 or 1 != 2)        # True```

```print(not (25 > 50 or 1 != 2))  # False```

### Key Comparison Operators in Python

#### Numeric Comparison Operators

| Operator | Name                      | Example   | Meaning                          |
|----------|---------------------------|-----------|----------------------------------|
| `==`     | Equality                  | `a == b`  | True if `a` equals `b`           |
| `!=`     | Not equal to              | `a != b`  | True if `a` is not equal to `b` |
| `>`      | Greater than              | `a > b`   | True if `a` is larger than `b`  |
| `<`      | Less than                 | `a < b`   | True if `a` is smaller than `b` |
| `>=`     | Greater than or equal to  | `a >= b`  | True if `a` is greater than or equal to `b` |
| `<=`     | Less than or equal to     | `a <= b`  | True if `a` is less than or equal to `b`   |

##### Examples

```python
print(32 == 30 + 2)        # → True
print(5 + 10 == 6 + 7)     # → False
print(4 / 2 < 8 - 4)       # → True
print(12 * 2 >= 24)        # → True
```

---

### String Comparison Operators

| Operator | Description                                        | Example                          |
|----------|----------------------------------------------------|----------------------------------|
| `==`     | Equal to — returns `True` if strings are the same  | `"cat" == "cat"` → `True`        |
| `!=`     | Not equal to — returns `True` if strings differ    | `"dog" != "cat"` → `True`        |
| `>`      | Greater than — based on Unicode (alphabetical)     | `"zebra" > "apple"` → `True`     |
| `<`      | Less than — checks if left comes before right      | `"apple" < "banana"` → `True`    |
| `>=`     | Greater than or equal to                           | `"abc" >= "abc"` → `True`        |
| `<=`     | Less than or equal to                              | `"abc" <= "bcd"` → `True`        |

#### Examples & Concepts

- Comparing identical strings returns `True`:

```python
print("a string" == "a string")  # True
```

- Different data types can't be compared using `<` or `>`:

```python
print("Five" < 6)  # TypeError
```

- Unicode values are used in string comparisons:
  - Uppercase A–Z: Unicode 65–90
  - Lowercase a–z: Unicode 97–122

```python
print("Brown" < "brown")  # True (because 'B' < 'b' in Unicode)
```

---

