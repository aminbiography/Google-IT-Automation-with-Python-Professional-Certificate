# Python Key Concepts for Automation: While Loops

A **while loop** allows to repeatedly execute a block of code **as long as a specified condition remains true**. It's especially useful when the number of repetitions is **not known ahead of time**, making it ideal for automation tasks.

---

## Core Components

- **Initialization**: Set a starting value.  
  _Example_: `x = 0`

- **Condition**: The loop continues running **while** the condition evaluates to `True`.  
  _Example_: `while x < 5:`

- **Loop Body**: The block of code that gets repeated.  
  It must be **indented** under the `while` statement.

- **Update**: Modify the loop variable inside the loop to eventually make the condition false.  
  _Example_: `x += 1`

---

## How a While Loop Works

1. Evaluate the condition.
2. If the condition is `True`, execute the loop body.
3. Update any necessary variables.
4. Repeat the process until the condition becomes `False`.

Once the condition is no longer true, the loop exits and the program continues with the next statement after the loop.

---

## Example

```python
x = 0
while x < 5:
    print("Not there yet, x=" + str(x))
    x += 1
print("x=" + str(x))
```
Output:
```
Not there yet, x=0  
Not there yet, x=1  
Not there yet, x=2  
Not there yet, x=3  
Not there yet, x=4  
x=5
```
In this example, the message is printed 5 times as x increments from 0 to 4.

## Real-World Use Cases
Retrying failed operations (e.g., login attempts)

Validating user input until it's acceptable

Monitoring or background task loops (e.g., checking for updates or alerts)

## Common Pitfall: Infinite Loops
If don’t update the loop variable or the condition never becomes false, the loop will continue forever.

Example of an infinite loop:
```
x = 0
while x < 5:
    print("Stuck here forever...")
    # missing x += 1
```
Always make sure your loop has a clear exit condition.

---

## Common Errors in Loops

- **Uninitialized Variables:**  
  Always initialize variables used in the loop’s condition.

- **Infinite Loops:**  
  Ensure variables in the condition are modified inside the loop to avoid infinite loops.

- **Prevention Tips:**  
  Use the `break` statement or refine loop conditions to ensure eventual termination.

---

## Terms

- **While loop:**  
  Repeats a block while a condition is true.

- **Infinite loop:**  
  A loop with no end condition or a condition that never becomes false.

- **Break:**  
  Stops loop execution immediately.

- **Pass:**  
  Placeholder; does nothing but is syntactically required.

---

## Math Concepts on the Practice Quiz

- **Prime Numbers:**  
  Numbers with only two factors—1 and itself (e.g., 2, 3, 5...).

- **Prime Factors:**  
  Prime numbers that divide a given number (e.g., 2 and 5 for 10).

- **Divisor:**  
  A number that divides another without a remainder.

- **Sum of Divisors:**  
  Add all divisors of a number.

- **Multiplication Table:**  
  A list of products formed by multiplying a number with others sequentially (e.g., 4×1, 4×2...).

## Coding Skills – Skill Group 1

**Skills Covered:**

- Initialize variables.
- Use a while loop with a valid condition.
- Avoid infinite loops.
- Increment variables inside loops.

**Example:**  
Function `count_factors()` counts the number of integer factors of a given number using a loop and modulo operation.

---

## Coding Skills – Skill Group 2

**Skills Covered:**

- Assign correct data types to variables before using in loops.
- Use `break` to exit loops early.

**Example:**  
Function `addition_table()` prints an addition table and exits early if the sum exceeds 20.

