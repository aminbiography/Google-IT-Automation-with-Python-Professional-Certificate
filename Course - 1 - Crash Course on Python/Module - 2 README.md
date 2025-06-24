# Python Key Concepts for Automation 02

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

---

## Type Conversion

- **Implicit Conversion**:  
  Python automatically converts types.  
  _Example_: `7 + 2.0 → 9.0`

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

## Built-in Functions
- print() – Displays output.
- type() – Returns the data type of an object.
- str() – Converts data to a string.
- sorted() – Sorts an iterable (returns a new list).
- max() / min() – Return the highest or lowest value.

```
print(type("Hello"))              # <class 'str'>
print(sorted([5, 2, 9]))          # [2, 5, 9]
print(max([1, 4, 7]))             # 7
```

## Arithmetic Operators

| Operator | Meaning            | Example  | Result |
| -------- | ------------------ | -------- | ------ |
| `+`      | Addition           | `2 + 3`  | `5`    |
| `-`      | Subtraction        | `5 - 2`  | `3`    |
| `*`      | Multiplication     | `2 * 3`  | `6`    |
| `/`      | Division           | `5 / 2`  | `2.5`  |
| `//`     | Floor Division     | `5 // 2` | `2`    |
| `%`      | Modulo (Remainder) | `5 % 2`  | `1`    |


## Common Errors
- TypeError: Adding incompatible types
Fix: Use str() to convert number to string before concatenation.

- ZeroDivisionError: Division by zero
Fix: Validate the denominator before dividing.

  
