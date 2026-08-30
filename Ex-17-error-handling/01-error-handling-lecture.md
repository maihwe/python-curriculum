# Error Handling: Anticipating and Managing Failures - Lecture

## Why This Matters

Real programs don't always work perfectly. Users do unexpected things:

```python
age = input("Enter your age: ")
years_until_100 = 100 - age  # CRASH if user types "abc"
```

If user enters "abc" instead of a number:
```
TypeError: unsupported operand type(s) for -: 'int' and 'str'
Program crashes!
```

Your program should expect failures and handle them gracefully.

**Error handling** lets you anticipate problems and respond to them.

```python
age = input("Enter your age: ")
try:
    age = int(age)
    years_until_100 = 100 - age
    print("Years until 100:", years_until_100)
except ValueError:
    print("Please enter a valid number")
```

Program keeps running even if user enters invalid data.

---

## The Mental Model: Errors Are Normal

In real programs, errors happen:
- User types wrong input
- File doesn't exist
- Network connection fails
- Calculation overflows
- Division by zero

Professional code anticipates these and handles them gracefully.

```
Beginner code:    Input → Calculate → Crash on error
Professional code: Input → Try → Handle error → Continue
```

---

## The Mental Model: Try/Except Blocks

Try/except blocks let you:
- **Try** something risky
- **Except** if it fails, do something else

```python
try:
    risky_code_here()
except:
    handle_error_here()
```

If risky_code succeeds, except block is skipped.
If risky_code fails, except block runs.

**Flow:**
```
try:
    age = int(input("Age: "))  ← Risky (user might type "abc")
    print(100 - age)
except:
    print("Invalid input")      ← Runs only if try fails
```

---

## The Mental Model: Specific Exceptions

Different errors have different types:

```
ValueError     → Wrong type ("abc" when int expected)
TypeError      → Wrong operation (add string to number)
ZeroDivisionError → Divide by zero
KeyError       → Dictionary key doesn't exist
IndexError     → List index out of range
FileNotFoundError → File doesn't exist
```

You can catch specific errors:

```python
try:
    result = int(user_input)
except ValueError:  # Specific error type
    print("Must be a number")
```

---

## The Mental Model: Multiple Except Blocks

Catch different errors differently:

```python
try:
    x = int(input("Enter number: "))
    y = int(input("Divisor: "))
    result = x / y
except ValueError:
    print("Must enter numbers")
except ZeroDivisionError:
    print("Can't divide by zero")
```

First matching except block runs. Others are skipped.

---

## The Mental Model: Finally Block

**Finally** runs regardless of try/except outcome:

```python
file = open("data.txt", "r")
try:
    data = file.read()
except:
    print("Error reading file")
finally:
    file.close()  # ALWAYS runs, even if error
```

Finally is perfect for cleanup (closing files, releasing resources).

---

## The Mental Model: Raising Exceptions

Sometimes you want to raise your own error:

```python
def validate_age(age):
    if age < 0:
        raise ValueError("Age can't be negative")
    if age > 150:
        raise ValueError("Age too high")
    return age

try:
    age = validate_age(-5)
except ValueError as e:
    print("Invalid:", e)
```

Raise lets you enforce constraints and signal problems.

---

## Key Concepts to Remember

1. **Errors are normal in real programs**
2. **Try/except catches errors**
3. **Try = risky code**
4. **Except = error handling code**
5. **Specific error types** (ValueError, TypeError, etc.)
6. **Multiple except blocks** for different errors
7. **Finally = always runs**
8. **Raise = create your own errors**
9. **Error handling = robust programs**
10. **Debugging = finding root causes**

---

## Common Misconceptions

**"Good code never has errors"**

Wrong. Good code handles errors gracefully.

**"Try/except slows down programs"**

No meaningful impact. Good code uses try/except everywhere.

**"I should catch all errors with except:"**

Bad. Use specific error types. Blank except hides bugs.

**"Errors always mean my code is wrong"**

Not necessarily. Sometimes users provide bad input.

---

## Error Types You'll See

**ValueError** - Wrong value for operation
```python
int("abc")  # ValueError
```

**TypeError** - Wrong type for operation
```python
"text" + 5  # TypeError
```

**ZeroDivisionError** - Divide by zero
```python
10 / 0  # ZeroDivisionError
```

**KeyError** - Dictionary key doesn't exist
```python
dict = {"a": 1}
dict["b"]  # KeyError
```

**IndexError** - List index out of range
```python
list = [1, 2, 3]
list[10]  # IndexError
```

**FileNotFoundError** - File doesn't exist
```python
open("nonexistent.txt", "r")  # FileNotFoundError
```

---

## Best Practices

**1. Catch specific errors**
```python
✅ except ValueError:
❌ except:
```

**2. Use meaningful error messages**
```python
✅ print("Age must be between 0 and 150")
❌ print("Error")
```

**3. Use finally for cleanup**
```python
✅ Always close files in finally
❌ Hope file closes somehow
```

**4. Raise errors for constraints**
```python
✅ if password_too_weak: raise ValueError(...)
❌ Silently accept weak password
```

---

## Summary

**Error handling** makes programs robust:
- Anticipate problems
- Catch errors gracefully
- Provide helpful messages
- Clean up resources
- Keep running

Professional programmers write defensive code that handles failures.

Next: see error handling in action.
