# Python Programming Guide: Basic to Advanced

## Table of Contents

1. [Getting Started with Python](#getting-started-with-python)
2. [Basic Syntax and Data Types](#basic-syntax-and-data-types)
3. [Control Structures](#control-structures)
4. [Functions and Modules](#functions-and-modules)
5. [Object-Oriented Programming](#object-oriented-programming)
6. [File Handling and I/O](#file-handling-and-io)
7. [Error Handling](#error-handling)
8. [Advanced Data Structures](#advanced-data-structures)
9. [Decorators and Context Managers](#decorators-and-context-managers)
10. [Concurrency and Async Programming](#concurrency-and-async-programming)
11. [Best Practices and Design Patterns](#best-practices-and-design-patterns)

---

## Getting Started with Python

### What is Python?

Python is a high-level, interpreted programming language known for its simplicity and readability. Created by Guido van Rossum in 1991, Python emphasizes code readability and allows programmers to express concepts in fewer lines of code.

### Key Features
- **Easy to learn and use**: Simple, readable syntax
- **Interpreted**: No compilation step needed
- **Cross-platform**: Runs on Windows, macOS, Linux
- **Large standard library**: "Batteries included" philosophy
- **Dynamic typing**: Variables don't need explicit type declarations
- **Object-oriented**: Supports OOP principles
- **Open source**: Free to use and distribute

### Installation

1. Download Python from [python.org](https://python.org)
2. Install with default settings
3. Verify installation:

```bash
python --version
pip --version
```

### Your First Python Program

```python
# Hello World program
print("Hello, World!")

# Interactive input
name = input("Enter your name: ")
print(f"Hello, {name}!")

# Basic calculations
a = 10
b = 20
sum_result = a + b
print(f"The sum of {a} and {b} is {sum_result}")
```

---

## Basic Syntax and Data Types

### Python Syntax Rules

- **Indentation matters**: Python uses indentation to define code blocks
- **Case sensitive**: `Variable` and `variable` are different
- **No semicolons needed**: Line breaks indicate statement endings
- **Comments**: Use `#` for single-line, `"""` or `'''` for multi-line

```python
# This is a comment
"""
This is a
multi-line comment
"""
```

### Variables and Assignment

```python
# Variable assignment
name = "John"
age = 25
height = 5.9
is_student = True

# Multiple assignment
x, y, z = 1, 2, 3
a = b = c = 0

# Swapping variables
x, y = y, x
```

### Data Types

#### Numbers

```python
# Integers
integer_num = 42
negative_num = -17

# Floats
float_num = 3.14
scientific = 2.5e-3  # 0.0025

# Complex numbers
complex_num = 3 + 4j

# Type conversion
int_from_float = int(3.14)    # 3
float_from_int = float(42)    # 42.0
str_from_int = str(123)       # "123"
```

#### Strings

```python
# String creation
single_quote = 'Hello'
double_quote = "World"
multiline = """This is a
multiline string"""

# String formatting
name = "Alice"
age = 30

# f-strings (Python 3.6+)
message = f"My name is {name} and I'm {age} years old"

# .format() method
message = "My name is {} and I'm {} years old".format(name, age)
message = "My name is {name} and I'm {age} years old".format(name=name, age=age)

# % formatting (older method)
message = "My name is %s and I'm %d years old" % (name, age)

# String methods
text = "  Hello World  "
print(text.strip())          # "Hello World"
print(text.lower())          # "  hello world  "
print(text.upper())          # "  HELLO WORLD  "
print(text.replace("Hello", "Hi"))  # "  Hi World  "
print(text.split())          # ["Hello", "World"]
```

#### Collections

```python
# Lists (ordered, mutable)
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# List operations
fruits.append("grape")           # Add item
fruits.insert(1, "mango")        # Insert at index
fruits.remove("banana")          # Remove item
popped = fruits.pop()            # Remove and return last item
fruits.sort()                    # Sort in place
fruits.reverse()                 # Reverse in place

# List slicing
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(numbers[2:5])    # [2, 3, 4]
print(numbers[:3])     # [0, 1, 2]
print(numbers[7:])     # [7, 8, 9]
print(numbers[::2])    # [0, 2, 4, 6, 8] (every 2nd element)
print(numbers[::-1])   # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0] (reverse)

# Tuples (ordered, immutable)
coordinates = (10, 20)
rgb = (255, 128, 0)
single_item_tuple = (42,)  # Note the comma

# Tuple unpacking
x, y = coordinates
r, g, b = rgb

# Dictionaries (unordered, mutable, key-value pairs)
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# Dictionary operations
person["email"] = "alice@example.com"  # Add new key-value pair
person["age"] = 31                     # Update existing value
del person["city"]                     # Remove key-value pair
age = person.get("age", 0)            # Get value with default

# Dictionary methods
keys = person.keys()
values = person.values()
items = person.items()

# Sets (unordered, mutable, unique elements)
unique_numbers = {1, 2, 3, 4, 5}
letters = set("hello")  # {'h', 'e', 'l', 'o'}

# Set operations
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}
union = set1 | set2        # {1, 2, 3, 4, 5, 6}
intersection = set1 & set2  # {3, 4}
difference = set1 - set2    # {1, 2}
```

---

## Control Structures

### Conditional Statements

```python
# Basic if-elif-else
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Your grade is: {grade}")

# Ternary operator (conditional expression)
age = 20
status = "adult" if age >= 18 else "minor"

# Multiple conditions
temperature = 25
humidity = 60

if temperature > 30 and humidity > 80:
    print("Hot and humid")
elif temperature > 30 or humidity > 80:
    print("Either hot or humid")
else:
    print("Pleasant weather")

# Checking membership
fruits = ["apple", "banana", "orange"]
if "apple" in fruits:
    print("Apple is in the list")

# Checking for None
value = None
if value is None:
    print("Value is None")
if value is not None:
    print("Value is not None")
```

### Loops

```python
# For loops
# Range function
for i in range(5):        # 0, 1, 2, 3, 4
    print(i)

for i in range(1, 6):     # 1, 2, 3, 4, 5
    print(i)

for i in range(0, 10, 2): # 0, 2, 4, 6, 8
    print(i)

# Iterating over collections
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)

# Enumerate for index and value
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")

# Iterating over dictionaries
person = {"name": "Alice", "age": 30, "city": "NYC"}

for key in person:
    print(key, person[key])

for key, value in person.items():
    print(f"{key}: {value}")

# While loops
count = 0
while count < 5:
    print(count)
    count += 1

# Loop control statements
for i in range(10):
    if i == 3:
        continue  # Skip this iteration
    if i == 7:
        break     # Exit the loop
    print(i)

# Else clause with loops (executes if loop completes without break)
for i in range(5):
    print(i)
else:
    print("Loop completed successfully")
```

### List Comprehensions

```python
# Basic list comprehension
squares = [x**2 for x in range(10)]
# Equivalent to:
# squares = []
# for x in range(10):
#     squares.append(x**2)

# List comprehension with condition
even_squares = [x**2 for x in range(10) if x % 2 == 0]

# Nested list comprehension
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened = [num for row in matrix for num in row]
# Result: [1, 2, 3, 4, 5, 6, 7, 8, 9]

# Dictionary comprehension
square_dict = {x: x**2 for x in range(5)}
# Result: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Set comprehension
unique_lengths = {len(word) for word in ["hello", "world", "python"]}
# Result: {5, 6}

# Generator expression (memory efficient)
squares_gen = (x**2 for x in range(10))
```

---

## Functions and Modules

### Defining Functions

```python
# Basic function
def greet(name):
    """Return a greeting message."""
    return f"Hello, {name}!"

# Function with default parameters
def power(base, exponent=2):
    """Calculate base raised to exponent power."""
    return base ** exponent

# Function with multiple return values
def get_name_age():
    name = "Alice"
    age = 30
    return name, age  # Returns a tuple

name, age = get_name_age()  # Tuple unpacking

# Function with variable arguments (*args)
def sum_all(*args):
    """Sum all provided arguments."""
    total = 0
    for num in args:
        total += num
    return total

# Function with keyword arguments (**kwargs)
def create_profile(**kwargs):
    """Create a user profile from keyword arguments."""
    profile = {}
    for key, value in kwargs.items():
        profile[key] = value
    return profile

# Function with mixed parameters
def complex_function(required_param, default_param="default", *args, **kwargs):
    print(f"Required: {required_param}")
    print(f"Default: {default_param}")
    print(f"Args: {args}")
    print(f"Kwargs: {kwargs}")

# Usage examples
print(greet("Alice"))
print(power(3))           # Uses default exponent=2, returns 9
print(power(3, 3))        # Returns 27
print(sum_all(1, 2, 3, 4, 5))

profile = create_profile(name="John", age=25, city="NYC")
complex_function("hello", "world", 1, 2, 3, extra="info")
```

### Lambda Functions

```python
# Basic lambda
square = lambda x: x**2
print(square(5))  # 25

# Lambda with multiple arguments
add = lambda x, y: x + y
print(add(3, 4))  # 7

# Using lambda with built-in functions
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Filter even numbers
evens = list(filter(lambda x: x % 2 == 0, numbers))

# Square all numbers
squares = list(map(lambda x: x**2, numbers))

# Sort by custom criteria
students = [("Alice", 85), ("Bob", 90), ("Charlie", 78)]
students.sort(key=lambda student: student[1])  # Sort by grade
```

### Modules and Packages

```python
# Importing modules
import math
import random
from datetime import datetime, timedelta
from collections import Counter, defaultdict
import os

# Using imported modules
print(math.pi)
print(math.sqrt(16))
print(random.randint(1, 10))
print(datetime.now())

# Creating your own module (save as mymodule.py)
# mymodule.py content:
def my_function():
    print("Hello from my module!")

PI = 3.14159

class MyClass:
    def __init__(self, value):
        self.value = value

# Importing your own module
# import mymodule
# mymodule.my_function()
# print(mymodule.PI)

# Module aliasing
import numpy as np
import pandas as pd

# Conditional imports
try:
    import requests
    HAS_REQUESTS = True
except ImportError:
    HAS_REQUESTS = False
    print("requests library not available")
```

### Scope and Closures

```python
# Global vs Local scope
global_var = "I'm global"

def test_scope():
    local_var = "I'm local"
    print(global_var)  # Can access global
    print(local_var)   # Can access local

def modify_global():
    global global_var
    global_var = "Modified global"

# Closures
def outer_function(x):
    def inner_function(y):
        return x + y
    return inner_function

add_5 = outer_function(5)
print(add_5(3))  # Returns 8

# Decorator example using closures
def timer_decorator(func):
    import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

@timer_decorator
def slow_function():
    import time
    time.sleep(1)
    return "Done"
```

---

## Object-Oriented Programming

### Classes and Objects

```python
# Basic class definition
class Person:
    # Class variable (shared by all instances)
    species = "Homo sapiens"
    
    def __init__(self, name, age):
        # Instance variables
        self.name = name
        self.age = age
    
    def greet(self):
        return f"Hello, I'm {self.name} and I'm {self.age} years old"
    
    def have_birthday(self):
        self.age += 1
        print(f"Happy birthday! {self.name} is now {self.age}")

# Creating objects
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

print(person1.greet())
person1.have_birthday()
```

### Inheritance

```python
# Base class
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species
    
    def make_sound(self):
        pass
    
    def info(self):
        return f"{self.name} is a {self.species}"

# Derived class
class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name, "Canine")
        self.breed = breed
    
    def make_sound(self):
        return "Woof!"
    
    def fetch(self):
        return f"{self.name} is fetching the ball"

class Cat(Animal):
    def __init__(self, name, breed):
        super().__init__(name, "Feline")
        self.breed = breed
    
    def make_sound(self):
        return "Meow!"
    
    def climb(self):
        return f"{self.name} is climbing a tree"

# Using inheritance
dog = Dog("Rex", "German Shepherd")
cat = Cat("Whiskers", "Persian")

print(dog.info())        # Inherited method
print(dog.make_sound())  # Overridden method
print(dog.fetch())       # Dog-specific method

# Multiple inheritance
class Flyable:
    def fly(self):
        return "Flying high!"

class Bird(Animal, Flyable):
    def __init__(self, name, wingspan):
        super().__init__(name, "Avian")
        self.wingspan = wingspan
    
    def make_sound(self):
        return "Tweet!"

parrot = Bird("Polly", "12 inches")
print(parrot.fly())      # From Flyable mixin
print(parrot.info())     # From Animal
```

### Special Methods (Magic Methods)

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def __str__(self):
        """String representation for users"""
        return f"Vector({self.x}, {self.y})"
    
    def __repr__(self):
        """String representation for developers"""
        return f"Vector(x={self.x}, y={self.y})"
    
    def __add__(self, other):
        """Addition operator"""
        return Vector(self.x + other.x, self.y + other.y)
    
    def __mul__(self, scalar):
        """Multiplication by scalar"""
        return Vector(self.x * scalar, self.y * scalar)
    
    def __len__(self):
        """Length/magnitude of vector"""
        return (self.x**2 + self.y**2)**0.5
    
    def __eq__(self, other):
        """Equality comparison"""
        return self.x == other.x and self.y == other.y
    
    def __getitem__(self, index):
        """Index access"""
        if index == 0:
            return self.x
        elif index == 1:
            return self.y
        else:
            raise IndexError("Vector index out of range")

# Usage
v1 = Vector(2, 3)
v2 = Vector(1, 4)

print(v1)              # Calls __str__
print(repr(v1))        # Calls __repr__
print(v1 + v2)         # Calls __add__
print(v1 * 3)          # Calls __mul__
print(len(v1))         # Calls __len__
print(v1 == v2)        # Calls __eq__
print(v1[0])           # Calls __getitem__
```

### Properties and Class Methods

```python
class Circle:
    def __init__(self, radius):
        self._radius = radius
    
    @property
    def radius(self):
        """Get the radius"""
        return self._radius
    
    @radius.setter
    def radius(self, value):
        """Set the radius with validation"""
        if value <= 0:
            raise ValueError("Radius must be positive")
        self._radius = value
    
    @property
    def area(self):
        """Calculate area (read-only property)"""
        return 3.14159 * self._radius ** 2
    
    @property
    def circumference(self):
        """Calculate circumference (read-only property)"""
        return 2 * 3.14159 * self._radius
    
    @classmethod
    def from_diameter(cls, diameter):
        """Alternative constructor"""
        return cls(diameter / 2)
    
    @staticmethod
    def pi():
        """Static method - doesn't need instance or class"""
        return 3.14159

# Usage
circle = Circle(5)
print(circle.radius)        # 5
print(circle.area)          # 78.54
circle.radius = 10          # Uses setter
print(circle.area)          # 314.159

# Alternative constructor
circle2 = Circle.from_diameter(20)
print(circle2.radius)       # 10

# Static method
print(Circle.pi())          # 3.14159
```

---

## File Handling and I/O

### Reading and Writing Files

```python
# Writing to a file
with open("example.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a test file.\n")
    
    # Writing multiple lines
    lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
    file.writelines(lines)

# Reading from a file
with open("example.txt", "r") as file:
    content = file.read()  # Read entire file
    print(content)

# Reading line by line
with open("example.txt", "r") as file:
    for line_number, line in enumerate(file, 1):
        print(f"Line {line_number}: {line.strip()}")

# Reading all lines into a list
with open("example.txt", "r") as file:
    lines = file.readlines()
    
# Appending to a file
with open("example.txt", "a") as file:
    file.write("This line is appended.\n")

# Different file modes
# 'r' - read (default)
# 'w' - write (overwrites existing file)
# 'a' - append
# 'x' - exclusive creation (fails if file exists)
# 'b' - binary mode (e.g., 'rb', 'wb')
# 't' - text mode (default)
# '+' - read and write
```

### Working with CSV Files

```python
import csv

# Writing CSV
data = [
    ['Name', 'Age', 'City'],
    ['Alice', 30, 'New York'],
    ['Bob', 25, 'San Francisco'],
    ['Charlie', 35, 'Chicago']
]

with open('people.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerows(data)

# Reading CSV
with open('people.csv', 'r') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)

# Using DictReader for named columns
with open('people.csv', 'r') as csvfile:
    reader = csv.DictReader(csvfile)
    for row in reader:
        print(f"Name: {row['Name']}, Age: {row['Age']}")

# Writing with DictWriter
fieldnames = ['Name', 'Age', 'City']
with open('people_dict.csv', 'w', newline='') as csvfile:
    writer = csv.DictWriter(csvfile, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerow({'Name': 'David', 'Age': 28, 'City': 'Boston'})
```

### Working with JSON

```python
import json

# Python object to JSON
data = {
    'name': 'Alice',
    'age': 30,
    'hobbies': ['reading', 'swimming', 'coding'],
    'address': {
        'street': '123 Main St',
        'city': 'New York'
    }
}

# Convert to JSON string
json_string = json.dumps(data, indent=2)
print(json_string)

# Write JSON to file
with open('data.json', 'w') as json_file:
    json.dump(data, json_file, indent=2)

# Read JSON from file
with open('data.json', 'r') as json_file:
    loaded_data = json.load(json_file)
    print(loaded_data['name'])

# Parse JSON string
json_string = '{"name": "Bob", "age": 25}'
parsed_data = json.loads(json_string)
print(parsed_data['name'])
```

### Working with Binary Files

```python
# Reading binary file
with open('image.jpg', 'rb') as binary_file:
    binary_data = binary_file.read()
    print(f"File size: {len(binary_data)} bytes")

# Writing binary file (copying a file)
with open('source.jpg', 'rb') as source:
    with open('destination.jpg', 'wb') as dest:
        dest.write(source.read())

# Working with pickle (Python object serialization)
import pickle

# Serialize Python object
data = {'numbers': [1, 2, 3, 4, 5], 'string': 'hello'}
with open('data.pickle', 'wb') as pickle_file:
    pickle.dump(data, pickle_file)

# Deserialize Python object
with open('data.pickle', 'rb') as pickle_file:
    loaded_data = pickle.load(pickle_file)
    print(loaded_data)
```

---

## Error Handling

### Try-Except Blocks

```python
# Basic exception handling
try:
    number = int(input("Enter a number: "))
    result = 10 / number
    print(f"Result: {result}")
except ValueError:
    print("Invalid input! Please enter a valid number.")
except ZeroDivisionError:
    print("Cannot divide by zero!")

# Multiple exceptions in one except block
try:
    # Some risky operation
    pass
except (ValueError, TypeError, ZeroDivisionError) as e:
    print(f"An error occurred: {e}")

# Catching all exceptions (use sparingly)
try:
    # Some operation
    pass
except Exception as e:
    print(f"Unexpected error: {e}")

# Using else and finally
try:
    file = open("data.txt", "r")
    data = file.read()
except FileNotFoundError:
    print("File not found!")
except PermissionError:
    print("Permission denied!")
else:
    # Executed if no exception occurs
    print("File read successfully!")
    print(data)
finally:
    # Always executed
    if 'file' in locals():
        file.close()
```

### Custom Exceptions

```python
# Creating custom exceptions
class CustomError(Exception):
    """Base class for custom exceptions"""
    pass

class ValidationError(CustomError):
    """Raised when validation fails"""
    def __init__(self, message, field=None):
        super().__init__(message)
        self.field = field

class NetworkError(CustomError):
    """Raised when network operations fail"""
    pass

# Using custom exceptions
def validate_email(email):
    if '@' not in email:
        raise ValidationError("Email must contain @", field="email")
    if '.' not in email.split('@')[1]:
        raise ValidationError("Invalid domain", field="email")
    return True

def send_email(email, message):
    try:
        validate_email(email)
        # Simulate network operation
        import random
        if random.random() < 0.3:  # 30% chance of failure
            raise NetworkError("Failed to connect to email server")
        print(f"Email sent to {email}")
    except ValidationError as e:
        print(f"Validation error in {e.field}: {e}")
    except NetworkError as e:
        print(f"Network error: {e}")

# Context managers for resource management
class FileManager:
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode
        self.file = None
    
    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file
    
    def __exit__(self, exc_type, exc_value, traceback):
        if self.file:
            self.file.close()

# Usage
with FileManager("test.txt", "w") as f:
    f.write("Hello, World!")
# File is automatically closed
```

### Assertion and Debugging

```python
# Assertions for debugging
def divide(a, b):
    assert b != 0, "Division by zero is not allowed"
    return a / b

# Assertions can be disabled with -O flag
# python -O script.py

# Logging for better debugging
import logging

# Configure logging
logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s - %(levelname)s - %(message)s'
)

def process_data(data):
    logging.info(f"Processing data: {data}")
    
    if not isinstance(data, list):
        logging.error("Data must be a list")
        raise TypeError("Data must be a list")
    
    if not data:
        logging.warning("Empty data list provided")
        return []
    
    result = [x * 2 for x in data]
    logging.debug(f"Result: {result}")
    return result

# Usage
try:
    result = process_data([1, 2, 3, 4])
    print(result)
except Exception as e:
    logging.exception("An error occurred:")
```

---

## Advanced Data Structures

### Collections Module

```python
from collections import Counter, defaultdict, deque, namedtuple, OrderedDict

# Counter - for counting hashable objects
text = "hello world"
char_count = Counter(text)
print(char_count)  # Counter({'l': 3, 'o': 2, 'h': 1, 'e': 1, ' ': 1, 'w': 1, 'r': 1, 'd': 1})

# Most common elements
print(char_count.most_common(3))  # [('l', 3), ('o', 2), ('h', 1)]

# defaultdict - dictionary with default values
dd = defaultdict(list)
dd['fruits'].append('apple')
dd['fruits'].append('banana')
print(dd['fruits'])  # ['apple', 'banana']
print(dd['vegetables'])  # [] (empty list, not KeyError)

# deque - double-ended queue
dq = deque([1, 2, 3, 4, 5])
dq.appendleft(0)    # Add to left
dq.append(6)        # Add to right
print(dq)           # deque([0, 1, 2, 3, 4, 5, 6])

left = dq.popleft() # Remove from left
right = dq.pop()    # Remove from right

# namedtuple - tuple with named fields
Point = namedtuple('Point', ['x', 'y'])
p = Point(10, 20)
print(p.x, p.y)     # 10 20
print(p[0], p[1])   # 10 20 (still works like tuple)

# OrderedDict - dictionary that remembers insertion order
od = OrderedDict()
od['first'] = 1
od['second'] = 2
od['third'] = 3
```

### Advanced List Operations

```python
# List slicing advanced techniques
numbers = list(range(20))  # [0, 1, 2, 3, ..., 19]

# Advanced slicing patterns
print(numbers[::3])     # Every 3rd element: [0, 3, 6, 9, 12, 15, 18]
print(numbers[2::3])    # Starting from index 2, every 3rd: [2, 5, 8, 11, 14, 17]
print(numbers[::-2])    # Reverse, every 2nd: [19, 17, 15, 13, 11, 9, 7, 5, 3, 1]
print(numbers[10::-1])  # From index 10 to beginning, reversed: [10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]

# List operations and methods
data = [3, 1, 4, 1, 5, 9, 2, 6, 5]

# Sorting without modifying original
sorted_data = sorted(data)                    # [1, 1, 2, 3, 4, 5, 5, 6, 9]
reverse_sorted = sorted(data, reverse=True)   # [9, 6, 5, 5, 4, 3, 2, 1, 1]

# Custom sorting
words = ['apple', 'pie', 'banana', 'cherry']
by_length = sorted(words, key=len)            # ['pie', 'apple', 'banana', 'cherry']
by_last_char = sorted(words, key=lambda x: x[-1])  # ['apple', 'pie', 'banana', 'cherry']

# Filter, map, reduce
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Filter - keep only even numbers
evens = list(filter(lambda x: x % 2 == 0, numbers))  # [2, 4, 6, 8, 10]

# Map - transform each element
squares = list(map(lambda x: x**2, numbers))         # [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Reduce - accumulate values
from functools import reduce
sum_all = reduce(lambda x, y: x + y, numbers)        # 55
product = reduce(lambda x, y: x * y, numbers)        # 3628800

# Zip - combine multiple iterables
names = ['Alice', 'Bob', 'Charlie']
ages = [25, 30, 35]
cities = ['NYC', 'LA', 'Chicago']

combined = list(zip(names, ages, cities))
# [('Alice', 25, 'NYC'), ('Bob', 30, 'LA'), ('Charlie', 35, 'Chicago')]

# Unzip
names, ages, cities = zip(*combined)

# Any and all
numbers = [2, 4, 6, 8, 10]
print(all(x % 2 == 0 for x in numbers))  # True (all even)
print(any(x > 8 for x in numbers))       # True (at least one > 8)
```

### Generators and Iterators

```python
# Generator functions
def fibonacci(n):
    """Generate first n Fibonacci numbers"""
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

# Using generator
for num in fibonacci(10):
    print(num)

# Generator expressions
squares_gen = (x**2 for x in range(10))
print(next(squares_gen))  # 0
print(next(squares_gen))  # 1

# Custom iterator class
class CountDown:
    def __init__(self, start):
        self.start = start
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.start <= 0:
            raise StopIteration
        self.start -= 1
        return self.start + 1

# Usage
for num in CountDown(5):
    print(num)  # 5, 4, 3, 2, 1

# itertools module for advanced iteration
from itertools import count, cycle, repeat, chain, combinations, permutations

# Infinite iterators
counter = count(10, 2)  # Start at 10, step by 2
# next(counter) gives 10, 12, 14, 16, ...

cycler = cycle(['A', 'B', 'C'])  # Repeats A, B, C, A, B, C, ...

repeater = repeat('Hello', 3)    # Repeats 'Hello' 3 times

# Combinatorial iterators
letters = ['A', 'B', 'C']
numbers = [1, 2, 3]

# Chain multiple iterables
chained = list(chain(letters, numbers))  # ['A', 'B', 'C', 1, 2, 3]

# Combinations and permutations
combos = list(combinations(letters, 2))  # [('A', 'B'), ('A', 'C'), ('B', 'C')]
perms = list(permutations(letters, 2))   # [('A', 'B'), ('A', 'C'), ('B', 'A'), ('B', 'C'), ('C', 'A'), ('C', 'B')]
```

---

## Decorators and Context Managers

### Understanding Decorators

```python
# Basic decorator concept
def my_decorator(func):
    def wrapper():
        print("Something before the function")
        func()
        print("Something after the function")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

# Equivalent to: say_hello = my_decorator(say_hello)
say_hello()

# Decorator with arguments
def repeat(times):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(times):
                result = func(*args, **kwargs)
            return result
        return wrapper
    return decorator

@repeat(3)
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Prints greeting 3 times

# Preserving function metadata
from functools import wraps

def timer(func):
    @wraps(func)  # Preserves original function's metadata
    def wrapper(*args, **kwargs):
        import time
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

@timer
def slow_function(duration):
    """A function that takes some time"""
    import time
    time.sleep(duration)
    return "Completed"

print(slow_function.__name__)  # 'slow_function' (not 'wrapper')
print(slow_function.__doc__)   # Original docstring preserved

# Class-based decorators
class CountCalls:
    def __init__(self, func):
        self.func = func
        self.count = 0
    
    def __call__(self, *args, **kwargs):
        self.count += 1
        print(f"{self.func.__name__} has been called {self.count} times")
        return self.func(*args, **kwargs)

@CountCalls
def say_hi():
    print("Hi there!")

say_hi()  # say_hi has been called 1 times
say_hi()  # say_hi has been called 2 times

# Multiple decorators
def bold(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return f"<b>{result}</b>"
    return wrapper

def italic(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return f"<i>{result}</i>"
    return wrapper

@bold
@italic
def get_text():
    return "Hello World"

print(get_text())  # <b><i>Hello World</i></b>
```

### Context Managers

```python
# Using built-in context managers
with open('file.txt', 'w') as f:
    f.write('Hello, World!')
# File is automatically closed

# Custom context manager using class
class DatabaseConnection:
    def __init__(self, db_name):
        self.db_name = db_name
        self.connection = None
    
    def __enter__(self):
        print(f"Connecting to {self.db_name}")
        self.connection = f"Connected to {self.db_name}"
        return self.connection
    
    def __exit__(self, exc_type, exc_value, traceback):
        print(f"Closing connection to {self.db_name}")
        if exc_type:
            print(f"Exception occurred: {exc_value}")
        return False  # Don't suppress exceptions

# Usage
with DatabaseConnection("mydb") as conn:
    print(f"Using {conn}")
    # Connection is automatically closed

# Context manager using contextlib
from contextlib import contextmanager
import time

@contextmanager
def timer_context():
    start = time.time()
    try:
        yield
    finally:
        end = time.time()
        print(f"Execution took {end - start:.4f} seconds")

# Usage
with timer_context():
    time.sleep(1)
    print("Some operation")

# Suppress exceptions
from contextlib import suppress

with suppress(FileNotFoundError):
    with open('nonexistent.txt', 'r') as f:
        content = f.read()
# No exception raised for missing file

# Context manager for temporary directory
import tempfile
import os

@contextmanager
def temp_directory():
    temp_dir = tempfile.mkdtemp()
    try:
        yield temp_dir
    finally:
        import shutil
        shutil.rmtree(temp_dir)

with temp_directory() as temp_dir:
    print(f"Working in {temp_dir}")
    # Create files, do work...
# Directory is automatically cleaned up
```

---

## Concurrency and Async Programming

### Threading

```python
import threading
import time
import queue

# Basic threading
def worker(name, duration):
    print(f"Worker {name} starting")
    time.sleep(duration)
    print(f"Worker {name} finished")

# Create and start threads
threads = []
for i in range(3):
    t = threading.Thread(target=worker, args=(f"Thread-{i}", 2))
    threads.append(t)
    t.start()

# Wait for all threads to complete
for t in threads:
    t.join()

print("All threads completed")

# Thread-safe operations with locks
shared_resource = 0
lock = threading.Lock()

def increment():
    global shared_resource
    for _ in range(100000):
        with lock:  # or lock.acquire() ... lock.release()
            shared_resource += 1

threads = []
for i in range(5):
    t = threading.Thread(target=increment)
    threads.append(t)
    t.start()

for t in threads:
    t.join()

print(f"Final value: {shared_resource}")

# Producer-Consumer pattern with Queue
def producer(q):
    for i in range(5):
        item = f"item-{i}"
        q.put(item)
        print(f"Produced {item}")
        time.sleep(1)
    q.put(None)  # Signal end

def consumer(q):
    while True:
        item = q.get()
        if item is None:
            break
        print(f"Consumed {item}")
        time.sleep(2)
        q.task_done()

q = queue.Queue()
t1 = threading.Thread(target=producer, args=(q,))
t2 = threading.Thread(target=consumer, args=(q,))

t1.start()
t2.start()

t1.join()
t2.join()
```

### Multiprocessing

```python
import multiprocessing
import time

# Basic multiprocessing
def worker_process(name, duration):
    print(f"Process {name} starting (PID: {multiprocessing.current_process().pid})")
    time.sleep(duration)
    print(f"Process {name} finished")

if __name__ == "__main__":
    # Create and start processes
    processes = []
    for i in range(3):
        p = multiprocessing.Process(target=worker_process, args=(f"Process-{i}", 2))
        processes.append(p)
        p.start()
    
    # Wait for all processes to complete
    for p in processes:
        p.join()
    
    print("All processes completed")

# Process Pool for parallel execution
def square(n):
    return n * n

if __name__ == "__main__":
    with multiprocessing.Pool(processes=4) as pool:
        numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        results = pool.map(square, numbers)
        print(results)

# Shared memory between processes
def worker_with_shared_data(shared_list, shared_value, lock):
    with lock:
        shared_value.value += 1
        shared_list.append(shared_value.value)

if __name__ == "__main__":
    manager = multiprocessing.Manager()
    shared_list = manager.list()
    shared_value = manager.Value('i', 0)
    lock = multiprocessing.Lock()
    
    processes = []
    for i in range(5):
        p = multiprocessing.Process(
            target=worker_with_shared_data, 
            args=(shared_list, shared_value, lock)
        )
        processes.append(p)
        p.start()
    
    for p in processes:
        p.join()
    
    print(f"Shared list: {list(shared_list)}")
    print(f"Final value: {shared_value.value}")
```

### Async Programming

```python
import asyncio
import aiohttp
import time

# Basic async function
async def say_hello(name, delay):
    print(f"Hello {name}!")
    await asyncio.sleep(delay)
    print(f"Goodbye {name}!")

# Running async functions
async def main():
    # Sequential execution
    await say_hello("Alice", 1)
    await say_hello("Bob", 1)
    
    # Parallel execution
    await asyncio.gather(
        say_hello("Charlie", 1),
        say_hello("David", 1),
        say_hello("Eve", 1)
    )

# Run the main function
# asyncio.run(main())

# Async context manager
class AsyncContextManager:
    async def __aenter__(self):
        print("Entering async context")
        await asyncio.sleep(0.1)
        return self
    
    async def __aexit__(self, exc_type, exc_val, exc_tb):
        print("Exiting async context")
        await asyncio.sleep(0.1)

async def use_async_context():
    async with AsyncContextManager():
        print("Inside async context")

# Async iterators
class AsyncRange:
    def __init__(self, count):
        self.count = count
    
    def __aiter__(self):
        return self
    
    async def __anext__(self):
        if self.count <= 0:
            raise StopAsyncIteration
        self.count -= 1
        await asyncio.sleep(0.1)
        return self.count + 1

async def use_async_iterator():
    async for num in AsyncRange(5):
        print(num)

# Async HTTP requests
async def fetch_url(session, url):
    try:
        async with session.get(url) as response:
            return await response.text()
    except Exception as e:
        return f"Error: {e}"

async def fetch_multiple_urls():
    urls = [
        'http://httpbin.org/delay/1',
        'http://httpbin.org/delay/2',
        'http://httpbin.org/delay/1'
    ]
    
    async with aiohttp.ClientSession() as session:
        tasks = [fetch_url(session, url) for url in urls]
        results = await asyncio.gather(*tasks)
        return results

# Async generators
async def async_fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        await asyncio.sleep(0.1)  # Simulate async work
        a, b = b, a + b

async def use_async_generator():
    async for num in async_fibonacci(10):
        print(num)
```

---

## Best Practices and Design Patterns

### Code Style and PEP 8

```python
# Good naming conventions
class UserAccount:  # Classes use PascalCase
    def __init__(self, user_name, email_address):  # Methods use snake_case
        self.user_name = user_name  # Attributes use snake_case
        self.email_address = email_address
        self._private_attribute = None  # Private attributes start with _
        self.__very_private = None     # Name mangling with __

# Constants use UPPER_CASE
MAX_CONNECTIONS = 100
DEFAULT_TIMEOUT = 30

# Function and variable naming
def calculate_total_price(item_price, tax_rate=0.08):  # Descriptive names
    """Calculate total price including tax."""
    return item_price * (1 + tax_rate)

# List comprehensions vs loops
# Good: Concise and readable
even_squares = [x**2 for x in range(10) if x % 2 == 0]

# Avoid: Too complex for list comprehension
# result = [process_item(x) for sublist in data 
#           for x in sublist if complex_condition(x) and other_condition(x)]

# Better: Use regular loop for complex logic
result = []
for sublist in data:
    for x in sublist:
        if complex_condition(x) and other_condition(x):
            result.append(process_item(x))

# String formatting preferences
name = "Alice"
age = 30

# Best: f-strings (Python 3.6+)
message = f"Hello, {name}! You are {age} years old."

# Good: .format() method
message = "Hello, {}! You are {} years old.".format(name, age)

# Avoid: % formatting (unless necessary for compatibility)
message = "Hello, %s! You are %d years old." % (name, age)
```

### Design Patterns

```python
# Singleton Pattern
class DatabaseConnection:
    _instance = None
    _initialized = False
    
    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(DatabaseConnection, cls).__new__(cls)
        return cls._instance
    
    def __init__(self):
        if not self._initialized:
            self.connection = "Database connected"
            self._initialized = True

# Factory Pattern
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "Woof!"

class Cat(Animal):
    def make_sound(self):
        return "Meow!"

class AnimalFactory:
    @staticmethod
    def create_animal(animal_type):
        animals = {
            'dog': Dog,
            'cat': Cat
        }
        animal_class = animals.get(animal_type.lower())
        if animal_class:
            return animal_class()
        else:
            raise ValueError(f"Unknown animal type: {animal_type}")

# Usage
dog = AnimalFactory.create_animal('dog')
print(dog.make_sound())

# Observer Pattern
class Subject:
    def __init__(self):
        self._observers = []
        self._state = None
    
    def attach(self, observer):
        self._observers.append(observer)
    
    def detach(self, observer):
        self._observers.remove(observer)
    
    def notify(self):
        for observer in self._observers:
            observer.update(self._state)
    
    def set_state(self, state):
        self._state = state
        self.notify()

class Observer:
    def __init__(self, name):
        self.name = name
    
    def update(self, state):
        print(f"{self.name} received update: {state}")

# Usage
subject = Subject()
obs1 = Observer("Observer 1")
obs2 = Observer("Observer 2")

subject.attach(obs1)
subject.attach(obs2)
subject.set_state("New State")

# Strategy Pattern
class PaymentStrategy(ABC):
    @abstractmethod
    def pay(self, amount):
        pass

class CreditCardPayment(PaymentStrategy):
    def __init__(self, card_number):
        self.card_number = card_number
    
    def pay(self, amount):
        return f"Paid ${amount} using Credit Card ending in {self.card_number[-4:]}"

class PayPalPayment(PaymentStrategy):
    def __init__(self, email):
        self.email = email
    
    def pay(self, amount):
        return f"Paid ${amount} using PayPal account {self.email}"

class PaymentContext:
    def __init__(self, strategy: PaymentStrategy):
        self.strategy = strategy
    
    def set_strategy(self, strategy: PaymentStrategy):
        self.strategy = strategy
    
    def execute_payment(self, amount):
        return self.strategy.pay(amount)

# Usage
payment = PaymentContext(CreditCardPayment("1234567890123456"))
print(payment.execute_payment(100))

payment.set_strategy(PayPalPayment("user@example.com"))
print(payment.execute_payment(50))
```

### Testing

```python
# Unit testing with unittest
import unittest
from unittest.mock import patch, MagicMock

def add_numbers(a, b):
    return a + b

def divide_numbers(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b

class TestMathFunctions(unittest.TestCase):
    
    def test_add_numbers(self):
        self.assertEqual(add_numbers(2, 3), 5)
        self.assertEqual(add_numbers(-1, 1), 0)
        self.assertEqual(add_numbers(0, 0), 0)
    
    def test_divide_numbers(self):
        self.assertEqual(divide_numbers(10, 2), 5)
        self.assertEqual(divide_numbers(9, 3), 3)
        
        # Test exception
        with self.assertRaises(ValueError):
            divide_numbers(10, 0)
    
    def setUp(self):
        """Run before each test method"""
        self.test_data = [1, 2, 3, 4, 5]
    
    def tearDown(self):
        """Run after each test method"""
        pass
    
    @patch('requests.get')
    def test_api_call(self, mock_get):
        # Mock external API call
        mock_response = MagicMock()
        mock_response.json.return_value = {'status': 'success'}
        mock_get.return_value = mock_response
        
        # Test function that makes API call
        # result = some_function_that_calls_api()
        # self.assertEqual(result['status'], 'success')

# Run tests
if __name__ == '__main__':
    unittest.main()

# Doctest - tests in docstrings
def fibonacci(n):
    """
    Generate the nth Fibonacci number.
    
    >>> fibonacci(0)
    0
    >>> fibonacci(1)
    1
    >>> fibonacci(5)
    5
    >>> fibonacci(10)
    55
    """
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

# Run doctests
if __name__ == '__main__':
    import doctest
    doctest.testmod()

# pytest example (external library)
# pip install pytest
"""
# test_example.py
import pytest

def test_add_numbers():
    assert add_numbers(2, 3) == 5
    assert add_numbers(-1, 1) == 0

def test_divide_by_zero():
    with pytest.raises(ValueError):
        divide_numbers(10, 0)

@pytest.fixture
def sample_data():
    return [1, 2, 3, 4, 5]

def test_with_fixture(sample_data):
    assert len(sample_data) == 5
    assert sum(sample_data) == 15

# Run with: pytest test_example.py
"""
```

### Performance Optimization

```python
# Profiling code performance
import cProfile
import time
from functools import lru_cache

def slow_function():
    time.sleep(0.1)
    return "result"

def test_performance():
    for i in range(10):
        slow_function()

# Profile the code
# cProfile.run('test_performance()')

# Memoization with lru_cache
@lru_cache(maxsize=128)
def fibonacci_cached(n):
    if n <= 1:
        return n
    return fibonacci_cached(n-1) + fibonacci_cached(n-2)

# Time comparison
import time

def time_function(func, *args):
    start = time.time()
    result = func(*args)
    end = time.time()
    print(f"{func.__name__} took {end - start:.6f} seconds")
    return result

# List comprehension vs for loop performance
def list_comp_method():
    return [x**2 for x in range(10000)]

def for_loop_method():
    result = []
    for x in range(10000):
        result.append(x**2)
    return result

# Generator for memory efficiency
def generate_squares(n):
    """Generator - memory efficient for large datasets"""
    for i in range(n):
        yield i**2

def list_squares(n):
    """List - uses more memory but faster access"""
    return [i**2 for i in range(n)]

# Using slots for memory optimization
class Point:
    __slots__ = ['x', 'y']  # Reduces memory usage
    
    def __init__(self, x, y):
        self.x = x
        self.y = y

class RegularPoint:
    def __init__(self, x, y):
        self.x = x
        self.y = y

# Efficient string operations
# Inefficient: repeated string concatenation
def inefficient_string_concat():
    result = ""
    for i in range(1000):
        result += str(i) + ","
    return result

# Efficient: join method
def efficient_string_concat():
    return ",".join(str(i) for i in range(1000))

# Using collections.defaultdict for grouping
from collections import defaultdict

data = [('apple', 5), ('banana', 3), ('apple', 2), ('cherry', 8)]

# Group by key efficiently
grouped = defaultdict(list)
for key, value in data:
    grouped[key].append(value)

print(dict(grouped))  # {'apple': [5, 2], 'banana': [3], 'cherry': [8]}
```

### Logging and Configuration

```python
# Advanced logging configuration
import logging
import logging.config
from datetime import datetime

# Configure logging
LOGGING_CONFIG = {
    'version': 1,
    'disable_existing_loggers': False,
    'formatters': {
        'standard': {
            'format': '%(asctime)s [%(levelname)s] %(name)s: %(message)s'
        },
        'detailed': {
            'format': '%(asctime)s [%(levelname)s] %(name)s:%(lineno)d: %(message)s'
        },
    },
    'handlers': {
        'default': {
            'level': 'INFO',
            'formatter': 'standard',
            'class': 'logging.StreamHandler',
        },
        'file': {
            'level': 'DEBUG',
            'formatter': 'detailed',
            'class': 'logging.FileHandler',
            'filename': 'app.log',
            'mode': 'a',
        },
    },
    'loggers': {
        '': {  # root logger
            'handlers': ['default', 'file'],
            'level': 'DEBUG',
            'propagate': False
        }
    }
}

logging.config.dictConfig(LOGGING_CONFIG)
logger = logging.getLogger(__name__)

# Usage
logger.debug("Debug message")
logger.info("Info message")
logger.warning("Warning message")
logger.error("Error message")
logger.critical("Critical message")

# Configuration management
import configparser
import os
from pathlib import Path

# config.ini file
"""
[database]
host = localhost
port = 5432
name = myapp
user = admin

[api]
base_url = https://api.example.com
timeout = 30
retry_count = 3

[logging]
level = INFO
file_path = /var/log/myapp.log
"""

# Reading configuration
config = configparser.ConfigParser()
config.read('config.ini')

# Accessing configuration
db_host = config['database']['host']
db_port = config.getint('database', 'port')
api_timeout = config.getint('api', 'timeout')

# Environment variables for sensitive data
API_KEY = os.getenv('API_KEY', 'default_key')
SECRET_TOKEN = os.getenv('SECRET_TOKEN')

# Configuration class
class Config:
    def __init__(self, config_file='config.ini'):
        self.config = configparser.ConfigParser()
        self.config.read(config_file)
    
    @property
    def database_url(self):
        db_config = self.config['database']
        return f"postgresql://{db_config['user']}@{db_config['host']}:{db_config['port']}/{db_config['name']}"
    
    @property
    def api_config(self):
        return {
            'base_url': self.config['api']['base_url'],
            'timeout': self.config.getint('api', 'timeout'),
            'retry_count': self.config.getint('api', 'retry_count')
        }

# Usage
app_config = Config()
print(app_config.database_url)
print(app_config.api_config)
```

---

## Conclusion

This comprehensive guide covers Python from basic concepts to advanced topics. Here are some key takeaways:

### Learning Path Recommendations:

1. **Beginners**: Start with basic syntax, data types, and control structures
2. **Intermediate**: Focus on functions, OOP, file handling, and error handling
3. **Advanced**: Explore decorators, context managers, async programming, and design patterns

### Best Practices to Remember:

- Follow PEP 8 style guidelines
- Write readable, self-documenting code
- Use meaningful variable and function names
- Handle errors gracefully
- Write tests for your code
- Use virtual environments for project isolation
- Keep functions small and focused on single tasks
- Document your code with docstrings

### Next Steps:

- **Web Development**: Learn Flask or Django
- **Data Science**: Explore NumPy, Pandas, Matplotlib
- **Machine Learning**: Study scikit-learn, TensorFlow, PyTorch
- **Automation**: Practice with web scraping, APIs, file processing
- **Desktop Apps**: Try Tkinter, PyQt, or Kivy
- **Game Development**: Experiment with Pygame

### Useful Resources:

- Python.org documentation
- Real Python tutorials
- Python Package Index (PyPI)
- GitHub for open-source projects
- Stack Overflow for problem-solving
- Python Enhancement Proposals (PEPs) for language evolution

---

## Appendix: Quick Reference

### Common Built-in Functions

```python
# Type conversion
int(), float(), str(), bool(), list(), tuple(), dict(), set()

# Math functions
abs(-5)           # 5
min(1, 2, 3)     # 1
max(1, 2, 3)     # 3
sum([1, 2, 3])   # 6
round(3.14159, 2) # 3.14
pow(2, 3)        # 8

# Sequence functions
len([1, 2, 3])   # 3
sorted([3, 1, 2]) # [1, 2, 3]
reversed([1, 2, 3]) # iterator
enumerate(['a', 'b', 'c']) # [(0, 'a'), (1, 'b'), (2, 'c')]
zip([1, 2], ['a', 'b']) # [(1, 'a'), (2, 'b')]

# Input/Output
input("Prompt: ")
print("Hello", "World", sep="-", end="!\n")

# Object inspection
type(obj)        # Object type
isinstance(obj, int) # Check type
hasattr(obj, 'attr') # Check attribute
getattr(obj, 'attr', default) # Get attribute
dir(obj)         # List attributes and methods
help(obj)        # Get help information
```

### String Methods Quick Reference

```python
s = "Hello World"

# Case methods
s.upper()        # "HELLO WORLD"
s.lower()        # "hello world"
s.title()        # "Hello World"
s.capitalize()   # "Hello world"
s.swapcase()     # "hELLO wORLD"

# Test methods
s.isdigit()      # False
s.isalpha()      # False (has space)
s.isalnum()      # False (has space)
s.isspace()      # False
s.isupper()      # False
s.islower()      # False

# Search methods
s.startswith("Hello") # True
s.endswith("World")   # True
s.find("World")       # 6 (index)
s.index("World")      # 6 (raises exception if not found)
s.count("l")          # 3

# Modification methods
s.replace("World", "Python") # "Hello Python"
s.strip()            # Remove whitespace
s.split()            # ["Hello", "World"]
"-".join(["a", "b"]) # "a-b"
```

### List Methods Quick Reference

```python
lst = [1, 2, 3]

# Adding elements
lst.append(4)        # [1, 2, 3, 4]
lst.insert(1, 'x')   # [1, 'x', 2, 3, 4]
lst.extend([5, 6])   # [1, 'x', 2, 3, 4, 5, 6]

# Removing elements
lst.remove('x')      # Remove first occurrence
lst.pop()            # Remove and return last item
lst.pop(0)           # Remove and return item at index
lst.clear()          # Remove all items

# Searching and counting
lst.index(2)         # Find index of first occurrence
lst.count(2)         # Count occurrences

# Sorting and reversing
lst.sort()           # Sort in place
lst.reverse()        # Reverse in place
lst.copy()           # Shallow copy
```

### Dictionary Methods Quick Reference

```python
d = {'a': 1, 'b': 2, 'c': 3}

# Accessing
d['a']               # 1 (KeyError if not found)
d.get('a', 0)        # 1 (return default if not found)

# Adding/Updating
d['d'] = 4           # Add new key-value pair
d.update({'e': 5, 'f': 6}) # Update multiple

# Removing
del d['a']           # Remove key
d.pop('b')           # Remove and return value
d.popitem()          # Remove and return arbitrary item
d.clear()            # Remove all items

# Views
d.keys()             # Dictionary keys
d.values()           # Dictionary values
d.items()            # Key-value pairs

# Copying
d.copy()             # Shallow copy
```

### File Operations Quick Reference

```python
# Reading files
with open('file.txt', 'r') as f:
    content = f.read()           # Read entire file
    lines = f.readlines()        # Read all lines as list
    line = f.readline()          # Read one line
    
    for line in f:               # Iterate over lines
        print(line.strip())

# Writing files
with open('file.txt', 'w') as f:
    f.write("Hello\n")           # Write string
    f.writelines(["Line 1\n", "Line 2\n"]) # Write list of strings

# File modes
# 'r' - read, 'w' - write, 'a' - append, 'x' - create
# 'b' - binary, 't' - text (default)
# '+' - read and write
```

### Exception Types Quick Reference

```python
# Common built-in exceptions
ValueError          # Invalid value
TypeError           # Wrong type
IndexError          # List index out of range
KeyError            # Dictionary key not found
AttributeError      # Attribute doesn't exist
FileNotFoundError   # File doesn't exist
PermissionError     # No permission
ZeroDivisionError   # Division by zero
ImportError         # Module can't be imported
NameError           # Variable not defined
SyntaxError         # Invalid syntax
IndentationError    # Wrong indentation
```

### Regular Expressions Quick Reference

```python
import re

# Common patterns
r'\d'               # Any digit
r'\w'               # Any word character
r'\s'               # Any whitespace
r'.'                # Any character except newline
r'^'                # Start of string
r'                # End of string
r'*'                # Zero or more
r'+'                # One or more
r'?'                # Zero or one
r'{n}'              # Exactly n times
r'{n,m}'            # Between n and m times

# Common functions
re.search(pattern, string)    # Find first match
re.match(pattern, string)     # Match at beginning
re.findall(pattern, string)   # Find all matches
re.sub(pattern, repl, string) # Replace matches
re.split(pattern, string)     # Split string

# Example usage
email_pattern = r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b'
phone_pattern = r'\d{3}-\d{3}-\d{4}'
```

### Virtual Environment Commands

```bash
# Create virtual environment
python -m venv myenv

# Activate (Windows)
myenv\Scripts\activate

# Activate (macOS/Linux)
source myenv/bin/activate

# Deactivate
deactivate

# Install packages
pip install package_name
pip install -r requirements.txt

# Generate requirements file
pip freeze > requirements.txt

# List installed packages
pip list
```

### Useful Libraries to Explore

#### Data Science & Analysis
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical data visualization
- **SciPy**: Scientific computing
- **Jupyter**: Interactive notebooks

#### Web Development
- **Flask**: Lightweight web framework
- **Django**: Full-featured web framework
- **FastAPI**: Modern, fast web framework
- **Requests**: HTTP library
- **Beautiful Soup**: Web scraping

#### Machine Learning
- **Scikit-learn**: Machine learning library
- **TensorFlow**: Deep learning framework
- **PyTorch**: Deep learning framework
- **Keras**: High-level neural networks API

#### GUI Development
- **Tkinter**: Built-in GUI toolkit
- **PyQt/PySide**: Cross-platform GUI toolkit
- **Kivy**: Multi-platform GUI framework

#### Database
- **SQLAlchemy**: SQL toolkit and ORM
- **PyMongo**: MongoDB driver
- **sqlite3**: Built-in SQLite interface

#### Testing
- **pytest**: Testing framework
- **unittest.mock**: Mock object library
- **coverage**: Code coverage measurement

#### Other Useful Libraries
- **Pillow**: Image processing
- **openpyxl**: Excel file handling
- **python-dateutil**: Date/time utilities
- **click**: Command line interface creation
- **rich**: Rich text and beautiful formatting

---

## Final Tips for Python Mastery

### Code Organization Tips

```python
# Project structure example
"""
myproject/
├── src/
│   ├── __init__.py
│   ├── main.py
│   ├── models/
│   │   ├── __init__.py
│   │   └── user.py
│   └── utils/
│       ├── __init__.py
│       └── helpers.py
├── tests/
│   ├── __init__.py
│   ├── test_main.py
│   └── test_models.py
├── requirements.txt
├── README.md
└── setup.py
"""

# Use __init__.py for package initialization
# src/__init__.py
__version__ = "1.0.0"
__author__ = "Your Name"

from .main import main_function
from .models import User

__all__ = ['main_function', 'User']
```

### Debugging Tips

```python
# Using pdb debugger
import pdb

def problematic_function(data):
    pdb.set_trace()  # Debugger will stop here
    result = process_data(data)
    return result

# Using logging for debugging
import logging
logging.basicConfig(level=logging.DEBUG)

def debug_function(x, y):
    logging.debug(f"Input: x={x}, y={y}")
    result = x + y
    logging.debug(f"Result: {result}")
    return result

# Assert statements for debugging
def divide(a, b):
    assert isinstance(a, (int, float)), f"a must be a number, got {type(a)}"
    assert isinstance(b, (int, float)), f"b must be a number, got {type(b)}"
    assert b != 0, "Cannot divide by zero"
    return a / b
```

### Performance Tips

```python
# Use generators for large datasets
def read_large_file(file_path):
    with open(file_path) as f:
        for line in f:
            yield line.strip()

# Use list comprehensions instead of loops when appropriate
squares = [x**2 for x in range(100)]  # Faster than loop

# Use built-in functions
sum([1, 2, 3, 4, 5])  # Faster than manual loop

# Use sets for membership testing
allowed_ids = {1, 2, 3, 4, 5}
if user_id in allowed_ids:  # O(1) vs O(n) for list
    print("Access granted")

# Use dict.get() instead of key checking
value = my_dict.get('key', 'default')  # Better than if/else
```

### Security Considerations

```python
# Input validation
def validate_email(email):
    import re
    pattern = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}
    return re.match(pattern, email) is not None

# Avoid eval() and exec() with user input
# BAD: eval(user_input)
# GOOD: Use ast.literal_eval() for safe evaluation
import ast
try:
    data = ast.literal_eval(user_input)  # Only evaluates literals
except (ValueError, SyntaxError):
    print("Invalid input")

# Use secrets module for cryptographic randomness
import secrets
token = secrets.token_urlsafe(32)  # Secure random token
```

This comprehensive Python guide should serve as your reference for progressing from basic to advanced Python programming. Remember that mastering Python is a journey - practice regularly, build projects, and don't hesitate to explore the vast ecosystem of Python libraries and frameworks!
