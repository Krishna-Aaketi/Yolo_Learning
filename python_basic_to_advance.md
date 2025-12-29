# 🐍 Python Interview Questions & Answers (Basic → Advanced + ML)

---

## 🔹 BASIC LEVEL (Foundation)

### 1️⃣ What is Python?
**Answer:**  
Python is a high-level, interpreted, object-oriented programming language known for its simple syntax and readability.

---

### 2️⃣ Why is Python popular?
**Answer:**
- Easy to learn & read  
- Large standard library  
- Cross-platform  
- Strong community support  
- Used in ML, AI, Web, Automation, Embedded testing  

---

### 3️⃣ Is Python interpreted or compiled?
**Answer:**  
Python is interpreted, but internally it first compiles code into bytecode, then executes it using the Python Virtual Machine (PVM).

---

### 4️⃣ What are Python data types?
**Answer:**
- `int`
- `float`
- `str`
- `bool`
- `list`
- `tuple`
- `set`
- `dict`

---

### 5️⃣ Difference between list and tuple?

| List | Tuple |
|-----|------|
| Mutable | Immutable |
| Slower | Faster |
| Uses more memory | Uses less memory |

---

### 6️⃣ What is a dictionary?
**Answer:**  
A dictionary stores key-value pairs.

```python
data = {"name": "Krishna", "age": 25}
````

---

### 7️⃣ What is indentation in Python?

**Answer:**
Indentation defines block of code. Python does not use `{}` like C/C++.

```python
if x > 0:
    print("Positive")
```

---

### 8️⃣ What are Python keywords?

**Answer:**
Reserved words like `if`, `else`, `for`, `while`, `class`, `def`.

---

### 9️⃣ What is a function?

**Answer:**
A reusable block of code defined using `def`.

```python
def add(a, b):
    return a + b
```

---

## 🔹 INTERMEDIATE LEVEL

### 🔟 What is OOP in Python?

**Answer:**
OOP is a programming style based on objects and classes.

**Four pillars:**

* Encapsulation
* Inheritance
* Polymorphism
* Abstraction

---

### 1️⃣1️⃣ What is a class?

**Answer:**
A class is a blueprint for creating objects.

```python
class Car:
    def drive(self):
        print("Driving")
```

---

### 1️⃣2️⃣ What is `self`?

**Answer:**
`self` refers to the current object of the class.

---

### 1️⃣3️⃣ What is inheritance?

**Answer:**
A child class acquiring properties of a parent class.

```python
class Child(Parent):
    pass
```

---

### 1️⃣4️⃣ What is exception handling?

**Answer:**
Handling runtime errors using `try-except`.

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Error")
```

---

### 1️⃣5️⃣ Difference between `==` and `is`?

**Answer:**

* `==` → value comparison
* `is` → memory location comparison

---

### 1️⃣6️⃣ What are Python modules?

**Answer:**
A module is a file containing Python code.

```python
import math
```

---

### 1️⃣7️⃣ What is `*args` and `**kwargs`?

**Answer:**

* `*args` → variable positional arguments
* `**kwargs` → variable keyword arguments

---

### 1️⃣8️⃣ What is list comprehension?

**Answer:**
Short way to create lists.

```python
squares = [x * x for x in range(5)]
```

---

## 🔹 ADVANCED LEVEL

### 1️⃣9️⃣ What is a generator?

**Answer:**
A function that returns an iterator using `yield`.

```python
def gen():
    yield 1
    yield 2
```

✔ Saves memory

---

### 2️⃣0️⃣ What is the Global Interpreter Lock (GIL)?

**Answer:**
GIL allows only one thread to execute Python bytecode at a time, limiting true multithreading.

---

### 2️⃣1️⃣ Difference between multithreading and multiprocessing?

| Multithreading  | Multiprocessing |
| --------------- | --------------- |
| Shares memory   | Separate memory |
| Affected by GIL | No GIL          |
| Faster for I/O  | Faster for CPU  |

---

### 2️⃣2️⃣ What are decorators?

**Answer:**
Decorators modify a function’s behavior without changing its code.

```python
def my_decorator(func):
    def wrapper():
        print("Before")
        func()
    return wrapper
```

---

### 2️⃣3️⃣ What is a lambda function?

**Answer:**
Anonymous one-line function.

```python
x = lambda a: a * 2
```

---

### 2️⃣4️⃣ What is shallow vs deep copy?

| Shallow Copy            | Deep Copy          |
| ----------------------- | ------------------ |
| Copies reference        | Copies full object |
| Changes affect original | Independent        |

---

### 2️⃣5️⃣ What is memory management in Python?

**Answer:**
Python uses:

* Heap memory
* Reference counting
* Garbage collector

---

### 2️⃣6️⃣ What is pickling?

**Answer:**
Converting Python objects into byte stream for storage or transmission.

---

### 2️⃣7️⃣ What is virtual environment?

**Answer:**
An isolated Python environment for dependencies.

```bash
python -m venv venv
```

---

## 🔹 Python + ML Interview Add-On

### 2️⃣8️⃣ Why Python for Machine Learning?

**Answer:**
* NumPy → fast numerical operations
* Pandas → data handling
* OpenCV → image/video processing
* PyTorch / TensorFlow → deep learning

---

### 2️⃣9️⃣ What is NumPy?
**Answer:**
Library for fast array and matrix operations.

---

### 3️⃣0️⃣ What is Pandas?
**Answer:**
Used for data analysis and preprocessing using DataFrames.

```
