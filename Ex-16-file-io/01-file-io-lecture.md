# File I/O: Reading and Writing Data - Lecture

## Why This Matters

So far, all your data disappears when the program ends:

```python
students = ["Alice", "Bob", "Charlie"]
print(students)  # Works
# Program ends
# Data is GONE forever
```

**File I/O** (Input/Output) lets you save data permanently to files.

```python
# Save to file
students = ["Alice", "Bob", "Charlie"]
file = open("students.txt", "w")
file.write(str(students))
file.close()

# Later, even after program ends:
file = open("students.txt", "r")
data = file.read()
print(data)  # "['Alice', 'Bob', 'Charlie']"
```

Data persists even when the program stops.

---

## The Mental Model: What Is a File?

A **file** is data stored on your computer's disk.

```
Your Computer
├── Documents/
│   ├── students.txt ← This is a file
│   ├── config.txt ← This is a file
│   └── data.csv ← This is a file
├── Pictures/
└── Desktop/
```

Files can contain:
- Text (students.txt, config.txt)
- Numbers (data.csv)
- Code (program.py)
- Anything

Your program can read files to get data, or write files to save data.

---

## The Mental Model: File Modes

When you open a file, you specify what you'll do:

```
"r" = Read mode (get data FROM file)
"w" = Write mode (put data INTO file)
"a" = Append mode (add data TO END of file)
```

**Read mode ("r"):**
```python
file = open("students.txt", "r")  # Open to read
data = file.read()                # Get data from file
```

**Write mode ("w"):**
```python
file = open("students.txt", "w")  # Open to write
file.write("Alice")               # Put data into file
```

**Append mode ("a"):**
```python
file = open("students.txt", "a")  # Open to append
file.write("\nBob")               # Add to end of file
```

---

## The Mental Model: File Lifecycle

Every file operation follows same steps:

```
1. OPEN   → Open the file
2. USE    → Read or write data
3. CLOSE  → Close the file
```

**Code example:**
```python
# Step 1: OPEN
file = open("students.txt", "r")

# Step 2: USE
data = file.read()

# Step 3: CLOSE
file.close()
```

Always close files when done. Leaving files open causes problems.

---

## The Mental Model: Reading Files

**Read entire file:**
```python
file = open("students.txt", "r")
all_data = file.read()  # Get EVERYTHING
file.close()
```

**Read line by line:**
```python
file = open("students.txt", "r")
line1 = file.readline()  # First line
line2 = file.readline()  # Second line
line3 = file.readline()  # Third line
file.close()
```

**Read all lines into list:**
```python
file = open("students.txt", "r")
all_lines = file.readlines()  # List of all lines
file.close()
```

---

## The Mental Model: Writing Files

**Write data to file:**
```python
file = open("students.txt", "w")
file.write("Alice\n")
file.write("Bob\n")
file.write("Charlie\n")
file.close()
```

**Important:** Write mode ("w") DELETES old content.

```python
file = open("students.txt", "w")  # File now empty!
file.write("New data")             # Only this remains
file.close()
```

---

## The Mental Model: Append Mode

**Append adds to end without deleting:**
```python
file = open("students.txt", "a")   # Append mode
file.write("David\n")              # Add to end
file.close()                        # Old data preserved
```

Use "a" when you want to keep old data AND add new data.

---

## The Mental Model: Context Managers (with statement)

Opening/closing manually is tedious:

```python
file = open("students.txt", "r")  # Must open
data = file.read()                 # Use
file.close()                       # Must close
```

**The `with` statement does it automatically:**

```python
with open("students.txt", "r") as file:
    data = file.read()  # File auto-closes here
```

Much cleaner. File automatically closes when block ends.

---

## Key Concepts to Remember

1. **File modes:** "r" (read), "w" (write), "a" (append)
2. **Open/Use/Close** file lifecycle
3. **read()** gets entire file
4. **readline()** gets one line
5. **readlines()** gets list of lines
6. **write()** puts data into file
7. **Append** adds to end without deleting
8. **with statement** auto-closes files
9. **File paths** can be relative or absolute
10. **Always close files** (or use with)

---

## Common Misconceptions

**"Write mode appends new data"**

No. Write mode deletes old content first.

**"I don't need to close files"**

Wrong. Unclosed files cause data loss and locks.

**"Reading and writing happen instantly"**

Partially. Data goes to buffer first, then disk on close.

**"File paths are always the same"**

No. Paths depend on computer. Use relative paths.

---

## Real-World Uses

**Reading configuration:**
```python
with open("config.txt", "r") as file:
    settings = file.read()
```

**Saving user data:**
```python
with open("user_data.txt", "w") as file:
    file.write("Alice, 25, Engineer")
```

**Logging program activity:**
```python
with open("log.txt", "a") as file:
    file.write("Program started at 10:30 AM\n")
```

**Processing CSV data:**
```python
with open("students.csv", "r") as file:
    for line in file.readlines():
        name, grade = line.split(",")
```

---

## Summary

**File I/O** lets you save and load data permanently.

**Three modes:**
- Read ("r") - get data from file
- Write ("w") - put data into file (deletes old)
- Append ("a") - add data to end (keeps old)

**Always close files** or use `with` statement.

Files are how real programs store persistent data.

Next: see files in action.
