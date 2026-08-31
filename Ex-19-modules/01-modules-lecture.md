# Modules: Organizing Code - Lecture (DEEP)

## Why This Matters

As programs grow, files become huge and messy.

**Modules** let you organize code into files by purpose:

```
math_utils.py      # Math functions
string_utils.py    # String functions
database.py        # Database operations
```

Then use them:

```python
from math_utils import calculate_average
average = calculate_average([85, 92, 88])
```

Organized. Reusable. Professional.

## The Mental Model: What Is a Module?

A module is a Python file with code you can import.

```python
# utils.py
def helper():
    return "Help"

# main.py
from utils import helper
result = helper()
```

When you import, the module's code runs.

## The Mental Model: Importing

Three ways:

**Import entire module:**
```python
import math
print(math.sqrt(16))
```

**Import specific item:**
```python
from math import sqrt
print(sqrt(16))
```

**Import with alias:**
```python
from math import sqrt as square_root
print(square_root(16))
```

## The Mental Model: Standard Library

Python comes with many modules:

```python
import math       # Math functions
import random     # Random values
import datetime   # Date and time
import os         # File system
```

No installation needed. Just import.

## The Mental Model: Packages

**Package** - folder of modules

```
my_project/
├── utils/
│   ├── __init__.py
│   ├── math_utils.py
│   └── string_utils.py
└── main.py
```

Import from package:

```python
from utils.math_utils import calculate
```

## Common Confusion Points

**"Why use modules?"**

Organize large projects. Reuse code.

---

**"What's a package?"**

Folder of modules. Used for organization.

---

## Summary

Modules organize code into files.

Import modules to use their code.

Standard library provides ready-to-use modules.

Packages organize modules into folders.

Professional organization.

---

END OF LECTURE
