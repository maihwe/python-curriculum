# Error Handling: Exercises & Practice

## Exercise 1: Basic Try/Except

Create a program that catches ValueError.

**Expected output (if user enters "abc"):**
```
Please enter a valid number
```

**What to do:**
1. Create a file called `basic_try_except.py`
2. Use try/except to convert input to int
3. If ValueError, print error message
4. Run it with invalid input
5. Run it with valid input

**Hint:** `try: int(input())` then `except ValueError:`

---

## Exercise 2: Multiple Except Blocks

Create a program with two different error handlers.

**Expected output (if y=0):**
```
Can't divide by zero
```

**What to do:**
1. Create a file called `multiple_except.py`
2. Get two numbers from user
3. Try to divide first by second
4. Catch ValueError (bad input)
5. Catch ZeroDivisionError (divide by zero)
6. Run with both error conditions

**Hint:** Two separate except blocks.

---

## Exercise 3: Catch KeyError

Create a program that safely accesses dictionary.

**Expected output:**
```
Key not found
```

**What to do:**
1. Create a file called `dict_error.py`
2. Create dictionary with 3 items
3. Try to access non-existent key
4. Catch KeyError
5. Run it

**Hint:** Use try/except KeyError.

---

## Exercise 4: Catch IndexError

Create a program that safely accesses list.

**Expected output:**
```
Index out of range
```

**What to do:**
1. Create a file called `list_error.py`
2. Create list with 3 items
3. Try to access index 10
4. Catch IndexError
5. Run it

**Hint:** Use try/except IndexError.

---

## Exercise 5: Error Message Variable

Create a program that captures error message.

**Expected output:**
```
Error: invalid literal for int() with base 10: 'abc'
```

**What to do:**
1. Create a file called `error_message.py`
2. Try to convert "abc" to int
3. Catch ValueError as e
4. Print the error message
5. Run it

**Hint:** `except ValueError as e:` then `print(e)`

---

## Exercise 6: Finally Block

Create a program that uses finally.

**Expected output:**
```
Can't divide by zero
Cleanup complete
```

**What to do:**
1. Create a file called `finally_block.py`
2. Try to divide 10 by 0
3. Catch ZeroDivisionError
4. Finally, print "Cleanup complete"
5. Run it

**Hint:** Finally runs after try or except.

---

## Exercise 7: Raise Custom Error

Create a function that raises ValueError.

**Expected output:**
```
Invalid: Age too young
```

**What to do:**
1. Create a file called `raise_error.py`
2. Define function that raises ValueError if age < 18
3. Try to call with age = 15
4. Catch and print error
5. Run it

**Hint:** `raise ValueError("message")`

---

## Exercise 8: Validation Function

Create a function that validates email.

**Expected output:**
```
Error: Must contain @
```

**What to do:**
1. Create a file called `validate_email.py`
2. Define function that raises ValueError if @ missing
3. Try with invalid email
4. Catch and print error
5. Run it

**Hint:** Check if "@" in email.

---

## Exercise 9: File Not Found Error

Create a program that handles missing files.

**Expected output:**
```
File not found
```

**What to do:**
1. Create a file called `file_error.py`
2. Try to open nonexistent file
3. Catch FileNotFoundError
4. Print error message
5. Run it

**Hint:** Use try/except FileNotFoundError.

---

## Exercise 10: Type Error

Create a program that catches TypeError.

**Expected output:**
```
Can't add string and number
```

**What to do:**
1. Create a file called `type_error.py`
2. Try to add "text" + 5
3. Catch TypeError
4. Print message
5. Run it

**Hint:** Trying to add incompatible types.

---

## Exercise 11: Safe Dictionary Access with Default

Create a program that uses default value on KeyError.

**Expected output:**
```
City: Unknown
```

**What to do:**
1. Create a file called `dict_default.py`
2. Create dictionary with name and age (no city)
3. Try to access city
4. On KeyError, use default "Unknown"
5. Print city
6. Run it

**Hint:** Provide default when key not found.

---

## Exercise 12: Chained Errors

Create a program that handles multiple error types.

**Program interaction:**
```
Enter number: 10
Enter divisor: abc
Must enter valid numbers
```

**What to do:**
1. Create a file called `chained_errors.py`
2. Get two numbers from user
3. Try to convert and divide
4. Catch ValueError
5. Catch ZeroDivisionError
6. Test both error conditions
7. Run it

**Hint:** Multiple except blocks.

---

## Exercise 13: Data Validation Loop

Create a program that keeps asking until valid.

**Expected output:**
```
Enter age: abc
Invalid, try again
Enter age: 25
Age: 25
```

**What to do:**
1. Create a file called `validation_loop.py`
2. Use while loop
3. Try to get valid age
4. Keep asking if ValueError
5. Break when valid
6. Run it

**Hint:** while True, break when valid.

---

## Exercise 14: Real-World - Safe CSV Processing

Create a program that processes data with errors.

**Expected output:**
```
Row 1: 10
Skipping invalid row: abc
Row 3: 30
```

**What to do:**
1. Create a file called `safe_processing.py`
2. Create list of strings: ["10", "abc", "30"]
3. Loop through each
4. Try to convert to int
5. On ValueError, skip and print message
6. On success, print value
7. Run it

**Hint:** Try/except inside for loop.

---

## Exercise 15: Real-World - Robust Calculator

Create a calculator that handles all errors gracefully.

**Expected output:**
```
Enter a: 10
Enter b: 5
10 + 5 = 15
Enter operation (or quit): divide
Enter a: 10
Enter b: 0
Can't divide by zero
```

**What to do:**
1. Create a file called `robust_calculator.py`
2. Create loop that asks for operation
3. Get two numbers
4. Try to perform operation
5. Catch ValueError (invalid input)
6. Catch ZeroDivisionError
7. Keep running until quit
8. Run it

**Hint:** While loop with multiple error cases.

---

## Checking Your Work

After exercises, ask yourself:

- ✓ Can I use try/except?
- ✓ Do I understand error types?
- ✓ Can I catch multiple errors?
- ✓ Can I use finally?
- ✓ Can I raise errors?

---

## Key Concepts to Remember

**Try/Except:**
- try = risky code
- except = error handler
- Can have multiple except blocks

**Common Errors:**
- ValueError = wrong value
- TypeError = wrong type
- ZeroDivisionError = divide by zero
- KeyError = dict key missing
- IndexError = list index missing
- FileNotFoundError = file missing

**Finally:**
- Always runs
- Perfect for cleanup

**Raise:**
- Create custom errors
- Enforce constraints

---

## Next Steps

Once you've mastered error handling:

1. You write robust programs
2. You handle user mistakes gracefully
3. You're ready for OOP
4. You understand defensive programming

You're making excellent progress! 🎉

**16 core topics complete → 2 final advanced topics!**

Next topic: **Topic 18: OOP Basics** (classes and objects)
