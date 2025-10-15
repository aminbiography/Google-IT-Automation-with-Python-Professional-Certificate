# **Crash Course on Python For IT Automation**

---

### **1. Python Foundations and Problem Solving**

Python is a versatile, high-level programming language used to automate tasks and solve IT-related problems efficiently.
The structured approach to problem-solving includes:

1. **Define the problem** – Understand the goal clearly.
2. **Research** – Identify relevant Python tools and libraries.
3. **Plan** – Decide the logic, data types, and functions to use.
4. **Write** – Implement the solution step by step.
5. **Test** – Verify that the script performs as expected.

**Example:**

```python
def greet(name):
    return f"Hello, {name}!"
print(greet("Alex"))
```

**Output:**

```
Hello, Alex!
```

---

### **2. Automation Scenario: User Login Report**

**Objective:** Generate a report showing which users are logged into which machines.

**Input:** A list of event objects with attributes – `date`, `user`, `machine`, and `type` (login/logout).
**Process:**

* Sort events by date using `.sort()` with a key function.
* Track users with a dictionary of sets (`{machine: {users}}`).
* Update sets according to login/logout actions.

**Output:** A readable report showing machines and their active users.

**Example:**

```python
machines = {'server1': {'alex', 'jordan'}, 'server2': {'chris'}}
for m, u in machines.items():
    print(f"{m}: {', '.join(u)}")
```

**Output:**

```
server1: alex, jordan
server2: chris
```

---

### **3. Research, Planning, and Writing**

* The **`sort()`** method modifies the original list, while **`sorted()`** returns a new sorted list.
* The **`key`** parameter specifies a function to determine sorting criteria.
* For login tracking, dictionaries and sets provide efficient data storage and lookup.

**Example:**

```python
numbers = [4, 6, 2, 7, 1]
numbers.sort()
print(numbers)
```

**Output:**

```
[1, 2, 4, 6, 7]
```

---

### **4. Real-World Automation Example**

Python can automate system-level tasks such as creating user accounts:

* **`csv`** handles input/output files.
* **`secrets`** generates random passwords.
* **`subprocess`** executes shell commands.

**Example:**

```python
import secrets
password = secrets.token_hex(8)
print(password)
```

**Output:**

```
e3f29acb19f74e91
```

This process demonstrates how repetitive administrative tasks can be automated effectively.

---

### **5. Career Planning: Finding a Path**

IT professionals may follow one of two broad directions:

* **Generalist:** Works across multiple areas (e.g., IT Support, IT Manager).
* **Specialist:** Focuses deeply on one domain (e.g., Python Developer, Cloud Engineer).

**Work Environments:**

* **Agency:** Provides IT services to multiple clients on contracts.
* **In-house:** Works within a single organization’s IT department.
* **Large Company:** Offers structured growth and benefits.
* **Small Company:** Offers flexibility and close collaboration.

---

### **6. Terms and Definitions**

#### **A**

* **Automation:** The process of replacing a manual step with one that happens automatically.

#### **B**

* **Break:** A way to exit out of a loop before the loop’s condition is false.
* **Built-in functions:** Functions that exist within Python and can be called directly.

#### **C**

* **Client-side scripting language:** Used in web programming; scripts are transferred from a web server to a user’s browser and executed there.
* **Code editors:** Tools that provide syntax highlighting, indentation, error checking, and autocompletion.
* **Comments:** Notes for programmers to clarify code purpose.
* **Computer program:** A sequence of instructions executed by a computer to reach a goal.
* **Control statements:** Direct the flow of program execution by making decisions or repeating actions.

#### **D**

* **Data types:** Categories of data (e.g., `string`, `int`, `float`, `bool`) defining properties and behaviors.
* **Dictionaries:** Collections that store data in key–value pairs.

**Example:**

```python
info = {"name": "Alex", "age": 25}
print(info["name"])
```

**Output:**

```
Alex
```

#### **E**

* **Explicit conversion:** Manual conversion between data types.
* **Expression:** A combination of values and operators that produces a result.

#### **F**

* **For loop:** Executes a block of code a fixed number of times or over a collection.
* **Functions:** Reusable blocks of code performing specific tasks.

**Example:**

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

#### **I**

* **IDE:** An integrated environment providing tools for software development.
* **Implicit conversion:** Automatic type conversion by Python.
* **Infinite loop:** A loop without an exit condition.
* **Interpreter:** The program that executes Python code.
* **Input:** Data entered by the user.
* **Iterators:** Objects used to traverse through collections.

#### **L**

* **List comprehensions:** Create new lists using concise syntax.
* **Logic errors:** Errors that prevent correct program operation.
* **Logical operators:** Combine or modify boolean values (`and`, `or`, `not`).
* **Loop:** Repeats code until a condition changes.

#### **M**

* **Machine language:** The binary-level language directly understood by computers.

#### **O**

* **Object-oriented programming:** Treats code elements as objects with properties and methods.
* **Output:** The result produced by a function or program.

#### **P**

* **Parameter (argument):** A value passed into a function.
* **Pass:** A placeholder statement used when no action is required.
* **Platform-specific scripting language:** Used for administration on specific systems.
* **Programming:** Writing code to make computers perform tasks.
* **Programming code:** Instructions written following a programming language’s syntax.
* **Programming languages:** Formal languages for developing software.
* **Python:** A general-purpose, high-level programming language.
* **Python interpreter:** Executes Python scripts by translating them into machine instructions.

#### **R**

* **Recursion:** Repeatedly applying a procedure to smaller instances of the same problem.
* **Refactoring:** Updating code to improve readability and structure.
* **Return value:** The output provided by a function after execution.

#### **S**

* **Script:** Automates a series of predefined tasks.
* **Semantics:** The meaning of code or statements.
* **String:** A sequence of characters enclosed in quotes.
* **Syntax:** Rules defining correct code structure.

**Example:**

```python
text = "Automation"
print(text.upper())
```

**Output:**

```
AUTOMATION
```

#### **T**

* **Tuples:** Immutable sequences written with parentheses.
  **Example:**

```python
t = (1, 2, 3)
print(t[1])
```

**Output:**

```
2
```

#### **V**

* **Variables:** Containers for storing changeable values.

#### **W**

* **While loop:** Repeats code while a condition is true.

**Example:**

```python
count = 0
while count < 3:
    print(count)
    count += 1
```

**Output:**

```
0
1
2
```
