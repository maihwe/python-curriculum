# Modules: Exercises & Practice

## Exercise 1: Create Simple Module

Create a module with helper functions.

**math_helpers.py:**
```python
def add(a, b): return a + b
def subtract(a, b): return a - b
```

**main.py:**
```python
from math_helpers import add, subtract
print(add(10, 5))
print(subtract(10, 5))
```

**Expected output:**
```
15
5
```

**What to do:**
1. Create math_helpers.py with two functions
2. Create main.py that imports and uses them
3. Run main.py
4. Should print results

**Hint:** Same file structure as examples.

---

## Exercise 2: Import Entire Module

Create module and import whole module.

**What to do:**
1. Create greetings.py with greet_english() and greet_spanish()
2. Create main.py that imports entire greetings module
3. Call both functions using module.function() syntax
4. Run it

**Expected output:**
```
Hello, World!
¡Hola, Mundo!
```

**Hint:** `import greetings` then `greetings.greet_english()`

---

## Exercise 3: Use Standard Library - Math

Use math module.

**Expected output:**
```
sqrt(16) = 4.0
pi = 3.14159...
```

**What to do:**
1. Create file using_math.py
2. Import math module
3. Calculate sqrt(16)
4. Print pi
5. Run it

**Hint:** `import math` then `math.sqrt()`

---

## Exercise 4: Use Standard Library - Random

Use random module.

**Expected output (sample):**
```
Random 1-100: 42
Random choice: blue
```

**What to do:**
1. Create file using_random.py
2. Generate random integer 1-100
3. Choose random item from list
4. Print both
5. Run it

**Hint:** `random.randint()` and `random.choice()`

---

## Exercise 5: Use Standard Library - DateTime

Use datetime module.

**Expected output (sample):**
```
Today: 2024-08-30
In 7 days: 2024-09-06
```

**What to do:**
1. Create file using_datetime.py
2. Get today's date
3. Calculate date 7 days from now
4. Print both
5. Run it

**Hint:** `datetime.date.today()` and `timedelta(days=7)`

---

## Exercise 6: Module with Constants

Create config module.

**config.py:**
```python
APP_NAME = "MyApp"
VERSION = "1.0"
DEBUG = True
```

**main.py:**
```python
from config import APP_NAME, VERSION
print(f"{APP_NAME} v{VERSION}")
```

**What to do:**
1. Create config.py with constants
2. Create main.py that imports and uses them
3. Run it

**Expected output:**
```
MyApp v1.0
```

**Hint:** Just store variables in module.

---

## Exercise 7: Module with Class

Create module containing a class.

**person.py:**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def info(self):
        return f"{self.name} ({self.age})"
```

**main.py:**
```python
from person import Person
p = Person("Alice", 25)
print(p.info())
```

**What to do:**
1. Create person.py with Person class
2. Create main.py that imports and uses it
3. Run it

**Expected output:**
```
Alice (25)
```

**Hint:** Classes can be in modules too.

---

## Exercise 8: Use OS Module

Use os module to explore file system.

**Expected output (sample):**
```
Current directory: /home/user/project
Files: ['main.py', 'utils.py']
```

**What to do:**
1. Create file using_os.py
2. Print current directory
3. List files in current directory
4. Run it

**Hint:** `os.getcwd()` and `os.listdir()`

---

## Exercise 9: Import with Alias

Use import aliases to avoid conflicts.

**calculator.py:**
```python
def add(a, b): return a + b
def multiply(a, b): return a * b
```

**main.py:**
```python
from calculator import add as plus, multiply as times
print(plus(5, 3))
print(times(5, 3))
```

**What to do:**
1. Create calculator.py
2. Create main.py using aliases
3. Run it

**Expected output:**
```
8
15
```

**Hint:** `from module import func as alias`

---

## Exercise 10: Multiple Imports from Module

Import multiple items from same module.

**Expected output:**
```
sqrt(16) = 4.0
sin(pi/2) = 1.0
```

**What to do:**
1. Create file using_math_multiple.py
2. Import sqrt and sin and pi from math
3. Calculate and print results
4. Run it

**Hint:** `from math import sqrt, sin, pi`

---

## Exercise 11: Organize Code in Subdirectory

Create module structure with subdirectory.

**utils/string_utils.py:**
```python
def reverse(text):
    return text[::-1]

def uppercase(text):
    return text.upper()
```

**main.py:**
```python
from utils.string_utils import reverse, uppercase
print(reverse("hello"))
print(uppercase("hello"))
```

**What to do:**
1. Create utils/ folder
2. Create string_utils.py inside
3. Create main.py that imports from utils
4. Run it

**Expected output:**
```
olleh
HELLO
```

**Hint:** Create folder first, then __init__.py

---

## Exercise 12: Module Exploration with dir()

Explore a module using dir().

**Expected output (sample):**
```
Math module has: acos, asin, atan, ...
```

**What to do:**
1. Create file explore_module.py
2. Import math
3. Use dir(math) to list contents
4. Print first few items
5. Run it

**Hint:** `dir(module)` returns list of contents.

---

## Exercise 13: Real-World - Config Pattern

Create real app structure with config.

**config.py:**
```python
DB_URL = "sqlite:///app.db"
APP_NAME = "MyApp"
DEBUG = True
```

**models.py:**
```python
class User:
    def __init__(self, name):
        self.name = name
```

**main.py:**
```python
from config import APP_NAME, DB_URL
from models import User

user = User("Alice")
print(f"{APP_NAME}: {user.name}")
print(f"Database: {DB_URL}")
```

**What to do:**
1. Create config.py
2. Create models.py
3. Create main.py
4. Run main.py

**Expected output:**
```
MyApp: Alice
Database: sqlite:///app.db
```

**Hint:** Typical app structure.

---

## Exercise 14: Real-World - Utilities Pattern

Create reusable utility modules.

**utils/validators.py:**
```python
def is_email_valid(email):
    return "@" in email

def is_strong_password(pwd):
    return len(pwd) >= 8
```

**main.py:**
```python
from utils.validators import is_email_valid, is_strong_password

print(is_email_valid("alice@example.com"))
print(is_strong_password("weak"))
print(is_strong_password("strongpass123"))
```

**What to do:**
1. Create utils folder
2. Create validators.py
3. Create main.py
4. Run it

**Expected output:**
```
True
False
True
```

**Hint:** Keep validators in separate module.

---

## Exercise 15: Real-World - Complete App

Build small app using modules.

**config.py:**
```python
# Configuration
DATABASE = "users.db"
```

**models.py:**
```python
class Contact:
    def __init__(self, name, phone):
        self.name = name
        self.phone = phone
```

**contacts.py:**
```python
# Simulated contact storage
contacts_list = []

def add_contact(contact):
    contacts_list.append(contact)

def list_contacts():
    return contacts_list
```

**main.py:**
```python
from config import DATABASE
from models import Contact
from contacts import add_contact, list_contacts

# Create contacts
alice = Contact("Alice", "555-1234")
bob = Contact("Bob", "555-5678")

add_contact(alice)
add_contact(bob)

# List contacts
for contact in list_contacts():
    print(f"{contact.name}: {contact.phone}")
```

**What to do:**
1. Create config.py
2. Create models.py
3. Create contacts.py
4. Create main.py
5. Run main.py

**Expected output:**
```
Alice: 555-1234
Bob: 555-5678
```

**Hint:** Separate concerns: config, models, logic, main.

---

## Checking Your Work

After exercises, ask yourself:

- ✓ Can I create modules?
- ✓ Can I import from modules?
- ✓ Do I understand file organization?
- ✓ Can I use standard library?
- ✓ Can I build multi-file apps?

---

## Key Concepts to Remember

**Module:**
- Python file with code
- Can contain functions, classes, variables

**Import:**
- `import module` - entire module
- `from module import item` - specific item
- `from module import item as alias` - with alias

**Standard Library:**
- math, random, datetime, os, etc.
- Available without installation

**Organization:**
- One purpose per module
- Group related code
- Use subdirectories for large projects

---

## Congratulations!

You've now completed ALL 19 topics of Python fundamentals!

**What you can build:**
✅ Console applications  
✅ Data processing programs  
✅ File handling systems  
✅ Object-oriented applications  
✅ Organized, professional code  

**You now have:**
✅ Complete understanding of Python basics
✅ Skills to solve real problems
✅ Knowledge to learn advanced topics
✅ Ability to write professional code

**Next:** Build projects, explore frameworks, contribute to open source.

**Keep coding. Keep learning. Keep growing.** 🚀

---

END OF CURRICULUM

You've completed:
- 19 comprehensive topics
- 240+ code examples
- 255+ practice exercises
- ~135,000 words of professional teaching content

This is your foundation. Build on it! 💪
