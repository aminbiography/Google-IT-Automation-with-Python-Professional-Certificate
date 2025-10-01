# Python Automation: Lists, Tuples, Dictionaries, Sets, Collections and Control Flow

---

## **Strings**

**Description:** Strings are sequences of characters, immutable in Python. They support many methods for text manipulation.
**Example:**

```python
text = "hello world"
print(text.upper())
```

**Output:**

```
HELLO WORLD
```

---

## **Lists**

**Description:** Lists are ordered, mutable collections that can store any data type.
**Example:**

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)
```

**Output:**

```
['apple', 'banana', 'cherry']
```

---

## **Dictionaries**

**Description:** Dictionaries store data as key–value pairs, allowing quick lookups.
**Example:**

```python
pet_dict = {"dogs": ["Collie", "Bulldog"], "cats": ["Persian"]}
print(pet_dict["dogs"])
```

**Output:**

```
['Collie', 'Bulldog']
```

---

## **Tuples**

**Description:** Tuples are ordered, immutable collections, often used for fixed data.
**Example:**

```python
coords = (10, 20)
print(coords[0])
```

**Output:**

```
10
```

---

## **Sets**

**Description:** Sets are unordered collections of unique elements.
**Example:**

```python
nums = {1, 2, 2, 3}
print(nums)
```

**Output:**

```
{1, 2, 3}
```

---

## **List Comprehensions**

**Description:** Provide a shorthand way to create lists from iterables with optional conditions.
**Example:**

```python
z = [x for x in range(0, 11) if x % 2 == 0]
print(z)
```

**Output:**

```
[0, 2, 4, 6, 8, 10]
```

---

## **Zip Function**

**Description:** Combines multiple iterables into tuples element-wise.
**Example:**

```python
names = ["Alice", "Bob"]
ages = [25, 30]
print(list(zip(names, ages)))
```

**Output:**

```
[('Alice', 25), ('Bob', 30)]
```

---

## **Methods**

**Description:** Functions tied to objects. They define object behavior (e.g., `append`, `lower`).
**Example:**

```python
nums = [1, 2]
nums.append(3)
print(nums)
```

**Output:**

```
[1, 2, 3]
```

---

## **Constructors (`__init__`)**

**Description:** Special method to initialize object attributes when creating a class instance.
**Example:**

```python
class Apple:
    def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor

fruit = Apple("red", "sweet")
print(fruit.color)
```

**Output:**

```
red
```

---

## **Special Methods (`__str__`, `__add__`, etc.)**

**Description:** Dunder methods that override operators or default behavior.
**Example:**

```python
class Apple:
    def __init__(self, color, flavor):
        self.color = color
        self.flavor = flavor
    def __str__(self):
        return f"This apple is {self.color} and tastes {self.flavor}"

fruit = Apple("green", "tart")
print(fruit)
```

**Output:**

```
This apple is green and tastes tart
```

---

## **Classes & Methods**

**Description:** Classes bundle attributes (data) and methods (behavior). Methods operate on `self` (the instance).
**Example:**

```python
class Piglet:
    def speak(self):
        return "oink!"

hamlet = Piglet()
print(hamlet.speak())
```

**Output:**

```
oink!
```

---


