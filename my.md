# Complete Python Programming Learning Guide

## Table of Contents
1. [Basics of Programming](#basics-of-programming)
2. [Basics of Python](#basics-of-python)
3. [Variables and Data Types](#variables-and-data-types)
4. [Python Operators](#python-operators)
5. [Branching Structure](#branching-structure)
6. [Looping Structure](#looping-structure)
7. [List Structure](#list-structure)
8. [Tuple Structure](#tuple-structure)
9. [Set Structure](#set-structure)
10. [Dictionary Structure](#dictionary-structure)
11. [Function Operations](#function-operations)
12. [File Operations](#file-operations)

---

## Basics of Programming

### Computer Programming
**Computer Programming** is the process of creating instructions for computers to execute. It involves writing code in a programming language to solve problems or perform specific tasks.

### Programming Language Classification
Programming languages are classified into:
- **Low-level languages**: Machine language, Assembly language
- **High-level languages**: Python, Java, C++, JavaScript
- **Scripting languages**: Python, JavaScript, Bash
- **Compiled vs Interpreted**: 
  - Compiled: C, C++, Java
  - Interpreted: Python, JavaScript

### Translator Programs
- **Compiler**: Translates entire program at once (C, C++)
- **Interpreter**: Translates line by line (Python)
- **Assembler**: Translates assembly language to machine code

### Algorithm and Flowchart

**Algorithm**: A step-by-step procedure to solve a problem.

**Example Algorithm (Find largest of two numbers)**:
1. Start
2. Input A and B
3. If A > B, then largest = A
4. Else largest = B
5. Display largest
6. Stop

**Flowchart Rules**:
- Use standard symbols (oval for start/stop, rectangle for process, diamond for decision)
- Flow should be top to bottom, left to right
- Use arrows to show flow direction
- Each symbol should have only one entry and exit point (except decision)

---

## Basics of Python

### Features of Python
- **Simple and Easy**: Clear, readable syntax
- **Interpreted**: No compilation needed
- **Object-Oriented**: Supports OOP concepts
- **Cross-platform**: Runs on Windows, Linux, Mac
- **Extensive Libraries**: Rich standard library
- **Free and Open Source**

### Identifiers and Keywords

**Identifiers**: Names given to variables, functions, classes
- Rules: Start with letter or underscore, can contain letters, digits, underscores
- Case-sensitive
- Cannot be keywords

**Keywords**: Reserved words in Python
```python
# Some Python keywords
and, or, not, if, else, elif, while, for, def, class, import, from, as, try, except
```

### Lines and Indentation
```python
# Single line
print("Hello World")

# Multiple lines using backslash
total = item_one + \
        item_two + \
        item_three

# Multiple lines with brackets
days = ['Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday']

# Indentation is crucial in Python
if True:
    print("True")  # 4 spaces indentation
    if True:
        print("Nested")  # 8 spaces indentation
```

### Quotation and Comments
```python
# Single line comment
print("Hello")  # End of line comment

"""
Multi-line comment
or docstring
"""

# Quotations
single_quote = 'Hello'
double_quote = "Hello"
triple_quote = """Multi-line
string"""
```

### Command Line Arguments
```python
import sys
print("Script name:", sys.argv[0])
print("Arguments:", sys.argv[1:])
```

---

## Variables and Data Types

### Variables
Variables are containers for storing data values.

**Naming Rules**:
- Start with letter or underscore
- Can contain letters, numbers, underscores
- Case-sensitive
- Cannot use keywords

```python
# Valid variable names
name = "John"
age = 25
_private = "hidden"
user_name = "john_doe"

# Invalid variable names
# 2name = "John"  # Starts with number
# user-name = "John"  # Contains hyphen
```

### Assigning Values
```python
# Single assignment
x = 5
name = "Alice"

# Multiple assignment
a, b, c = 1, 2, 3
x = y = z = 10

# Swapping values
a, b = b, a
```

### Standard Data Types

#### 1. Numbers
```python
# Integer
age = 25
negative = -10

# Float
price = 99.99
scientific = 1.2e3  # 1200.0

# Complex
complex_num = 3 + 4j
```

#### 2. Strings
```python
name = "Alice"
message = 'Hello World'
multiline = """This is a
multiline string"""

# String operations
full_name = "John" + " " + "Doe"  # Concatenation
repeated = "Ha" * 3  # "HaHaHa"
```

#### 3. Lists
```python
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]
```

#### 4. Tuples
```python
coordinates = (10, 20)
colors = ("red", "green", "blue")
```

#### 5. Dictionaries
```python
person = {"name": "Alice", "age": 30}
grades = {"math": 95, "science": 87}
```

#### 6. Sets
```python
unique_numbers = {1, 2, 3, 4, 5}
fruits = {"apple", "banana", "orange"}
```

#### 7. Boolean
```python
is_student = True
is_working = False
```

### Data Type Conversion
```python
# Implicit conversion
x = 10
y = 3.14
result = x + y  # result is float

# Explicit conversion
num_str = "123"
num_int = int(num_str)  # String to integer
num_float = float(num_str)  # String to float
str_num = str(123)  # Integer to string

# Other conversions
list_from_string = list("hello")  # ['h', 'e', 'l', 'l', 'o']
tuple_from_list = tuple([1, 2, 3])  # (1, 2, 3)
```

---

## Python Operators

### Arithmetic Operators
```python
a = 10
b = 3

addition = a + b        # 13
subtraction = a - b     # 7
multiplication = a * b  # 30
division = a / b        # 3.333...
floor_division = a // b # 3
modulus = a % b         # 1
exponent = a ** b       # 1000
```

### Comparison Operators
```python
a = 10
b = 5

equal = a == b          # False
not_equal = a != b      # True
greater = a > b         # True
less = a < b            # False
greater_equal = a >= b  # True
less_equal = a <= b     # False
```

### Logical Operators
```python
x = True
y = False

and_result = x and y    # False
or_result = x or y      # True
not_result = not x      # False

# With conditions
age = 25
if age >= 18 and age <= 65:
    print("Working age")
```

### Assignment Operators
```python
x = 10
x += 5   # x = x + 5  → 15
x -= 3   # x = x - 3  → 12
x *= 2   # x = x * 2  → 24
x /= 4   # x = x / 4  → 6.0
x //= 2  # x = x // 2 → 3.0
x %= 2   # x = x % 2  → 1.0
x **= 3  # x = x ** 3 → 1.0
```

### Bitwise Operators
```python
a = 12  # 1100 in binary
b = 7   # 0111 in binary

bitwise_and = a & b     # 4 (0100)
bitwise_or = a | b      # 15 (1111)
bitwise_xor = a ^ b     # 11 (1011)
bitwise_not = ~a        # -13
left_shift = a << 1     # 24 (11000)
right_shift = a >> 1    # 6 (0110)
```

### Membership Operators
```python
fruits = ["apple", "banana", "orange"]
print("apple" in fruits)      # True
print("grape" not in fruits)  # True

# With strings
text = "Hello World"
print("Hello" in text)        # True
```

### Identity Operators
```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(a is c)      # True (same object)
print(a is b)      # False (different objects)
print(a == b)      # True (same content)
print(a is not b)  # True
```

### Operator Precedence (High to Low)
1. `()` - Parentheses
2. `**` - Exponentiation
3. `+x, -x, ~x` - Unary operators
4. `*, /, //, %` - Multiplication, division
5. `+, -` - Addition, subtraction
6. `<<, >>` - Bitwise shifts
7. `&` - Bitwise AND
8. `^` - Bitwise XOR
9. `|` - Bitwise OR
10. `==, !=, <, >, <=, >=, is, is not, in, not in` - Comparisons
11. `not` - Logical NOT
12. `and` - Logical AND
13. `or` - Logical OR

---

## Branching Structure

### Conditional Statements

#### Simple if Statement
```python
age = 18
if age >= 18:
    print("You can vote")
```

#### if-else Statement
```python
number = 10
if number % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

#### if-elif-else Statement
```python
marks = 85

if marks >= 90:
    grade = "A+"
elif marks >= 80:
    grade = "A"
elif marks >= 70:
    grade = "B"
elif marks >= 60:
    grade = "C"
else:
    grade = "F"

print(f"Grade: {grade}")
```

### Nested if Statements
```python
age = 25
income = 50000

if age >= 18:
    if income >= 30000:
        print("Eligible for loan")
    else:
        print("Income too low")
else:
    print("Age requirement not met")
```

### Practical Examples

#### Find Largest of Three Numbers
```python
def find_largest(a, b, c):
    if a >= b and a >= c:
        return a
    elif b >= a and b >= c:
        return b
    else:
        return c

# Usage
num1, num2, num3 = 10, 25, 15
largest = find_largest(num1, num2, num3)
print(f"Largest: {largest}")
```

#### Leap Year Check
```python
def is_leap_year(year):
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                return True
            else:
                return False
        else:
            return True
    else:
        return False

# Usage
year = 2024
if is_leap_year(year):
    print(f"{year} is a leap year")
else:
    print(f"{year} is not a leap year")
```

---

## Looping Structure

### for Loop
```python
# Basic for loop
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Loop with start, stop, step
for i in range(2, 10, 2):
    print(i)  # 2, 4, 6, 8

# Loop through list
fruits = ["apple", "banana", "orange"]
for fruit in fruits:
    print(fruit)

# Loop through string
for char in "Hello":
    print(char)
```

### while Loop
```python
# Basic while loop
count = 0
while count < 5:
    print(count)
    count += 1

# While with condition
number = 1
while number <= 10:
    if number % 2 == 0:
        print(f"{number} is even")
    number += 1
```

### Nested Loops
```python
# Nested for loops - multiplication table
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i} x {j} = {i*j}")
    print()  # New line after each table

# Pattern printing
for i in range(5):
    for j in range(i + 1):
        print("*", end="")
    print()  # New line
```

### Loop Control Statements

#### break Statement
```python
for i in range(10):
    if i == 5:
        break
    print(i)  # Prints 0, 1, 2, 3, 4
```

#### continue Statement
```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # Prints 1, 3, 5, 7, 9
```

#### else with Loops
```python
for i in range(5):
    print(i)
else:
    print("Loop completed normally")

# With break
for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("This won't print")  # else doesn't execute when break is used
```

### Practical Examples

#### Prime Number Check
```python
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Find prime numbers up to 20
for num in range(2, 21):
    if is_prime(num):
        print(num, end=" ")
```

#### Fibonacci Series
```python
def fibonacci(n):
    if n <= 1:
        return n
    
    a, b = 0, 1
    for i in range(2, n + 1):
        a, b = b, a + b
    return b

# Print first 10 Fibonacci numbers
for i in range(10):
    print(fibonacci(i), end=" ")
```

#### Factorial
```python
def factorial(n):
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

# Calculate factorial of 5
print(f"5! = {factorial(5)}")
```

---

## List Structure

### Creating Lists
```python
# Empty list
empty_list = []
empty_list2 = list()

# List with elements
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# List from range
numbers = list(range(1, 6))  # [1, 2, 3, 4, 5]
```

### Accessing List Elements
```python
fruits = ["apple", "banana", "orange", "grape"]

# Positive indexing
print(fruits[0])    # apple
print(fruits[1])    # banana

# Negative indexing
print(fruits[-1])   # grape
print(fruits[-2])   # orange

# Slicing
print(fruits[1:3])  # ['banana', 'orange']
print(fruits[:2])   # ['apple', 'banana']
print(fruits[2:])   # ['orange', 'grape']
print(fruits[:])    # ['apple', 'banana', 'orange', 'grape']
```

### Updating Lists
```python
fruits = ["apple", "banana", "orange"]

# Modify single element
fruits[1] = "mango"
print(fruits)  # ['apple', 'mango', 'orange']

# Modify multiple elements
fruits[1:3] = ["kiwi", "grape"]
print(fruits)  # ['apple', 'kiwi', 'grape']

# Add elements
fruits.append("cherry")      # Add at end
fruits.insert(1, "berry")   # Add at specific position
fruits.extend(["peach", "plum"])  # Add multiple elements

print(fruits)  # ['apple', 'berry', 'kiwi', 'grape', 'cherry', 'peach', 'plum']
```

### Deleting from Lists
```python
fruits = ["apple", "banana", "orange", "grape", "banana"]

# Remove by value (first occurrence)
fruits.remove("banana")
print(fruits)  # ['apple', 'orange', 'grape', 'banana']

# Remove by index
deleted_item = fruits.pop(2)  # Removes and returns 'grape'
print(fruits)  # ['apple', 'orange', 'banana']

# Remove last element
last_item = fruits.pop()
print(fruits)  # ['apple', 'orange']

# Delete by index
del fruits[0]
print(fruits)  # ['orange']

# Clear all elements
fruits.clear()
print(fruits)  # []
```

### List Operations
```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

# Concatenation
result = list1 + list2  # [1, 2, 3, 4, 5, 6]

# Repetition
repeated = list1 * 3    # [1, 2, 3, 1, 2, 3, 1, 2, 3]

# Membership
print(2 in list1)       # True
print(7 not in list1)   # True

# Length
print(len(list1))       # 3

# Minimum and Maximum
numbers = [10, 5, 8, 20, 3]
print(min(numbers))     # 3
print(max(numbers))     # 20
print(sum(numbers))     # 46
```

### Built-in List Functions and Methods
```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]

# Sorting
numbers.sort()          # Sort in place
print(numbers)          # [1, 1, 2, 3, 4, 5, 6, 9]

sorted_list = sorted([3, 1, 4, 1, 5])  # Returns new sorted list
numbers.sort(reverse=True)  # Sort in descending order

# Reversing
numbers.reverse()
print(numbers)

# Count occurrences
count = numbers.count(1)
print(f"1 appears {count} times")

# Find index
index = numbers.index(5)
print(f"5 is at index {index}")

# Copy list
numbers_copy = numbers.copy()
```

### List Comprehensions
```python
# Basic list comprehension
squares = [x**2 for x in range(1, 6)]  # [1, 4, 9, 16, 25]

# With condition
evens = [x for x in range(1, 11) if x % 2 == 0]  # [2, 4, 6, 8, 10]

# With string manipulation
words = ["hello", "world", "python"]
upper_words = [word.upper() for word in words]  # ['HELLO', 'WORLD', 'PYTHON']
```

---

## Tuple Structure

### Creating Tuples
```python
# Empty tuple
empty_tuple = ()
empty_tuple2 = tuple()

# Tuple with elements
coordinates = (10, 20)
colors = ("red", "green", "blue")
mixed = (1, "hello", 3.14, True)

# Single element tuple (note the comma)
single = (5,)  # or single = 5,

# Tuple without parentheses
point = 10, 20, 30
```

### Accessing Tuple Elements
```python
colors = ("red", "green", "blue", "yellow")

# Positive indexing
print(colors[0])    # red
print(colors[1])    # green

# Negative indexing
print(colors[-1])   # yellow
print(colors[-2])   # blue

# Slicing
print(colors[1:3])  # ('green', 'blue')
print(colors[:2])   # ('red', 'green')
print(colors[2:])   # ('blue', 'yellow')
```

### Difference Between List and Tuple

| List | Tuple |
|------|-------|
| Mutable (can be changed) | Immutable (cannot be changed) |
| Uses square brackets [] | Uses parentheses () |
| More memory consumption | Less memory consumption |
| Slower | Faster |
| Can use as dictionary key: No | Can use as dictionary key: Yes |

```python
# List - Mutable
my_list = [1, 2, 3]
my_list[0] = 10  # This works
print(my_list)   # [10, 2, 3]

# Tuple - Immutable
my_tuple = (1, 2, 3)
# my_tuple[0] = 10  # This would cause an error
```

### Updating Tuples (Workaround)
```python
# Since tuples are immutable, you can't directly update them
# But you can create a new tuple
original = (1, 2, 3)
updated = original + (4, 5)  # (1, 2, 3, 4, 5)

# Or convert to list, modify, then back to tuple
temp_list = list(original)
temp_list.append(4)
updated = tuple(temp_list)
```

### Deleting Tuples
```python
colors = ("red", "green", "blue")

# You cannot delete individual elements
# del colors[0]  # This would cause an error

# But you can delete the entire tuple
del colors
# print(colors)  # This would cause an error as colors no longer exists
```

### Tuple Operations
```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)

# Concatenation
result = tuple1 + tuple2  # (1, 2, 3, 4, 5, 6)

# Repetition
repeated = tuple1 * 3     # (1, 2, 3, 1, 2, 3, 1, 2, 3)

# Membership
print(2 in tuple1)        # True
print(7 not in tuple1)    # True

# Length
print(len(tuple1))        # 3

# Min, Max, Sum
numbers = (10, 5, 8, 20, 3)
print(min(numbers))       # 3
print(max(numbers))       # 20
print(sum(numbers))       # 46
```

### Built-in Tuple Functions
```python
numbers = (3, 1, 4, 1, 5, 9, 2, 6, 1)

# Count occurrences
count = numbers.count(1)
print(f"1 appears {count} times")  # 1 appears 3 times

# Find index of first occurrence
index = numbers.index(5)
print(f"5 is at index {index}")    # 5 is at index 4

# Convert to other types
numbers_list = list(numbers)
numbers_set = set(numbers)
```

### Tuple Unpacking
```python
# Assigning tuple values to variables
point = (10, 20, 30)
x, y, z = point
print(f"x={x}, y={y}, z={z}")

# Swapping variables
a = 5
b = 10
a, b = b, a  # Now a=10, b=5

# Function returning multiple values
def get_name_age():
    return "Alice", 25

name, age = get_name_age()
```

---

## Set Structure

### Creating Sets
```python
# Empty set
empty_set = set()  # Note: {} creates an empty dictionary

# Set with elements
fruits = {"apple", "banana", "orange"}
numbers = {1, 2, 3, 4, 5}
mixed = {1, "hello", 3.14}  # Note: can't have mutable elements like lists

# Set from list (removes duplicates)
numbers_list = [1, 2, 2, 3, 3, 4]
unique_numbers = set(numbers_list)  # {1, 2, 3, 4}

# Set from string
letters = set("hello")  # {'h', 'e', 'l', 'o'}
```

### Properties of Set Items
1. **Unordered**: Items don't have a defined order
2. **Unchangeable**: Can't change items, but can add/remove
3. **No Duplicates**: Duplicate values are automatically removed
4. **Immutable Elements**: Set items must be immutable (strings, numbers, tuples)

```python
# Duplicates are automatically removed
numbers = {1, 2, 2, 3, 3, 4}
print(numbers)  # {1, 2, 3, 4}

# Can't have mutable elements
# invalid_set = {[1, 2], [3, 4]}  # This would cause an error
```

### Adding Items to Sets
```python
fruits = {"apple", "banana"}

# Add single item
fruits.add("orange")
print(fruits)  # {'apple', 'banana', 'orange'}

# Add multiple items
fruits.update(["grape", "kiwi"])
# or
fruits.update({"mango", "peach"})
print(fruits)  # {'apple', 'banana', 'orange', 'grape', 'kiwi', 'mango', 'peach'}

# Update with another set
tropical_fruits = {"pineapple", "coconut"}
fruits.update(tropical_fruits)
```

### Removing Items from Sets
```python
fruits = {"apple", "banana", "orange", "grape"}

# Remove specific item (raises error if not found)
fruits.remove("banana")
print(fruits)  # {'apple', 'orange', 'grape'}

# Discard specific item (no error if not found)
fruits.discard("kiwi")  # No error even though kiwi is not in set
fruits.discard("apple")
print(fruits)  # {'orange', 'grape'}

# Remove and return arbitrary item
item = fruits.pop()
print(f"Removed: {item}")
print(fruits)

# Clear all items
fruits.clear()
print(fruits)  # set()

# Delete entire set
del fruits
```

### Set Operations

#### Union (|)
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Union - all unique elements from both sets
union_result = set1 | set2          # {1, 2, 3, 4, 5, 6}
# or
union_result = set1.union(set2)     # {1, 2, 3, 4, 5, 6}
```

#### Intersection (&)
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Intersection - common elements
intersection_result = set1 & set2            # {3, 4}
# or
intersection_result = set1.intersection(set2) # {3, 4}
```

#### Difference (-)
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Difference - elements in set1 but not in set2
difference_result = set1 - set2           # {1, 2}
# or
difference_result = set1.difference(set2) # {1, 2}
```

#### Symmetric Difference (^)
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Symmetric difference - elements in either set, but not both
sym_diff_result = set1 ^ set2                      # {1, 2, 5, 6}
# or
sym_diff_result = set1.symmetric_difference(set2)  # {1, 2, 5, 6}
```

### Set Methods and Functions
```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}
set3 = {1, 2}

# Check if subset
print(set3.issubset(set1))    # True
print(set1.issuperset(set3))  # True

# Check if disjoint (no common elements)
print(set1.isdisjoint({5, 6}))  # True

# Length
print(len(set1))  # 3

# Membership
print(2 in set1)     # True
print(5 not in set1) # True

# Convert to other types
set_list = list(set1)
set_tuple = tuple(set1)
```

---

## Dictionary Structure

### Creating Dictionaries
```python
# Empty dictionary
empty_dict = {}
empty_dict2 = dict()

# Dictionary with elements
person = {"name": "Alice", "age": 30, "city": "New York"}
grades = {"math": 95, "science": 87, "english": 92}

# Using dict() constructor
person2 = dict(name="Bob", age=25, city="London")

# From list of tuples
items = [("a", 1), ("b", 2), ("c", 3)]
dict_from_list = dict(items)  # {'a': 1, 'b': 2, 'c': 3}
```

### Accessing Dictionary Values
```python
person = {"name": "Alice", "age": 30, "city": "New York"}

# Access using key
print(person["name"])     # Alice
print(person["age"])      # 30

# Access using get() method (safer)
print(person.get("name"))        # Alice
print(person.get("phone"))       # None
print(person.get("phone", "N/A")) # N/A (default value)

# Get all keys, values, items
print(person.keys())     # dict_keys(['name', 'age', 'city'])
print(person.values())   # dict_values(['Alice', 30, 'New York'])
print(person.items())    # dict_items([('name', 'Alice'), ('age', 30), ('city', 'New York')])
```

### Adding Values to Dictionary
```python
person = {"name": "Alice", "age": 30}

# Add new key-value pair
person["city"] = "New York"
person["phone"] = "123-456-7890"
print(person)  # {'name': 'Alice', 'age': 30, 'city': 'New York', 'phone': '123-456-7890'}

# Update existing value
person["age"] = 31
print(person)  # {'name': 'Alice', 'age': 31, 'city': 'New York', 'phone': '123-456-7890'}

# Update multiple values
person.update({"email": "alice@email.com", "country": "USA"})
print(person)
```

### Deleting from Dictionary
```python
person = {"name": "Alice", "age": 30, "city": "New York", "phone": "123-456-7890"}

# Delete specific key-value pair
del person["phone"]
print(person)  # {'name': 'Alice', 'age': 30, 'city': 'New York'}

# Remove and return value
age = person.pop("age")
print(f"Removed age: {age}")  # Removed age: 30
print(person)  # {'name': 'Alice', 'city': 'New York'}

# Remove and return arbitrary key-value pair
item = person.popitem()
print(f"Removed: {item}")  # Removed: ('city', 'New York')

# Clear all items
person.clear()
print(person)  # {}

# Delete entire dictionary
del person
```

### Properties of Dictionary Keys
1. **Unique**: No duplicate keys allowed
2. **Immutable**: Keys must be immutable (strings, numbers, tuples)
3. **Case-sensitive**: "Name" and "name" are different keys

```python
# Valid keys
valid_dict = {
    "name": "Alice",        # String key
    42: "answer",           # Integer key
    3.14: "pi",            # Float key
    (1, 2): "coordinate"   # Tuple key
}

# Invalid keys (would cause error)
# invalid_dict = {[1, 2]: "list key"}  # Lists are mutable
# invalid_dict = {{1, 2}: "set key"}   # Sets are mutable

# Duplicate keys (last value wins)
duplicate_keys = {"name": "Alice", "age": 30, "name": "Bob"}
print(duplicate_keys)  # {'name': 'Bob', 'age': 30}
```

### Built-in Dictionary Functions and Methods
```python
grades = {"math": 95, "science": 87, "english": 92, "history": 88}

# Length
print(len(grades))  # 4

# Check if key exists
print("math" in grades)      # True
print("art" not in grades)   # True

# Get all keys as list
keys_list = list(grades.keys())
print(keys_list)  # ['math', 'science', 'english', 'history']

# Get all values as list
values_list = list(grades.values())
print(values_list)  # [95, 87, 92, 88]

# Copy dictionary
grades_copy = grades.copy()

# Dictionary from keys
subjects = ["math", "science", "english"]
default_grades = dict.fromkeys(subjects, 0)
print(default_grades)  # {'math': 0, 'science': 0, 'english': 0}

# Set default value for key
grades.setdefault("art", 85)  # Adds art: 85 if not exists
print(grades)
```

### Dictionary Comprehensions
```python
# Create dictionary from range
squares = {x: x**2 for x in range(1, 6)}  # {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# Filter dictionary
grades = {"math": 95, "science": 87, "english": 92, "history": 78}
high_grades = {subject: grade for subject, grade in grades.items() if grade >= 90}
print(high_grades)  # {'math': 95, 'english': 92}

# Transform values
uppercase_grades = {subject.upper(): grade for subject, grade in grades.items()}
print(uppercase_grades)  # {'MATH': 95, 'SCIENCE': 87, 'ENGLISH': 92, 'HISTORY': 78}
```

### Nested Dictionaries
```python
students = {
    "student1": {"name": "Alice", "age": 20, "grades": {"math": 95, "science": 87}},
    "student2": {"name": "Bob", "age": 22, "grades": {"math": 88, "science": 92}}
}

# Access nested values
print(students["student1"]["name"])              # Alice
print(students["student1"]["grades"]["math"])    # 95

# Add to nested dictionary
students["student1"]["grades"]["english"] = 90
print(students["student1"]["grades"])  # {'math': 95, 'science': 87, 'english': 90}
```

---

## Function Operations

### Defining Functions
```python
# Basic function
def greet():
    print("Hello, World!")

# Call the function
greet()  # Output: Hello, World!

# Function with parameters
def greet_person(name):
    print(f"Hello, {name}!")

greet_person("Alice")  # Output: Hello, Alice!

# Function with return value
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3)
print(result)  # Output: 8
```

### Function Arguments

#### Default Arguments
```python
def greet(name, message="Hello"):
    print(f"{message}, {name}!")

greet("Alice")              # Hello, Alice!
greet("Bob", "Good morning") # Good morning, Bob!
```

#### Keyword Arguments
```python
def introduce(name, age, city):
    print(f"Name: {name}, Age: {age}, City: {city}")

# Positional arguments
introduce("Alice", 25, "New York")

# Keyword arguments
introduce(city="London", name="Bob", age=30)

# Mixed (positional first, then keyword)
introduce("Charlie", age=35, city="Paris")
```

#### Variable-length Arguments (*args)
```python
def calculate_sum(*numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(calculate_sum(1, 2, 3))        # 6
print(calculate_sum(1, 2, 3, 4, 5))  # 15
```

#### Keyword Variable-length Arguments (**kwargs)
```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25, city="New York")
# Output:
# name: Alice
# age: 25
# city: New York
```

#### All Types Together
```python
def complex_function(required, default="default", *args, **kwargs):
    print(f"Required: {required}")
    print(f"Default: {default}")
    print(f"Args: {args}")
    print(f"Kwargs: {kwargs}")

complex_function("must_have", "changed", 1, 2, 3, name="Alice", age=25)
```

### Library vs User-defined Functions

#### Built-in/Library Functions
```python
# Built-in functions
print(len("Hello"))      # 5
print(max([1, 5, 3]))    # 5
print(abs(-10))          # 10

# Math library functions
import math
print(math.sqrt(16))     # 4.0
print(math.pi)           # 3.141592653589793

# Random library functions
import random
print(random.randint(1, 10))    # Random number between 1 and 10
print(random.choice(['a', 'b', 'c']))  # Random choice
```

#### User-defined Functions
```python
def calculate_area(length, width):
    """Calculate area of rectangle"""
    return length * width

def is_even(number):
    """Check if number is even"""
    return number % 2 == 0

# Usage
area = calculate_area(10, 5)
print(f"Area: {area}")        # Area: 50
print(is_even(4))             # True
print(is_even(7))             # False
```

### Passing by Reference vs Passing by Value
```python
# Immutable objects (numbers, strings, tuples) - Pass by Value
def modify_number(x):
    x = x + 10
    print(f"Inside function: {x}")

num = 5
modify_number(num)
print(f"Outside function: {num}")  # Original value unchanged
# Output:
# Inside function: 15
# Outside function: 5

# Mutable objects (lists, dictionaries) - Pass by Reference
def modify_list(lst):
    lst.append(4)
    print(f"Inside function: {lst}")

my_list = [1, 2, 3]
modify_list(my_list)
print(f"Outside function: {my_list}")  # Original list modified
# Output:
# Inside function: [1, 2, 3, 4]
# Outside function: [1, 2, 3, 4]
```

### Lambda Functions
```python
# Basic lambda function
square = lambda x: x ** 2
print(square(5))  # 25

# Lambda with multiple arguments
add = lambda x, y: x + y
print(add(3, 5))  # 8

# Lambda with conditions
max_value = lambda a, b: a if a > b else b
print(max_value(10, 15))  # 15

# Lambda with built-in functions
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # [1, 4, 9, 16, 25]

evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)    # [2, 4]
```

### Date and Time Functions
```python
import datetime

# Current date and time
now = datetime.datetime.now()
print(f"Current date and time: {now}")

# Current date
today = datetime.date.today()
print(f"Today's date: {today}")

# Format date and time
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print(f"Formatted: {formatted_date}")

# Create specific date
specific_date = datetime.date(2024, 12, 25)
print(f"Christmas 2024: {specific_date}")

# Date arithmetic
import datetime
today = datetime.date.today()
tomorrow = today + datetime.timedelta(days=1)
last_week = today - datetime.timedelta(weeks=1)

print(f"Today: {today}")
print(f"Tomorrow: {tomorrow}")
print(f"Last week: {last_week}")

# Time functions
import time
print(f"Current timestamp: {time.time()}")
time.sleep(1)  # Sleep for 1 second
print("Woke up after 1 second")
```

### Scope and Local/Global Variables
```python
# Global variable
global_var = "I'm global"

def test_scope():
    # Local variable
    local_var = "I'm local"
    print(f"Inside function - Global: {global_var}")
    print(f"Inside function - Local: {local_var}")

test_scope()
print(f"Outside function - Global: {global_var}")
# print(local_var)  # This would cause an error

# Modifying global variable
counter = 0

def increment():
    global counter
    counter += 1

print(f"Before: {counter}")  # 0
increment()
print(f"After: {counter}")   # 1
```

---

## File Operations

### File Opening Modes
```python
# File opening modes:
# 'r'  - Read (default)
# 'w'  - Write (overwrites existing file)
# 'a'  - Append
# 'x'  - Exclusive creation (fails if file exists)
# 'b'  - Binary mode (rb, wb, ab)
# 't'  - Text mode (default)
# '+'  - Read and write (r+, w+, a+)
```

### Opening and Closing Files
```python
# Method 1: Manual open and close
file = open("example.txt", "r")
content = file.read()
file.close()

# Method 2: Using with statement (recommended)
with open("example.txt", "r") as file:
    content = file.read()
# File automatically closed after with block
```

### Reading Files
```python
# Read entire file
with open("data.txt", "r") as file:
    content = file.read()
    print(content)

# Read line by line
with open("data.txt", "r") as file:
    for line in file:
        print(line.strip())  # strip() removes newline characters

# Read all lines into a list
with open("data.txt", "r") as file:
    lines = file.readlines()
    for line in lines:
        print(line.strip())

# Read one line at a time
with open("data.txt", "r") as file:
    first_line = file.readline()
    second_line = file.readline()
    print(f"First: {first_line.strip()}")
    print(f"Second: {second_line.strip()}")

# Read specific number of characters
with open("data.txt", "r") as file:
    chunk = file.read(10)  # Read first 10 characters
    print(chunk)
```

### Writing Files
```python
# Write to file (overwrites existing content)
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new line.\n")

# Write multiple lines
lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
with open("output.txt", "w") as file:
    file.writelines(lines)

# Append to file
with open("output.txt", "a") as file:
    file.write("This line is appended.\n")

# Write with print function
with open("output.txt", "w") as file:
    print("Hello, World!", file=file)
    print("Another line", file=file)
```

### File Operations Examples

#### Copy File Content
```python
def copy_file(source, destination):
    try:
        with open(source, "r") as src_file:
            with open(destination, "w") as dest_file:
                content = src_file.read()
                dest_file.write(content)
        print(f"File copied from {source} to {destination}")
    except FileNotFoundError:
        print(f"Source file {source} not found")
    except Exception as e:
        print(f"Error occurred: {e}")

copy_file("input.txt", "output.txt")
```

#### Count Words in File
```python
def count_words(filename):
    try:
        with open(filename, "r") as file:
            content = file.read()
            words = content.split()
            return len(words)
    except FileNotFoundError:
        print(f"File {filename} not found")
        return 0

word_count = count_words("document.txt")
print(f"Word count: {word_count}")
```

#### Read CSV File
```python
def read_csv(filename):
    try:
        with open(filename, "r") as file:
            for line in file:
                data = line.strip().split(",")
                print(data)
    except FileNotFoundError:
        print(f"File {filename} not found")

# Create sample CSV
with open("students.csv", "w") as file:
    file.write("Name,Age,Grade\n")
    file.write("Alice,20,A\n")
    file.write("Bob,22,B\n")
    file.write("Charlie,21,A\n")

print("Reading CSV file:")
read_csv("students.csv")
```

#### Write Log File
```python
import datetime

def write_log(message):
    timestamp = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    log_entry = f"[{timestamp}] {message}\n"
    
    with open("application.log", "a") as log_file:
        log_file.write(log_entry)

# Usage
write_log("Application started")
write_log("User logged in")
write_log("Data processed successfully")
```

#### File Statistics
```python
import os

def file_statistics(filename):
    try:
        # Check if file exists
        if not os.path.exists(filename):
            print(f"File {filename} does not exist")
            return
        
        # File size
        size = os.path.getsize(filename)
        print(f"File size: {size} bytes")
        
        # Line and word count
        with open(filename, "r") as file:
            lines = file.readlines()
            line_count = len(lines)
            word_count = sum(len(line.split()) for line in lines)
            char_count = sum(len(line) for line in lines)
        
        print(f"Lines: {line_count}")
        print(f"Words: {word_count}")
        print(f"Characters: {char_count}")
        
    except Exception as e:
        print(f"Error: {e}")

file_statistics("example.txt")
```

### Error Handling with Files
```python
def safe_file_operation(filename):
    try:
        with open(filename, "r") as file:
            content = file.read()
            return content
    except FileNotFoundError:
        print(f"Error: File '{filename}' not found")
        return None
    except PermissionError:
        print(f"Error: Permission denied to read '{filename}'")
        return None
    except IOError:
        print(f"Error: Could not read file '{filename}'")
        return None
    except Exception as e:
        print(f"Unexpected error: {e}")
        return None

# Usage
content = safe_file_operation("data.txt")
if content:
    print("File read successfully")
else:
    print("Failed to read file")
```

---

## Practical Programming Examples

### Example 1: Student Grade Management System
```python
def grade_management_system():
    students = {}
    
    while True:
        print("\n--- Student Grade Management ---")
        print("1. Add student")
        print("2. Add grade")
        print("3. Calculate average")
        print("4. Display all students")
        print("5. Exit")
        
        choice = input("Enter your choice: ")
        
        if choice == "1":
            name = input("Enter student name: ")
            students[name] = []
            print(f"Student {name} added successfully")
            
        elif choice == "2":
            name = input("Enter student name: ")
            if name in students:
                try:
                    grade = float(input("Enter grade: "))
                    students[name].append(grade)
                    print(f"Grade {grade} added for {name}")
                except ValueError:
                    print("Invalid grade. Please enter a number.")
            else:
                print("Student not found")
                
        elif choice == "3":
            name = input("Enter student name: ")
            if name in students and students[name]:
                average = sum(students[name]) / len(students[name])
                print(f"{name}'s average: {average:.2f}")
            else:
                print("Student not found or no grades available")
                
        elif choice == "4":
            for name, grades in students.items():
                if grades:
                    average = sum(grades) / len(grades)
                    print(f"{name}: Grades = {grades}, Average = {average:.2f}")
                else:
                    print(f"{name}: No grades")
                    
        elif choice == "5":
            break
        else:
            print("Invalid choice")

# Uncomment to run
# grade_management_system()
```

### Example 2: Simple Calculator with Functions
```python
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero"
    return x / y

def calculator():
    operations = {
        '1': ('Add', add),
        '2': ('Subtract', subtract),
        '3': ('Multiply', multiply),
        '4': ('Divide', divide)
    }
    
    while True:
        print("\n--- Simple Calculator ---")
        for key, (name, _) in operations.items():
            print(f"{key}. {name}")
        print("5. Exit")
        
        choice = input("Enter choice: ")
        
        if choice == '5':
            break
            
        if choice in operations:
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
                
                operation_name, operation_func = operations[choice]
                result = operation_func(num1, num2)
                
                print(f"Result: {num1} {operation_name.lower()} {num2} = {result}")
                
            except ValueError:
                print("Invalid input. Please enter numbers only.")
        else:
            print("Invalid choice")

# Uncomment to run
# calculator()
```

### Example 3: Text File Analyzer
```python
def analyze_text_file(filename):
    """Analyze a text file and provide statistics"""
    try:
        with open(filename, 'r') as file:
            content = file.read()
            
        # Basic statistics
        lines = content.split('\n')
        words = content.split()
        characters = len(content)
        characters_no_spaces = len(content.replace(' ', ''))
        
        # Word frequency
        word_freq = {}
        for word in words:
            word = word.lower().strip('.,!?";')
            word_freq[word] = word_freq.get(word, 0) + 1
        
        # Find most common word
        most_common = max(word_freq, key=word_freq.get) if word_freq else "None"
        
        # Results
        print(f"File Analysis: {filename}")
        print("-" * 30)
        print(f"Lines: {len(lines)}")
        print(f"Words: {len(words)}")
        print(f"Characters (with spaces): {characters}")
        print(f"Characters (without spaces): {characters_no_spaces}")
        print(f"Most common word: '{most_common}' ({word_freq.get(most_common, 0)} times)")
        
        # Save analysis to file
        with open(f"{filename}_analysis.txt", 'w') as output:
            output.write(f"Analysis of {filename}\n")
            output.write("=" * 40 + "\n")
            output.write(f"Lines: {len(lines)}\n")
            output.write(f"Words: {len(words)}\n")
            output.write(f"Characters: {characters}\n")
            output.write(f"Most common word: {most_common}\n\n")
            output.write("Word Frequency:\n")
            for word, count in sorted(word_freq.items()):
                output.write(f"{word}: {count}\n")
        
        print(f"Analysis saved to {filename}_analysis.txt")
        
    except FileNotFoundError:
        print(f"File {filename} not found")
    except Exception as e:
        print(f"Error analyzing file: {e}")

# Example usage
sample_text = """
Python is a powerful programming language.
It is easy to learn and widely used.
Python has many libraries and frameworks.
Learning Python opens many opportunities.
"""

# Create sample file
with open("sample.txt", "w") as f:
    f.write(sample_text)

# Analyze the file
analyze_text_file("sample.txt")
```

---

## Final Project Ideas

### 1. Personal Expense Tracker
Create a program that:
- Stores expenses in a file
- Categorizes expenses (food, transport, entertainment, etc.)
- Calculates monthly totals
- Shows spending patterns
- Allows adding, editing, deleting expenses

### 2. Simple Library Management System
Features to implement:
- Book database (title, author, ISBN, availability)
- Member registration
- Book borrowing and returning
- Search functionality
- Due date tracking
- Fine calculation

### 3. Quiz Application
Create a quiz system that:
- Loads questions from a file
- Tracks scores
- Supports multiple choice questions
- Shows results and correct answers
- Saves high scores

### 4. Contact Manager
Build an application to:
- Store contact information
- Search contacts by name, phone, email
- Export contacts to CSV
- Import contacts from file
- Backup and restore functionality

Remember to practice these concepts regularly and build small projects to reinforce your learning. Good luck with your Python programming course!
