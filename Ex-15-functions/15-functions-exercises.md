# Functions: Exercises & Practice

## Exercise 1: Simple Function

Create a function that prints a message.

**Expected output:**
```
Hello from function!
```

**What to do:**
1. Create a file called `simple_function.py`
2. Define function `say_hello()` with no parameters
3. Inside, print "Hello from function!"
4. Call the function
5. Run it

**Hint:** `def say_hello():`

---

## Exercise 2: Function with Parameter

Create a function that greets someone by name.

**Expected output:**
```
Hello, Alice!
Hello, Bob!
```

**What to do:**
1. Create a file called `greet_function.py`
2. Define function `greet(name)`
3. Inside, print "Hello, " + name + "!"
4. Call it twice with different names
5. Run it

**Hint:** `def greet(name):`

---

## Exercise 3: Function with Return

Create a function that adds two numbers and returns result.

**Expected output:**
```
5 + 3 = 8
10 + 20 = 30
```

**What to do:**
1. Create a file called `add_function.py`
2. Define function `add(a, b)` that returns a + b
3. Call it with (5, 3) and store in variable
4. Print result
5. Repeat with (10, 20)
6. Run it

**Hint:** `return a + b`

---

## Exercise 4: Multiple Calls

Create a function and call it many times.

**Expected output:**
```
1
2
3
4
5
```

**What to do:**
1. Create a file called `multiple_calls.py`
2. Define function `count(n)` that prints n
3. Call it 5 times with 1, 2, 3, 4, 5
4. Run it

**Hint:** Just repeat the function call 5 times.

---

## Exercise 5: Local vs Global Scope

Create a program showing local and global variables.

**Expected output:**
```
Global x = 100
Inside function, x = 5
After function, x = 100
```

**What to do:**
1. Create a file called `scope_demo.py`
2. Create global variable x = 100
3. Create function that sets local x = 5
4. Print x before, inside (call function), after
5. Run it

**Hint:** Variables inside functions don't affect global ones.

---

## Exercise 6: Conversion Function

Create a function that converts kilometers to miles.

**Expected output:**
```
10 km = 6.21371 miles
```

**What to do:**
1. Create a file called `km_to_miles.py`
2. Define function `km_to_miles(km)`
3. Inside: return km * 0.621371
4. Call with 10, print result
5. Run it

**Hint:** 1 km = 0.621371 miles

---

## Exercise 7: Validation Function

Create a function that checks if age is valid (18+).

**Expected output:**
```
Age 25 valid: True
Age 15 valid: False
```

**What to do:**
1. Create a file called `age_validator.py`
2. Define function `is_adult(age)`
3. If age >= 18, return True
4. Otherwise, return False
5. Call with 25 and 15, print results
6. Run it

**Hint:** Use if/else.

---

## Exercise 8: Function Calling Function

Create two functions where one calls the other.

**Expected output:**
```
Result: 20
```

**What to do:**
1. Create a file called `function_chain.py`
2. Define function `add(a, b)` that returns a + b
3. Define function `double_sum(x, y)` that:
   - Calls add(x, y)
   - Multiplies result by 2
   - Returns it
4. Call double_sum(5, 5)
5. Print result
6. Run it

**Hint:** `result = add(5, 5)` inside double_sum

---

## Exercise 9: List Processing Function

Create a function that finds the biggest number in a list.

**Expected output:**
```
Maximum: 42
```

**What to do:**
1. Create a file called `find_max.py`
2. Define function `find_max(numbers)`
3. Inside: loop through list, find largest
4. Return largest
5. Call with [10, 42, 3, 28]
6. Print result
7. Run it

**Hint:** Start with max = numbers[0], then compare.

---

## Exercise 10: String Processing Function

Create a function that reverses a string.

**Expected output:**
```
Forward: Hello
Backward: olleH
```

**What to do:**
1. Create a file called `reverse_string.py`
2. Define function `reverse(text)`
3. Inside: return text[::-1]
4. Call with "Hello"
5. Print both versions
6. Run it

**Hint:** [::-1] reverses strings.

---

## Exercise 11: Counting Function

Create a function that counts vowels in a string.

**Expected output:**
```
Vowels in 'Hello World': 3
```

**What to do:**
1. Create a file called `count_vowels.py`
2. Define function `count_vowels(text)`
3. Loop through letters, count if in 'aeiouAEIOU'
4. Return count
5. Call with "Hello World"
6. Print result
7. Run it

**Hint:** Use `if letter in 'aeiouAEIOU':`

---

## Exercise 12: Temperature Converter

Create function to convert temperature scales.

**Expected output:**
```
0°C = 32.0°F
100°C = 212.0°F
```

**What to do:**
1. Create a file called `temp_converter.py`
2. Define function `celsius_to_fahrenheit(c)`
3. Formula: (c * 9/5) + 32
4. Call with 0 and 100
5. Print results
6. Run it

**Hint:** (c * 9/5) + 32

---

## Exercise 13: Grade Calculator

Create function that returns letter grade.

**Expected output:**
```
85% = B
92% = A
72% = C
```

**What to do:**
1. Create a file called `grade_calc.py`
2. Define function `get_grade(percent)`
3. If >= 90: return "A"
4. Else if >= 80: return "B"
5. Else if >= 70: return "C"
6. Else: return "F"
7. Test with 85, 92, 72
8. Run it

**Hint:** Use elif statements.

---

## Exercise 14: Real-World - Password Validator

Create function that validates passwords.

**Expected output:**
```
Is 'pass123' valid: True
Is 'weak' valid: False
```

**What to do:**
1. Create a file called `password_validator.py`
2. Define function `is_strong_password(pwd)`
3. Return True if:
   - Length >= 8
   - Contains at least 1 number
   - Contains at least 1 letter
4. Test with "pass123" and "weak"
5. Run it

**Hint:** Use `any(c.isdigit() for c in pwd)` and `any(c.isalpha() for c in pwd)`

---

## Exercise 15: Real-World - Calculator with Multiple Operations

Create a calculator with several functions.

**Expected output:**
```
5 + 3 = 8
5 - 3 = 2
5 * 3 = 15
5 / 3 = 1.67
```

**What to do:**
1. Create a file called `calculator.py`
2. Define functions: add, subtract, multiply, divide
3. Each takes 2 parameters, returns result
4. divide should check for division by zero
5. Test all operations
6. Run it

**Hint:** Build and test functions one by one.

---

## Checking Your Work

After exercises, ask yourself:

- ✓ Can I define and call functions?
- ✓ Do I understand parameters?
- ✓ Do I understand return values?
- ✓ Do I understand local scope?
- ✓ Can I write practical functions?

---

## Key Concepts to Remember

**Defining:**
- `def function_name(parameters):`
- Indented code inside

**Calling:**
- `function_name(arguments)`
- Multiple calls possible

**Parameters vs Arguments:**
- Parameter = in definition
- Argument = when calling

**Return Values:**
- `return value`
- Stops function, sends value back

**Scope:**
- Local = inside function only
- Global = everywhere
- Local overrides global inside function

---

## Next Steps

Once you've mastered functions:

1. You can write reusable code
2. You can build complex programs
3. You're ready for file input/output
4. You understand code organization

You're making excellent progress! 🎉

**14 core topics complete → 1 more advanced topic to go!**

Next topic: **Topic 16: File I/O** (reading and writing files)
