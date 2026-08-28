# File I/O: Examples & Demos

## Example 1: Write to File

**Code:**
```python
# Create file and write data
file = open("greeting.txt", "w")
file.write("Hello, World!")
file.close()

print("File created!")
```

**Output:**
```
File created!
```

**File contents (greeting.txt):**
```
Hello, World!
```

**Key insight:** Write mode creates file and saves data.

---

## Example 2: Read from File

**Code:**
```python
# First, create a file
file = open("greeting.txt", "w")
file.write("Hello, World!")
file.close()

# Now read it back
file = open("greeting.txt", "r")
data = file.read()
file.close()

print("Data from file:", data)
```

**Output:**
```
Data from file: Hello, World!
```

**Key insight:** Read mode retrieves data from file.

---

## Example 3: Write Multiple Lines

**Code:**
```python
file = open("students.txt", "w")
file.write("Alice\n")
file.write("Bob\n")
file.write("Charlie\n")
file.close()

file = open("students.txt", "r")
data = file.read()
file.close()

print(data)
```

**Output:**
```
Alice
Bob
Charlie
```

**Key insight:** \n adds newlines between entries.

---

## Example 4: Append to File

**Code:**
```python
# Create initial file
file = open("students.txt", "w")
file.write("Alice\n")
file.write("Bob\n")
file.close()

# Append new student
file = open("students.txt", "a")
file.write("Charlie\n")
file.close()

# Read all
file = open("students.txt", "r")
data = file.read()
file.close()

print(data)
```

**Output:**
```
Alice
Bob
Charlie
```

**Key insight:** Append preserves old data and adds new.

---

## Example 5: Read Line by Line

**Code:**
```python
# Create file
file = open("students.txt", "w")
file.write("Alice\nBob\nCharlie\n")
file.close()

# Read line by line
file = open("students.txt", "r")
line1 = file.readline()
line2 = file.readline()
line3 = file.readline()
file.close()

print("Line 1:", line1)
print("Line 2:", line2)
print("Line 3:", line3)
```

**Output:**
```
Line 1: Alice

Line 2: Bob

Line 3: Charlie

```

**Key insight:** readline() gets one line at a time (with \n).

---

## Example 6: Read All Lines as List

**Code:**
```python
# Create file
file = open("students.txt", "w")
file.write("Alice\nBob\nCharlie\n")
file.close()

# Read all lines into list
file = open("students.txt", "r")
lines = file.readlines()
file.close()

for i, line in enumerate(lines):
    print(f"Line {i}: {line}")
```

**Output:**
```
Line 0: Alice

Line 1: Bob

Line 2: Charlie

```

**Key insight:** readlines() returns list of all lines.

---

## Example 7: Using with Statement

**Code:**
```python
# Write with 'with' statement
with open("greeting.txt", "w") as file:
    file.write("Hello!")

# Read with 'with' statement
with open("greeting.txt", "r") as file:
    data = file.read()

print("Data:", data)
```

**Output:**
```
Data: Hello!
```

**Key insight:** 'with' auto-closes file. Cleaner code.

---

## Example 8: Write Numbers to File

**Code:**
```python
# Write numbers
numbers = [10, 20, 30, 40, 50]

with open("numbers.txt", "w") as file:
    for num in numbers:
        file.write(str(num) + "\n")

# Read back
with open("numbers.txt", "r") as file:
    data = file.read()

print(data)
```

**Output:**
```
10
20
30
40
50
```

**Key insight:** Must convert numbers to strings to write.

---

## Example 9: Save Dictionary to File

**Code:**
```python
person = {
    "name": "Alice",
    "age": 25,
    "job": "Engineer"
}

# Save to file
with open("person.txt", "w") as file:
    for key, value in person.items():
        file.write(key + ": " + str(value) + "\n")

# Read back
with open("person.txt", "r") as file:
    print(file.read())
```

**Output:**
```
name: Alice
age: 25
job: Engineer
```

**Key insight:** Dictionaries can be saved line by line.

---

## Example 10: Count Lines in File

**Code:**
```python
# Create file
with open("students.txt", "w") as file:
    file.write("Alice\nBob\nCharlie\nDavid\n")

# Count lines
with open("students.txt", "r") as file:
    lines = file.readlines()
    count = len(lines)

print("Total lines:", count)
```

**Output:**
```
Total lines: 4
```

**Key insight:** readlines() makes counting easy.

---

## Example 11: Remove Whitespace from Lines

**Code:**
```python
# Create file with extra spaces
with open("students.txt", "w") as file:
    file.write("  Alice  \n  Bob  \n  Charlie  \n")

# Read and clean
with open("students.txt", "r") as file:
    lines = file.readlines()

print("With whitespace:")
for line in lines:
    print(f"'{line}'")

print("\nCleaned:")
for line in lines:
    print(f"'{line.strip()}'")
```

**Output:**
```
With whitespace:
'  Alice  
'
'  Bob  
'
'  Charlie  
'

Cleaned:
'Alice'
'Bob'
'Charlie'
```

**Key insight:** .strip() removes leading/trailing spaces.

---

## Example 12: Process CSV Data

**Code:**
```python
# Create CSV file
with open("grades.csv", "w") as file:
    file.write("Alice,95\n")
    file.write("Bob,87\n")
    file.write("Charlie,92\n")

# Read and process CSV
with open("grades.csv", "r") as file:
    for line in file.readlines():
        name, grade = line.strip().split(",")
        print(f"{name}: {grade}%")
```

**Output:**
```
Alice: 95%
Bob: 87%
Charlie: 92%
```

**Key insight:** split() parses CSV data.

---

## Example 13: Append to Existing File

**Code:**
```python
# Create file
with open("log.txt", "w") as file:
    file.write("Program started\n")

# Add more entries
with open("log.txt", "a") as file:
    file.write("Processing data\n")
    file.write("Operation complete\n")

# Read all
with open("log.txt", "r") as file:
    print(file.read())
```

**Output:**
```
Program started
Processing data
Operation complete
```

**Key insight:** Append mode keeps old data, adds new.

---

## Example 14: Check If File Exists

**Code:**
```python
import os

filename = "students.txt"

if os.path.exists(filename):
    with open(filename, "r") as file:
        print("File exists! Contents:")
        print(file.read())
else:
    print("File doesn't exist yet")
```

**Output:**
```
File doesn't exist yet
```

**Key insight:** os.path.exists() checks if file exists.

---

## Example 15: Real-World - Simple Database

**Code:**
```python
# Save contacts
contacts = {
    "Alice": "alice@example.com",
    "Bob": "bob@example.com",
    "Charlie": "charlie@example.com"
}

with open("contacts.txt", "w") as file:
    for name, email in contacts.items():
        file.write(f"{name},{email}\n")

# Load contacts
loaded_contacts = {}
with open("contacts.txt", "r") as file:
    for line in file.readlines():
        name, email = line.strip().split(",")
        loaded_contacts[name] = email

print("Loaded contacts:")
for name, email in loaded_contacts.items():
    print(f"{name}: {email}")
```

**Output:**
```
Loaded contacts:
Alice: alice@example.com
Bob: bob@example.com
Charlie: charlie@example.com
```

**Key insight:** Files can store and restore dictionaries.

---

## Summary of Examples

- Create and read files
- Write multiple lines
- Append without deleting
- Read line by line
- Use 'with' statement
- Work with numbers
- Save dictionaries
- Process CSV data
- Check file existence
- Simple database system

Next: practice with exercises.
