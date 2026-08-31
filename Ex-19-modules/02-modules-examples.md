# Modules: Examples & Demos

## Example 1: Create and Import Module

**math_utils.py:**
```python
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b
```

**main.py:**
```python
from math_utils import add, multiply

result1 = add(5, 3)
result2 = multiply(5, 3)

print("Add:", result1)
print("Multiply:", result2)
```

**Output:**
```
Add: 8
Multiply: 15
```

**Key insight:** Import functions from module and use them.

---

## Example 2: Import Entire Module

**greetings.py:**
```python
def greet_english(name):
    print(f"Hello, {name}!")

def greet_spanish(name):
    print(f"¡Hola, {name}!")
```

**main.py:**
```python
import greetings

greetings.greet_english("Alice")
greetings.greet_spanish("Bob")
```

**Output:**
```
Hello, Alice!
¡Hola, Bob!
```

**Key insight:** Import module name and use with dot notation.

---

## Example 3: Import with Alias

**calculator.py:**
```python
def add(a, b): return a + b
def subtract(a, b): return a - b
def multiply(a, b): return a * b
def divide(a, b): return a / b
```

**main.py:**
```python
from calculator import add as plus, multiply as times

print(plus(10, 5))
print(times(10, 5))
```

**Output:**
```
15
50
```

**Key insight:** Alias shortens names or avoids conflicts.

---

## Example 4: Using Standard Library - Math

**Code:**
```python
import math

print("Square root of 16:", math.sqrt(16))
print("Pi:", math.pi)
print("Sine of pi/2:", math.sin(math.pi / 2))
print("Ceiling of 4.3:", math.ceil(4.3))
```

**Output:**
```
Square root of 16: 4.0
Pi: 3.141592653589793
Sine of pi/2: 1.0
Ceiling of 4.3: 5
```

**Key insight:** Standard library provides ready-to-use functions.

---

## Example 5: Using Standard Library - Random

**Code:**
```python
import random

# Random integer
print("Random 1-10:", random.randint(1, 10))

# Random from list
colors = ["red", "green", "blue"]
print("Random color:", random.choice(colors))

# Shuffle list
numbers = [1, 2, 3, 4, 5]
random.shuffle(numbers)
print("Shuffled:", numbers)
```

**Output:**
```
Random 1-10: 7
Random color: blue
Shuffled: [3, 1, 5, 2, 4]
```

**Key insight:** Random module for generating random values.

---

## Example 6: Using Standard Library - DateTime

**Code:**
```python
import datetime

# Current date and time
now = datetime.datetime.now()
print("Now:", now)

# Date only
today = datetime.date.today()
print("Today:", today)

# Time difference
future = now + datetime.timedelta(days=7)
print("In 7 days:", future)
```

**Output:**
```
Now: 2024-08-30 15:30:45.123456
Today: 2024-08-30
In 7 days: 2024-09-06 15:30:45.123456
```

**Key insight:** DateTime for working with dates and times.

---

## Example 7: Using Standard Library - OS

**Code:**
```python
import os

# Current directory
print("Current dir:", os.getcwd())

# List files
print("Files:", os.listdir("."))

# Check if exists
print("main.py exists:", os.path.exists("main.py"))
```

**Output:**
```
Current dir: /home/user/project
Files: ['main.py', 'utils.py', 'data.txt']
main.py exists: True
```

**Key insight:** OS module for file system operations.

---

## Example 8: Module with Constants

**config.py:**
```python
DATABASE_URL = "postgresql://localhost"
API_KEY = "secret123"
MAX_RETRIES = 3
DEBUG = True
```

**main.py:**
```python
from config import DATABASE_URL, MAX_RETRIES

print("Database:", DATABASE_URL)
print("Max retries:", MAX_RETRIES)
```

**Output:**
```
Database: postgresql://localhost
Max retries: 3
```

**Key insight:** Modules can store constants.

---

## Example 9: Module with Classes

**student.py:**
```python
class Student:
    def __init__(self, name, grade):
        self.name = name
        self.grade = grade
    
    def info(self):
        return f"{self.name}: {self.grade}"
```

**main.py:**
```python
from student import Student

alice = Student("Alice", "A")
bob = Student("Bob", "B")

print(alice.info())
print(bob.info())
```

**Output:**
```
Alice: A
Bob: B
```

**Key insight:** Modules can contain classes.

---

## Example 10: Multi-file Organization

**utils/math_utils.py:**
```python
def calculate_tax(amount, rate=0.1):
    return amount * rate

def calculate_discount(amount, discount_percent):
    return amount * (discount_percent / 100)
```

**utils/string_utils.py:**
```python
def format_currency(amount):
    return f"${amount:.2f}"

def capitalize_words(text):
    return text.title()
```

**main.py:**
```python
from utils.math_utils import calculate_tax, calculate_discount
from utils.string_utils import format_currency

price = 100
tax = calculate_tax(price)
discount = calculate_discount(price, 10)

print("Price:", format_currency(price))
print("Tax:", format_currency(tax))
print("After discount:", format_currency(price - discount))
```

**Output:**
```
Price: $100.00
Tax: $10.00
After discount: $90.00
```

**Key insight:** Organize modules in subdirectories.

---

## Example 11: Module with Main Guard

**utilities.py:**
```python
def add(a, b):
    return a + b

if __name__ == "__main__":
    # This only runs if utilities.py is run directly
    print(add(5, 3))
```

**main.py:**
```python
from utilities import add

print("From main:", add(10, 20))
```

**Output:**
```
From main: 30
```

**Key insight:** `if __name__ == "__main__"` prevents running on import.

---

## Example 12: Check Module Documentation

**Code:**
```python
import math

# Get list of functions in math
print(dir(math))

# Get help on sqrt
help(math.sqrt)
```

**Output:**
```
['__doc__', '__name__', ..., 'acos', 'asin', ..., 'sqrt', ...]
Help on built-in function sqrt in module math:
sqrt(x, /)
    Return the square root of x.
```

**Key insight:** dir() and help() explore modules.

---

## Example 13: Import from Standard Library

**Code:**
```python
from collections import Counter
from itertools import combinations

# Counter
items = ["a", "b", "a", "c", "b", "a"]
count = Counter(items)
print("Count:", count)

# Combinations
nums = [1, 2, 3]
combos = list(combinations(nums, 2))
print("Combinations:", combos)
```

**Output:**
```
Count: Counter({'a': 3, 'b': 2, 'c': 1})
Combinations: [(1, 2), (1, 3), (2, 3)]
```

**Key insight:** Standard library has many useful utilities.

---

## Example 14: Import Multiple from Module

**Code:**
```python
from math import sqrt, pi, sin, cos

print("sqrt(16):", sqrt(16))
print("pi:", pi)
print("sin(pi/2):", sin(pi / 2))
print("cos(0):", cos(0))
```

**Output:**
```
sqrt(16): 4.0
pi: 3.141592653589793
sin(pi/2): 1.0
cos(0): 1.0
```

**Key insight:** Import multiple items from same module.

---

## Example 15: Real-World - Application Structure

**config.py:**
```python
DATABASE_URL = "sqlite:///app.db"
DEBUG = True
MAX_USERS = 1000
```

**models/user.py:**
```python
class User:
    def __init__(self, name, email):
        self.name = name
        self.email = email
```

**utils/validators.py:**
```python
def is_valid_email(email):
    return "@" in email and "." in email.split("@")[1]
```

**main.py:**
```python
from config import DATABASE_URL, DEBUG
from models.user import User
from utils.validators import is_valid_email

user = User("Alice", "alice@example.com")
print("Valid email:", is_valid_email(user.email))
print("Database:", DATABASE_URL)
```

**Output:**
```
Valid email: True
Database: sqlite:///app.db
```

**Key insight:** Real applications organize code across modules.

---

## Summary of Examples

- Create and import modules
- Import entire module
- Import with aliases
- Use standard library (math, random, datetime, os)
- Store constants in modules
- Store classes in modules
- Organize across multiple files
- Use __name__ guard
- Explore modules with dir() and help()
- Import multiple items
- Real-world application structure

Next: practice with exercises.
