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

## 🔹 What is OOP in Python?

**Answer (Interview-ready):**  
OOP (Object-Oriented Programming) is a programming approach where we organize code using **classes and objects**, so that **data and behavior are bundled together**, making the code **reusable, modular, and easy to maintain**.

In Python, OOP is implemented using **classes, objects, and methods**.

---

## 🔹 Four Pillars of OOP (Very Important)

---

## 1️⃣ Encapsulation

### 👉 What is Encapsulation?
Encapsulation means **wrapping data (variables) and methods together inside a class** and **restricting direct access** to some data.

### 👉 Why is it needed?
- Protects data  
- Prevents accidental modification  
- Improves security  

### 👉 Example:
```python
class Vehicle:
    def __init__(self, speed):
        self.__speed = speed   # private variable

    def get_speed(self):
        return self.__speed
````

🔹 `__speed` cannot be accessed directly from outside the class.

### 👉 Real-world example:

* Vehicle speed is hidden
* Accessed only via methods

---

## 2️⃣ Inheritance

### 👉 What is Inheritance?

Inheritance allows a **child class to use properties and methods of a parent class**.

### 👉 Why is it needed?

* Code reuse
* Avoid duplication
* Easy maintenance

### 👉 Example:

```python
class Vehicle:
    def move(self):
        print("Vehicle moving")

class Car(Vehicle):
    pass
```

### 👉 Usage:

* `Car` automatically gets the `move()` method.

### 👉 Real-world example:

* Vehicle → Car → ElectricCar

---

## 3️⃣ Polymorphism

### 👉 What is Polymorphism?

Polymorphism means **same method name, different behavior**.

### 👉 Why is it needed?

* Flexibility
* Cleaner code
* Easy extension

### 👉 Example:

```python
class Car:
    def fuel(self):
        print("Petrol")

class ElectricCar:
    def fuel(self):
        print("Electric")
```

🔹 Same method `fuel()` behaves differently.

### 👉 Real-world example:

* Different vehicles, same `start()` action

---

## 4️⃣ Abstraction

### 👉 What is Abstraction?

Abstraction means **hiding implementation details** and showing only **essential features**.

### 👉 Why is it needed?

* Reduce complexity
* Focus on *what* an object does, not *how*

### 👉 Example:

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def move(self):
        pass
```

🔹 Child classes must implement `move()`.

---

## 🔹 Simple Summary Table (Interview Favorite)

| Pillar        | Meaning                         | Purpose     |
| ------------- | ------------------------------- | ----------- |
| Encapsulation | Data hiding                     | Security    |
| Inheritance   | Parent → Child                  | Reusability |
| Polymorphism  | Same method, different behavior | Flexibility |
| Abstraction   | Hide implementation             | Simplicity  |

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

---

## 🔹 OBJECT-ORIENTED & ADVANCED PYTHON

### 3️⃣1️⃣ What is `__init__` method?
**Answer:**  
`__init__` is a constructor automatically called when an object is created.  
It is used to initialize variables.

```python
class Car:
    def __init__(self, name):
        self.name = name
````

---

### 3️⃣2️⃣ What is `__str__` and `__repr__`?

**Answer:**

* `__str__` → user-friendly output
* `__repr__` → developer/debug-friendly output

---

### 3️⃣3️⃣ What is method overloading in Python?

**Answer:**
Python does not support traditional method overloading.
We use **default arguments** or `*args`.

---

### 3️⃣4️⃣ What is method overriding?

**Answer:**
A child class provides its own implementation of a parent class method.

---

### 3️⃣5️⃣ What is encapsulation?

**Answer:**
Wrapping data and methods together and restricting direct access using `_` or `__`.

---

### 3️⃣6️⃣ What is abstraction?

**Answer:**
Hiding internal implementation details and showing only essential features.

---

### 3️⃣7️⃣ What are abstract base classes?

**Answer:**
Classes that contain abstract methods using the `abc` module.

---

### 3️⃣8️⃣ What is duck typing?

**Answer:**
Python focuses on object behavior, not type.
“If it walks like a duck, it’s a duck.”

---

### 3️⃣9️⃣ What is `with` statement?

**Answer:**
Used for resource management (file, lock).

```python
with open("file.txt") as f:
    data = f.read()
```

---

### 4️⃣0️⃣ What is a context manager?

**Answer:**
An object that manages resources using `__enter__` and `__exit__`.

---

## 🔹 PYTHON PERFORMANCE & MEMORY

### 4️⃣1️⃣ Why Python is slower than C++?

**Answer:**

* Interpreted language
* Dynamic typing
* GIL
* Extra memory overhead

---

### 4️⃣2️⃣ How to optimize Python code?

**Answer:**

* Use NumPy vectorization
* Avoid loops
* Use generators
* Use multiprocessing
* Profile code

---

### 4️⃣3️⃣ What is `cProfile`?

**Answer:**
Used to analyze function execution time.

---

### 4️⃣4️⃣ What is garbage collection?

**Answer:**
Automatic removal of unused objects using reference counting and cyclic GC.

---

### 4️⃣5️⃣ What is reference counting?

**Answer:**
Each object keeps count of references.
When count becomes zero → object deleted.

---

## 🔹 MULTITHREADING / MULTIPROCESSING

### 4️⃣6️⃣ What is a race condition?

**Answer:**
When multiple threads access shared data and the result depends on execution order.

---

### 4️⃣7️⃣ How to avoid race conditions?

**Answer:**

* Locks
* Semaphores
* Queues

---

### 4️⃣8️⃣ What is a deadlock?

**Answer:**
Two threads wait forever for each other to release resources.

---

### 4️⃣9️⃣ When to use multithreading?

**Answer:**
For I/O-bound tasks (file, network, camera input).

---

### 5️⃣0️⃣ When to use multiprocessing?

**Answer:**
For CPU-bound tasks (ML inference, heavy computation).

---

## 🔹 PYTHON + ML INTERVIEW QUESTIONS (VERY IMPORTANT)

### 5️⃣1️⃣ Explain ML pipeline in Python

**Answer:**
Data collection → preprocessing → model training → evaluation → deployment

---

### 5️⃣2️⃣ What is data preprocessing?

**Answer:**

* Handling missing values
* Normalization
* Encoding categorical data
* Noise removal

---

### 5️⃣3️⃣ Why NumPy is faster than lists?

**Answer:**

* Uses contiguous memory
* Written in C
* Vectorized operations

---

### 5️⃣4️⃣ What is Pandas DataFrame?

**Answer:**
2D labeled data structure similar to an Excel table.

---

### 5️⃣5️⃣ Difference between `.loc` and `.iloc`?

**Answer:**

* `.loc` → label-based
* `.iloc` → index-based

---

### 5️⃣6️⃣ What is batch processing in ML?

**Answer:**
Processing data in chunks to reduce memory usage and improve speed.

---

### 5️⃣7️⃣ What is overfitting?

**Answer:**
Model performs well on training data but poorly on unseen data.

---

### 5️⃣8️⃣ How do you improve ML performance?

**Answer:**

* More data
* Better features
* Hyperparameter tuning
* Regularization

---

### 5️⃣9️⃣ How Python is used in real-time ML systems?

**Answer:**

* Frame preprocessing
* Model inference
* Post-processing
* Automation & orchestration

---

### 6️⃣0️⃣ How do you explain Python role in your project?

**Best Answer:**
“Python is used for ML model integration, video processing, tracking, OCR, performance optimization, and automation. Critical latency-sensitive parts are optimized using GPU and native libraries.”

```
