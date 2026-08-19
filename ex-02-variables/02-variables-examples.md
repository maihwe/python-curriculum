# Variables: Examples & Demos

## Example 1: Creating and Using a Simple Variable

**Code:**
```python
message = "Hello, Python!"
print(message)
```

**Execution flow:**

Line 1: Python creates a box labeled `message` and puts `"Hello, Python!"` inside

Line 2: Python looks inside the `message` box, finds `"Hello, Python!"`, and prints it

**Output:**
```
Hello, Python!
```

**Key insight:** The variable name is just a label. When you refer to it, Python retrieves what's inside.

---

## Example 2: Reusing Variables Multiple Times

Variables are powerful because you can use them multiple times without retyping the value.

**Code:**
```python
name = "Alice"
print(name)
print(name)
print(name)
```

**Execution flow:**

Line 1: Store `"Alice"` in the variable `name`

Line 2: Print what's in `name` → displays "Alice"

Line 3: Print what's in `name` → displays "Alice" again

Line 4: Print what's in `name` → displays "Alice" again

**Output:**
```
Alice
Alice
Alice
```

**Key insight:** You defined `name` once, but used it three times. You didn't have to type `"Alice"` three times. The variable saved you typing and made your code clearer.

---

## Example 3: Variables Store Different Types

**Code:**
```python
age = 25
price = 19.99
name = "Bob"
is_student = True

print(age)
print(price)
print(name)
print(is_student)
```

**Execution flow:**

Line 1: Store the number `25` in `age`

Line 2: Store the decimal `19.99` in `price`

Line 3: Store the text `"Bob"` in `name`

Line 4: Store the value `True` in `is_student`

Lines 5-8: Print each variable

**Output:**
```
25
19.99
Bob
True
```

**Key insight:** Variables aren't picky. They hold numbers, text, true/false—whatever you put in them.

---

## Example 4: Variables Change Over Time

**Code:**
```python
score = 0
print(score)

score = 50
print(score)

score = 100
print(score)
```

**Execution flow:**

Line 1: Create `score` with value `0`

Line 2: Print `score` → displays "0"

Line 3: Change `score` to `50` (the old value `0` is gone)

Line 4: Print `score` → displays "50"

Line 5: Change `score` to `100`

Line 6: Print `score` → displays "100"

**Output:**
```
0
50
100
```

**Key insight:** Each `=` assignment *replaces* the old value. The box is emptied and refilled. The old value is gone forever.

---

## Example 5: Using Variables in Print Statements

Here's something critical: when you use a variable in `print()`, Python doesn't print the variable *name*. It prints what's *inside* the variable.

**Code:**
```python
name = "Charlie"
age = 30

print(name)
print(age)
```

**Output:**
```
Charlie
30
```

NOT:
```
name
age
```

Python is smart: it sees `name` (no quotes) and thinks "Oh, this is a variable. Let me look up what's inside and print that."

---

## Example 6: Variable Names vs. Text

Compare: using a variable name (no quotes) vs. printing literal text (with quotes)

**Code:**
```python
name = "Charlie"

print(name)        # Variable - prints what's inside
print("name")      # Text - prints the word "name"
```

**Output:**
```
Charlie
name
```

**Key insight:** No quotes = Python looks it up. With quotes = Python treats it as literal text.

---

## Example 7: Multiple Variables Working Together

**Code:**
```python
first_name = "Alice"
last_name = "Johnson"
age = 28

print(first_name)
print(last_name)
print(age)
```

**Execution flow:**

Line 1: Store `"Alice"` in `first_name`

Line 2: Store `"Johnson"` in `last_name`

Line 3: Store `28` in `age`

Lines 4-6: Print each variable

**Output:**
```
Alice
Johnson
28
```

**Key insight:** You can have as many variables as you need. Each one is a separate box with its own label.

---

## Example 8: Reusing and Changing Variables

**Code:**
```python
points = 0
print("Starting points:", points)

points = 10
print("After first round:", points)

points = 25
print("After second round:", points)
```

**Wait!** This introduces something new: printing multiple things in one `print()` statement.

When you use commas inside `print()`, Python prints everything separated by a space:

`print("Text", variable)` → Python displays: `Text value_in_variable`

**Output:**
```
Starting points: 0
After first round: 10
After second round: 25
```

**Key insight:** This is a preview of something we'll explore more. For now: commas in `print()` let you print multiple things at once, separated by spaces.

---

## Common Mistakes & Error Messages

### Mistake 1: Using a Variable That Doesn't Exist

**Code:**
```python
print(username)
```

**Error:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print(username)
          ^
NameError: name 'username' is not defined
```

**What this means:** Python looked for a variable called `username`, but you never created it. There's no box with that label.

**Fix:** Create the variable first:
```python
username = "Alice"
print(username)
```

---

### Mistake 2: Forgetting Quotes Around Text

**Code:**
```python
name = Alice
print(name)
```

**Error:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    name = Alice
           ^
NameError: name 'Alice' is not defined
```

**What this means:** Python thinks `Alice` is a variable name, not text. You need quotes to tell Python "this is literal text."

**Fix:** Add quotes:
```python
name = "Alice"
print(name)
```

---

### Mistake 3: Typo in Variable Name

**Code:**
```python
name = "Alice"
print(nam)        # Typo: nam instead of name
```

**Error:**
```
Traceback (most recent call last):
  File "hello.py", line 2, in <module>
    print(nam)
          ^
NameError: name 'nam' is not defined
```

**What this means:** Python is looking for a variable called `nam`, but you created one called `name`. Python doesn't forgive typos.

**Fix:** Spell it correctly:
```python
name = "Alice"
print(name)
```

---

### Mistake 4: Using Special Characters in Variable Names

**Code:**
```python
user-name = "Alice"
print(user-name)
```

**Error:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    user-name = "Alice"
        ^
SyntaxError: invalid syntax
```

**What this means:** The hyphen `-` is not allowed in variable names. Python sees `user`, then `-`, then `name` and gets confused.

**Fix:** Use underscores instead:
```python
user_name = "Alice"
print(user_name)
```

---

### Mistake 5: Starting Variable Name with a Number

**Code:**
```python
2name = "Alice"
print(2name)
```

**Error:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    2name = "Alice"
    ^
SyntaxError: invalid syntax
```

**What this means:** Variable names can't start with a number.

**Fix:** Start with a letter:
```python
name2 = "Alice"
print(name2)
```

---

## Summary of Examples

- Variables store values you can reuse
- You create them with `name = value`
- Python looks them up when you use them (no quotes)
- Text must have quotes; numbers and true/false don't
- Variables can change—each assignment replaces the old value
- Variable names follow rules and conventions
- Errors tell you exactly what went wrong

Next: practice these concepts with exercises.
