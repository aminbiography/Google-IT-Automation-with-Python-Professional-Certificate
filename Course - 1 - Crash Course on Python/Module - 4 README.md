# Python Automation: Lists, Tuples, Dictionaries, Sets, Collections and Control Flow

### 1. **List**

Mutable, ordered collection.

```python
fruits = ["apple", "banana", "cherry"]
print(fruits[1])
```

**Output:**

```
banana
```

---

### 2. **Tuple**

Immutable, ordered collection.

```python
coords = (10, 20)
print(coords[0])
```

**Output:**

```
10
```

---

### 3. **String**

Immutable sequence of characters.

```python
word = "Hello"
print(word.upper())
```

**Output:**

```
HELLO
```

---

### 4. **Dictionary**

Key–value pairs, unordered.

```python
ages = {"Alice": 25, "Bob": 30}
print(ages["Bob"])
```

**Output:**

```
30
```

---

### 5. **Set**

Unordered collection of unique elements.

```python
nums = {1, 2, 2, 3}
print(nums)
```

**Output:**

```
{1, 2, 3}
```

---

### 6. **List Comprehension**

Compact way to build lists.

```python
squares = [x**2 for x in range(5)]
print(squares)
```

**Output:**

```
[0, 1, 4, 9, 16]
```

---

### 7. **For Loop**

Iterates over elements.

```python
for n in [1,2,3]:
    print(n)
```

**Output:**

```
1
2
3
```

---

### 8. **While Loop**

Repeats until condition is False.

```python
x = 3
while x > 0:
    print(x)
    x -= 1
```

**Output:**

```
3
2
1
```

---

### 9. **If–Else Statement**

Decision making.

```python
age = 18
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

**Output:**

```
Adult
```

---

### 10. **Zip**

Combine iterables into tuples.

```python
names = ["A", "B"]
scores = [90, 85]
print(list(zip(names, scores)))
```

**Output:**

```
[('A', 90), ('B', 85)]
```

---


