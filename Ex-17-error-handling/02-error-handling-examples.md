# Error Handling: Examples & Demos

## Example 1: Try/Except Basic

**Code:**
```python
try:
    age = int(input("Enter age: "))
    print("Age:", age)
except ValueError:
    print("Please enter a valid number")
```

**Output (if user enters "abc"):**
```
Enter age: abc
Please enter a valid number
```

**Output (if user enters "25"):**
```
Enter age: 25
Age: 25
```

**Key insight:** Try/except prevents crash from bad input.

---

## Example 2: Multiple Except Blocks

**Code:**
```python
try:
    x = int(input("Number: "))
    y = int(input("Divisor: "))
    result = x / y
    print("Result:", result)
except ValueError:
    print("Must enter numbers")
except ZeroDivisionError:
    print("Can't divide by zero")
```

**Output (if y=0):**
```
Number: 10
Divisor: 0
Can't divide by zero
```

**Key insight:** Different errors caught by different except blocks.

---

## Example 3: Accessing Non-Existent Dictionary Key

**Code:**
```python
person = {"name": "Alice", "age": 25}

try:
    city = person["city"]
except KeyError:
    print("Key 'city' not found in dictionary")

print("Program continues")
```

**Output:**
```
Key 'city' not found in dictionary
Program continues
```

**Key insight:** Try/except catches KeyError gracefully.

---

## Example 4: List Index Out of Range

**Code:**
```python
numbers = [10, 20, 30]

try:
    print(numbers[0])  # Works
    print(numbers[10]) # IndexError
except IndexError:
    print("Index out of range")
```

**Output:**
```
10
Index out of range
```

**Key insight:** Catch IndexError when accessing lists.

---

## Example 5: Type Errors

**Code:**
```python
try:
    result = "text" + 5
except TypeError:
    print("Can't add string and number")
```

**Output:**
```
Can't add string and number
```

**Key insight:** TypeError when operations don't match types.

---

## Example 6: File Not Found

**Code:**
```python
try:
    file = open("nonexistent.txt", "r")
    data = file.read()
except FileNotFoundError:
    print("File not found")
```

**Output:**
```
File not found
```

**Key insight:** Catch FileNotFoundError gracefully.

---

## Example 7: Finally Block

**Code:**
```python
try:
    x = int(input("Number: "))
    result = 100 / x
    print("Result:", result)
except ZeroDivisionError:
    print("Can't divide by zero")
finally:
    print("Finally block always runs")
```

**Output (if x=0):**
```
Number: 0
Can't divide by zero
Finally block always runs
```

**Key insight:** Finally runs whether try succeeds or except runs.

---

## Example 8: Error Message as Variable

**Code:**
```python
try:
    age = int("abc")
except ValueError as e:
    print("Error:", e)
```

**Output:**
```
Error: invalid literal for int() with base 10: 'abc'
```

**Key insight:** Catch error message with `as e`.

---

## Example 9: Raising Custom Errors

**Code:**
```python
def validate_age(age):
    if age < 0:
        raise ValueError("Age can't be negative")
    if age > 150:
        raise ValueError("Age unrealistic")
    return age

try:
    age = validate_age(-5)
except ValueError as e:
    print("Invalid:", e)
```

**Output:**
```
Invalid: Age can't be negative
```

**Key insight:** Raise errors to enforce constraints.

---

## Example 10: Validation Function

**Code:**
```python
def validate_email(email):
    if "@" not in email:
        raise ValueError("Invalid email")
    return email

try:
    email = validate_email("bademail")
except ValueError as e:
    print("Error:", e)
```

**Output:**
```
Error: Invalid email
```

**Key insight:** Use raise to validate user input.

---

## Example 11: Safe Dictionary Access

**Code:**
```python
person = {"name": "Alice", "age": 25}

try:
    city = person["city"]
    print("City:", city)
except KeyError:
    print("City not in dictionary, using default")
    city = "Unknown"

print("City:", city)
```

**Output:**
```
City not in dictionary, using default
City: Unknown
```

**Key insight:** Provide sensible defaults on KeyError.

---

## Example 12: Chained Try/Except

**Code:**
```python
try:
    data = input("Enter number: ")
    x = int(data)
    y = input("Enter divisor: ")
    divisor = int(y)
    result = x / divisor
    print("Result:", result)
except ValueError:
    print("Must enter valid numbers")
except ZeroDivisionError:
    print("Divisor can't be zero")
```

**Output (if inputs valid):**
```
Enter number: 10
Enter divisor: 2
Result: 5.0
```

**Key insight:** Multiple errors caught in same try/except.

---

## Example 13: File Operations with Finally

**Code:**
```python
file = None
try:
    file = open("test.txt", "w")
    file.write("Hello!")
except IOError:
    print("Error writing file")
finally:
    if file:
        file.close()
    print("File closed")
```

**Output:**
```
File closed
```

**Key insight:** Finally ensures resources are cleaned up.

---

## Example 14: Nested Try/Except

**Code:**
```python
try:
    x = int(input("Number: "))
    try:
        y = int(input("Divisor: "))
        result = x / y
        print("Result:", result)
    except ZeroDivisionError:
        print("Can't divide by zero")
except ValueError:
    print("Must enter numbers")
```

**Output (if x=10, y=0):**
```
Number: 10
Divisor: 0
Can't divide by zero
```

**Key insight:** Try/except can be nested for complex logic.

---

## Example 15: Real-World - Safe Data Processing

**Code:**
```python
data = ["10", "20", "abc", "30"]
numbers = []

for item in data:
    try:
        num = int(item)
        numbers.append(num)
    except ValueError:
        print(f"Skipping invalid: {item}")

print("Valid numbers:", numbers)
print("Sum:", sum(numbers))
```

**Output:**
```
Skipping invalid: abc
Valid numbers: [10, 20, 30]
Sum: 60
```

**Key insight:** Try/except in loops for robust data processing.

---

## Summary of Examples

- Basic try/except
- Multiple except blocks
- Catching specific errors (KeyError, IndexError, TypeError, FileNotFoundError)
- Finally blocks
- Error messages with `as e`
- Raising custom errors
- Validation functions
- Safe dictionary access
- Chained try/except
- File operations with cleanup
- Nested try/except
- Real-world data processing

Next: practice with exercises.
