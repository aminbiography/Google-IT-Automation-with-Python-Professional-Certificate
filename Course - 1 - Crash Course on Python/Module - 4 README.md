# **Python Loops & Recursion**

---

## **1. While Loop**
Use when you want to loop until a condition changes.

```python
number = 1
while number <= 5:
    print(number, end=" ")
    number += 1
```
**Output:**
```
1 2 3 4 5
```

---

## **2. For Loop with Range**
Iterates over a fixed sequence.

```python
for num in range(1, 6):
    print(num, end=" ")
```
**Output:**
```
1 2 3 4 5
```

---

## **3. Range with Step**
Use `range(start, stop, step)`.

```python
for num in range(10, 0, -2):
    print(num, end=" ")
```
**Output:**
```
10 8 6 4 2
```

---

## **4. Nested Loops (Matrix Example)**
Outer loop → rows; inner loop → columns.

```python
for row in range(1, 4):
    for col in range(1, 4):
        print(row * col, end=" ")
    print()
```
**Output:**
```
1 2 3 
2 4 6 
3 6 9
```

---

## **5. Control Statements**
**Break**: exits loop early  
**Continue**: skips current iteration  

```python
for num in range(1, 6):
    if num == 4:
        break
    print(num, end=" ")
```
**Output:**
```
1 2 3
```

```python
for num in range(1, 6):
    if num == 4:
        continue
    print(num, end=" ")
```
**Output:**
```
1 2 3 5
```

---

## **6. Printing on Same Line**
Override newline with `end=" "`.

```python
for num in range(1, 4):
    print(num, end=" ")
```
**Output:**
```
1 2 3
```

---

## **7. Counting Digits**
Repeated division by 10.

```python
n = 144
count = 0
while n > 0:
    n //= 10
    count += 1
print(count)
```
**Output:**
```
3
```

---

## **8. Pattern Printing**
Increasing stars per row.

```python
for row in range(1, 6):
    for star in range(row):
        print("*", end=" ")
    print()
```
**Output:**
```
* 
* * 
* * * 
* * * * 
* * * * *
```

---

## **9. Countdown with While**

```python
x = 3
while x >= 0:
    print(x, end=" ")
    x -= 1
```
**Output:**
```
3 2 1 0
```

---

## **10. Even Numbers up to N**

```python
maximum = 6
result = ""
for num in range(2, maximum+1, 2):
    result += str(num) + " "
print(result.strip())
```
**Output:**
```
2 4 6
```

---

## **11. Recursion Example (Factorial)**

```python
def factorial(n):
    if n < 2:
        return 1
    return n * factorial(n-1)

print(factorial(5))
```
**Output:**
```
120
```

---

## **12. Recursion for Hierarchical Structures**

```python
def count_files(dir_structure):
    if not dir_structure:
        return 0
    total = len(dir_structure.get("files", []))
    for sub in dir_structure.get("subdirs", []):
        total += count_files(sub)
    return total

# Example
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

