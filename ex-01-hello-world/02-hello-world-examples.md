# Hello World: Examples & Demos

## Example 1: The Basic Hello World

**Code:**
```python
print("Hello, World!")
```

**What happens when you run it:**

Step 1: You save this as `hello.py`

Step 2: You open your terminal and type:
```
python3 hello.py
```

Step 3: Python reads the file

Step 4: Python executes the line

**Output:**
```
Hello, World!
```

**What you see on your screen:**
```
$ python3 hello.py
Hello, World!
$
```

The cursor returns to the prompt. The program is done.

---

## Example 2: Multiple Print Statements

What if we want to display more than one message?

**Code:**
```python
print("Hello, World!")
print("Welcome to Python!")
print("This is fun!")
```

**Execution flow:**

Line 1: Python sees `print("Hello, World!")` → executes it → "Hello, World!" appears

Line 2: Python sees `print("Welcome to Python!")` → executes it → "Welcome to Python!" appears

Line 3: Python sees `print("This is fun!")` → executes it → "This is fun!" appears

**Output:**
```
Hello, World!
Welcome to Python!
This is fun!
```

**Key insight:** Python reads your code **top to bottom, one line at a time**. Each `print()` statement displays on its own line.

---

## Example 3: Different Text in Print

Python doesn't care what text you put inside the quotes. It just displays it.

**Code:**
```python
print("Python is awesome!")
print("I'm learning to code!")
print("42")
print("!@#$%^&*()")
```

**Output:**
```
Python is awesome!
I'm learning to code!
42
!@#$%^&*()
```

**Key insight:** `print()` displays *exactly* what you put inside the quotes. No interpretation, no filtering. Just text on the screen.

---

## Example 4: Empty Print (Creating Blank Lines)

What happens if you print nothing?

**Code:**
```python
print("Line 1")
print()
print("Line 2")
```

**Output:**
```
Line 1

Line 2
```

**What's happening:** 

- `print("Line 1")` displays "Line 1"
- `print()` displays nothing but adds a blank line
- `print("Line 2")` displays "Line 2"

The `print()` with nothing inside creates a blank line. This is useful for spacing output.

---

## Example 5: Numbers as Text

You can print numbers, but they must be in quotes to be treated as text.

**Code:**
```python
print("The answer is 42")
print("2 + 2 = 4")
print("Year: 2024")
```

**Output:**
```
The answer is 42
2 + 2 = 4
Year: 2024
```

**Key insight:** If you put a number inside quotes, Python treats it as text, not as a mathematical value. We'll do real math later with variables.

---

## Example 6: Special Characters and Symbols

You can print almost anything inside quotes.

**Code:**
```python
print("Hello! How are you?")
print("Email: user@example.com")
print("Price: $19.99")
print("© 2024")
print("Line with... dots and --- dashes")
```

**Output:**
```
Hello! How are you?
Email: user@example.com
Price: $19.99
© 2024
Line with... dots and --- dashes
```

**Key insight:** Python doesn't interpret the text. It just displays it exactly as you write it.

---

## Example 7: Long Text in Print

You can print long messages.

**Code:**
```python
print("This is a longer message that spans what might normally be multiple lines, but since it's all in one print() statement, it displays as one line on your screen.")
```

**Output:**
```
This is a longer message that spans what might normally be multiple lines, but since it's all in one print() statement, it displays as one line on your screen.
```

**Key insight:** `print()` doesn't automatically wrap text. Everything in the quotes displays as one continuous line (until you tell Python to break it with another print statement).

---

## Common Mistakes & Error Messages

Understanding errors helps you learn faster.

### Mistake 1: Forgetting the Quotes

**Code:**
```python
print(Hello, World!)
```

**Error message:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print(Hello, World!)
          ^
NameError: name 'Hello' is not defined
```

**What this means:** Python looked for a thing called `Hello` in your program, but it doesn't exist. The quotes tell Python "this is text, not a name."

**Fix:** Add quotes:
```python
print("Hello, World!")
```

---

### Mistake 2: Forgetting the Parentheses

**Code:**
```python
print "Hello, World!"
```

**Error message:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print "Hello, World!"
          ^
SyntaxError: invalid syntax
```

**What this means:** Python doesn't recognize the syntax. In modern Python, `print()` requires parentheses. Without them, Python is confused.

**Fix:** Add parentheses:
```python
print("Hello, World!")
```

---

### Mistake 3: Mismatched Quotes

**Code:**
```python
print("Hello, World!')
```

**Error message:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print("Hello, World!')
          ^
SyntaxError: unterminated string literal (detected at line 1)
```

**What this means:** You opened with a double quote `"` but closed with a single quote `'`. Python expects them to match.

**Fix:** Use matching quotes:
```python
print("Hello, World!")
```

---

### Mistake 4: Missing Closing Parenthesis

**Code:**
```python
print("Hello, World!"
```

**Error message:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print("Hello, World!"
          ^
SyntaxError: '(' was never closed
```

**What this means:** You opened a parenthesis with `(` but never closed it with `)`.

**Fix:** Add the closing parenthesis:
```python
print("Hello, World!")
```

---

### Mistake 5: Extra Closing Parenthesis

**Code:**
```python
print("Hello, World!"))
```

**Error message:**
```
Traceback (most recent call last):
  File "hello.py", line 1, in <module>
    print("Hello, World!"))
                          ^
SyntaxError: unmatched ')'
```

**What this means:** You have an extra closing parenthesis. Python closes the `print()` at the first `)`, and then sees a second one with nothing to close.

**Fix:** Remove the extra parenthesis:
```python
print("Hello, World!")
```

---

## Running Code: Step-by-Step

Here's exactly how to run these examples on your computer:

**Step 1: Create a file**
- Open a text editor (not Word—use Notepad, VS Code, or similar)
- Write: `print("Hello, World!")`
- Save it as `hello.py` in a folder you'll remember

**Step 2: Open your terminal**
- Windows: Press Win + R, type `cmd`, press Enter
- Mac: Open Terminal (Applications → Utilities → Terminal)
- Linux: Open Terminal

**Step 3: Navigate to your file**
- Type: `cd` followed by the path to your folder
- Example: `cd Desktop` (if your file is on Desktop)

**Step 4: Run the file**
- Type: `python3 hello.py`
- Press Enter

**Step 5: You should see:**
```
Hello, World!
```

If you get an error, read the error message carefully. It tells you exactly what went wrong.

---

## Summary

- `print()` displays text on your screen
- Each print statement creates a new line
- Text must be in quotes
- Python reads code top to bottom
- Errors are messages telling you what to fix

Next: learn how to use **variables** to store and reuse information.
