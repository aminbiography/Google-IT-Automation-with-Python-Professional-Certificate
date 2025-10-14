# **Crash Course on Python For IT Automation**

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

Objective: Generate a report showing which users are logged into which machines.

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


