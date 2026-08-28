# File I/O: Exercises & Practice

## Exercise 1: Write to File

Create a program that writes text to a file.

**Expected file contents (hello.txt):**
```
Hello, World!
```

**What to do:**
1. Create a file called `write_file.py`
2. Open file "hello.txt" in write mode
3. Write "Hello, World!"
4. Close file
5. Run it
6. Check that hello.txt was created

**Hint:** `file = open("hello.txt", "w")`

---

## Exercise 2: Read from File

Create a program that reads text from a file.

**Expected output:**
```
Hello, World!
```

**What to do:**
1. Create a file called `read_file.py`
2. First, create hello.txt (from Exercise 1)
3. Open and read the file
4. Print the data
5. Run it

**Hint:** `data = file.read()`

---

## Exercise 3: Write Multiple Lines

Create a program that writes multiple lines to file.

**Expected file contents (students.txt):**
```
Alice
Bob
Charlie
```

**What to do:**
1. Create a file called `write_lines.py`
2. Write 3 student names to students.txt
3. Use \n to separate lines
4. Run it
5. Check students.txt

**Hint:** Use `file.write(name + "\n")`

---

## Exercise 4: Read Multiple Lines

Create a program that reads lines from file.

**Expected output:**
```
Alice
Bob
Charlie
```

**What to do:**
1. Create a file called `read_lines.py`
2. Create students.txt first (Exercise 3)
3. Read the file
4. Print all data
5. Run it

**Hint:** `file.read()` gets everything.

---

## Exercise 5: Append to File

Create a program that adds data without deleting.

**Expected file contents:**
```
Alice
Bob
Charlie
David
```

**What to do:**
1. Create a file called `append_file.py`
2. Create students.txt with Alice, Bob, Charlie
3. Append "David\n"
4. Read and print all
5. Run it

**Hint:** Use append mode "a"

---

## Exercise 6: Using with Statement

Create a program using `with` statement.

**Expected output:**
```
Data: Hello!
```

**What to do:**
1. Create a file called `with_statement.py`
2. Write to file using `with`
3. Read from file using `with`
4. Print data
5. Run it

**Hint:** `with open(filename, mode) as file:`

---

## Exercise 7: Line by Line Processing

Create a program that processes each line.

**Expected output:**
```
Line 1: Alice
Line 2: Bob
Line 3: Charlie
```

**What to do:**
1. Create a file called `process_lines.py`
2. Create students.txt
3. Use readlines() to get all lines
4. Loop and print with line numbers
5. Run it

**Hint:** `readlines()` returns list of lines.

---

## Exercise 8: Count Lines

Create a program that counts lines in file.

**Expected output:**
```
Total lines: 3
```

**What to do:**
1. Create a file called `count_lines.py`
2. Create students.txt
3. Read lines using readlines()
4. Count them
5. Print count
6. Run it

**Hint:** `len(readlines())` gives count.

---

## Exercise 9: Strip Whitespace

Create a program that cleans up data from file.

**Expected output:**
```
Alice
Bob
Charlie
```

**What to do:**
1. Create a file called `strip_whitespace.py`
2. Create file with extra spaces: "  Alice  \n  Bob  \n"
3. Read lines
4. Use .strip() to remove spaces
5. Print cleaned data
6. Run it

**Hint:** `line.strip()` removes leading/trailing spaces.

---

## Exercise 10: Save and Load Numbers

Create a program that saves and loads numbers.

**Expected output:**
```
Numbers from file: [10, 20, 30]
```

**What to do:**
1. Create a file called `numbers_io.py`
2. Write 10, 20, 30 to file (one per line)
3. Read them back
4. Convert to integers
5. Store in list
6. Print list
7. Run it

**Hint:** `int(value)` converts string to number.

---

## Exercise 11: Save Dictionary

Create a program that saves dictionary to file.

**Expected file contents (person.txt):**
```
name: Alice
age: 25
job: Engineer
```

**What to do:**
1. Create a file called `save_dict.py`
2. Create dictionary with name, age, job
3. Write each key: value to file
4. Run it
5. Check person.txt

**Hint:** Loop through dictionary items.

---

## Exercise 12: Process CSV Data

Create a program that reads CSV and processes it.

**Expected output:**
```
Alice: 95%
Bob: 87%
Charlie: 92%
```

**What to do:**
1. Create a file called `process_csv.py`
2. Create grades.csv with "Alice,95" etc
3. Read file
4. Use split(",") to parse
5. Print formatted output
6. Run it

**Hint:** `line.strip().split(",")`

---

## Exercise 13: Real-World - Simple Log File

Create a program that logs program events.

**Expected file contents (log.txt):**
```
Program started
Processing data
Operation complete
```

**What to do:**
1. Create a file called `log_system.py`
2. Create/open log.txt in write mode
3. Write "Program started"
4. Close, reopen in append mode
5. Write "Processing data"
6. Close, reopen in append mode
7. Write "Operation complete"
8. Read and print entire log
9. Run it

**Hint:** Use append mode for subsequent writes.

---

## Exercise 14: Real-World - Student Grades Database

Create a program that saves and loads student grades.

**Expected output:**
```
Loaded students:
Alice: 95
Bob: 87
Charlie: 92
```

**What to do:**
1. Create a file called `grades_db.py`
2. Create dictionary with students and grades
3. Save to grades.txt (name: grade format)
4. Create new dictionary
5. Read from file and load into dictionary
6. Print loaded data
7. Run it

**Hint:** Use loop to read, split, and rebuild dictionary.

---

## Exercise 15: Real-World - Contact Manager

Create a program that manages contacts.

**Expected output:**
```
Saved 3 contacts
Loaded contacts:
Alice: alice@example.com
Bob: bob@example.com
Charlie: charlie@example.com
```

**What to do:**
1. Create a file called `contact_manager.py`
2. Create dictionary of contacts (name: email)
3. Save all contacts to contacts.txt
4. Load them back into new dictionary
5. Display loaded contacts
6. Run it

**Hint:** Format: "name,email" in file, split to rebuild dict.

---

## Checking Your Work

After exercises, ask yourself:

- ✓ Can I write to files?
- ✓ Can I read from files?
- ✓ Do I understand file modes?
- ✓ Can I use 'with' statement?
- ✓ Can I process file data?

---

## Key Concepts to Remember

**File Modes:**
- "r" = read (get data)
- "w" = write (put data, deletes old)
- "a" = append (add to end, keeps old)

**File Methods:**
- read() = all data
- readline() = one line
- readlines() = list of lines
- write() = put data

**Best Practice:**
- Use 'with' statement (auto-closes)
- Always close files
- Use .strip() to clean whitespace
- Use split() to parse data

**File Lifecycle:**
1. Open
2. Read or write
3. Close

---

## Next Steps

Once you've mastered file I/O:

1. You can persist data between runs
2. You can process real files
3. You're ready for error handling
4. You understand data storage

You're making excellent progress! 🎉

**15 core topics complete → Final advanced topics ahead!**

Next topic: **Topic 17: Error Handling** (try/except blocks)
