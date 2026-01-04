# 🐍 Python Interview Questions & Answers (Experienced Professionals)

---

## 🔹 Core Python (Advanced)

### 1. What are mutable and immutable objects?
**Answer:**
- **Mutable objects** can be changed after creation (e.g., `list`, `dict`, `set`)
- **Immutable objects** cannot be changed (e.g., `int`, `float`, `str`, `tuple`)

👉 Changes to mutable objects inside a function affect the caller, while immutable objects create new instances.

---

### 2. Difference between deep copy and shallow copy
**Answer:**
- **Shallow copy** copies references to nested objects
- **Deep copy** creates independent copies of all nested objects  

👉 Use deep copy when modifying nested structures independently.

---

### 3. Difference between `__new__()` and `__init__()`
**Answer:**
- `__new__()` creates the object
- `__init__()` initializes the object after creation  

👉 `__new__()` is mainly used for immutable objects and design patterns like Singleton.

---

### 4. How does Python manage memory?
**Answer:**
Python uses:
- Reference counting
- Garbage Collection for cyclic references  

Memory is allocated dynamically using private heaps.

---

### 5. What is `__slots__`?
**Answer:**
`__slots__` restricts dynamic attribute creation, reduces memory usage, and improves performance for large numbers of objects.

---

### 6. Explain the LEGB rule
**Answer:**
Variable lookup order:
1. Local  
2. Enclosing  
3. Global  
4. Built-in  

---

### 7. Difference between `a = a + [1]` and `a += [1]`
**Answer:**
- `+` creates a new object
- `+=` modifies the object in place (for mutable types)

---

### 8. What is integer caching and string interning?
**Answer:**
Python caches small integers (`-5` to `256`) and interns some strings to improve performance and memory usage.

---

### 9. What is the GIL?
**Answer:**
The **Global Interpreter Lock (GIL)** allows only one thread to execute Python bytecode at a time.  
It simplifies memory management but limits CPU-bound multithreading.

---

### 10. How do you optimize Python code?
**Answer:**
- Use efficient data structures  
- Reduce loops  
- Use generators  
- Profile before optimizing  
- Offload heavy work to C extensions  

---

## 🔹 Object-Oriented Programming (OOP)

### 11. What is MRO and `super()`?
**Answer:**
- **MRO (Method Resolution Order)** defines how methods are searched in inheritance
- `super()` follows MRO and enables cooperative multiple inheritance

---

### 12. Composition vs Inheritance
**Answer:**
- **Inheritance**: *is-a* relationship  
- **Composition**: *has-a* relationship  

👉 Composition is more flexible and preferred in large systems.

---

### 13. What are Abstract Base Classes (ABCs)?
**Answer:**
ABCs define required methods that subclasses must implement and enforce interface-like behavior.

---

### 14. How do you enforce interfaces in Python?
**Answer:**
- Using Abstract Base Classes  
- Using duck typing  

---

### 15. What problems occur with multiple inheritance?
**Answer:**
The **diamond problem**, resolved using Python’s MRO.

---

### 16. When do you override magic methods?
**Answer:**
- `__eq__`, `__hash__` → dictionary keys  
- `__repr__` → debugging  
- `__str__` → user-friendly output  

---

### 17. What are dataclasses?
**Answer:**
Dataclasses reduce boilerplate code and auto-generate common methods.  
Used mainly for data containers.

---

### 18. Class variables vs instance variables
**Answer:**
- **Class variables** are shared across instances  
- **Instance variables** are unique to each object  

---

### 19. Explain duck typing
**Answer:**
Python focuses on behavior rather than type.  
> “If it behaves like a duck, it is a duck.”

---

### 20. How do you make an object immutable?
**Answer:**
- Avoid setters  
- Use `@dataclass(frozen=True)`  
- Override `__setattr__`  

---

## 🔹 Decorators & Context Managers

### 21. How do decorators work?
**Answer:**
Decorators wrap functions to extend behavior using closures.

---

### 22. What is `functools.wraps`?
**Answer:**
Preserves original function metadata such as name and docstring.

---

### 23. What are context managers?
**Answer:**
Context managers handle setup and cleanup logic using `with`.

---

### 24. How do you create a custom context manager?
**Answer:**
Using:
- `__enter__()` and `__exit__()`  
- `contextlib.contextmanager`  

---

## 🔹 Generators & Iterators

### 25. Generator vs iterator
**Answer:**
Generators are simpler and use `yield`.  
They produce values lazily.

---

### 26. Why are generators memory efficient?
**Answer:**
They generate values on demand instead of storing them.

---

### 27. What is `yield from`?
**Answer:**
Delegates iteration to another generator.

---

### 28. What is lazy evaluation?
**Answer:**
Values are computed only when needed.

---

### 29. Generator vs list comprehension
**Answer:**
- List comprehension is eager  
- Generator expressions are lazy  

---

## 🔹 Concurrency

### 30. Threading vs multiprocessing
**Answer:**
- **Threading** shares memory but is limited by the GIL  
- **Multiprocessing** enables true parallelism  

---

### 31. What is asyncio?
**Answer:**
Asyncio is an event-loop based concurrency framework for I/O-bound tasks.

---

### 32. What are coroutines?
**Answer:**
Functions that can pause and resume execution using `await`.

---

### 33. How do you avoid race conditions?
**Answer:**
Using locks, semaphores, or thread-safe data structures.

---

## 🔹 Exceptions & Debugging

### 34. Difference between `raise` and `raise e`
**Answer:**
- `raise` preserves traceback  
- `raise e` resets traceback  

---

### 35. What is exception chaining?
**Answer:**
Linking exceptions using `raise X from Y`.

---

### 36. How do you profile Python code?
**Answer:**
Using `cProfile`, `line_profiler`, and `tracemalloc`.

---

## 🔹 Data Structures

### 37. Why are dictionaries fast?
**Answer:**
They use hash tables with **O(1)** average lookup time.

---

### 38. What is LRU cache?
**Answer:**
A cache that evicts least recently used items.  
Implemented using `functools.lru_cache`.

---

### 39. Difference between list and deque
**Answer:**
`deque` provides faster append and pop operations from both ends.

---

## 🔹 Python Internals

### 40. How does Python execute code?
**Answer:**
Source code → Bytecode → Python Virtual Machine (PVM)

---

### 41. CPython vs PyPy
**Answer:**
- **CPython** is C-based  
- **PyPy** uses JIT compilation for speed  

---

### 42. What is pickling?
**Answer:**
Serialization of Python objects.  
⚠️ Unsafe with untrusted data.

---

## 🔹 Real-World & Testing

### 43. How do you structure large Python projects?
**Answer:**
Using layered architecture, modular code, and separation of concerns.

---

### 44. How do you write testable code?
**Answer:**
By using dependency injection and mocking.

---

### 45. What is TDD?
**Answer:**
**Test-Driven Development**:
1. Write tests  
2. Write code  
3. Refactor  

---

## 🔹 Tricky Questions

### 46. Difference between `is` and `==`
**Answer:**
- `is` checks identity  
- `==` checks value equality  

---

### 47. Why are default arguments evaluated once?
**Answer:**
They are evaluated at function definition time.

---

### 48. Does Python support private variables?
**Answer:**
Python supports name mangling using double underscores (`__var`).

---

### 49. Difference between `None`, `False`, and `0`
**Answer:**
All are falsy but represent different semantic meanings.

---

### 50. Can Python be used for high-performance systems?
**Answer:**
Yes—using async I/O, multiprocessing, C extensions, and optimized libraries.

---
