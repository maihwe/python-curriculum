# Type Conversion: Exercises & Practice

## Exercise 1: Convert Text to Integer

Create a program that gets a number from the user, converts it to an integer, and prints it.

**Program interaction:**
```
Enter a number: 42
42
```

**What to do:**
1. Create a file called `text_to_int.py`
2. Use `input()` to get a number from the user
3. Convert it to `int()`
4. Print the result
5. Run it and test with different numbers

**Hint:** Remember `input()` returns text. You need `int()` to convert it.

---

## Exercise 2: Convert Text to Float

Create a program that gets a decimal number from the user, converts it to float, and prints it.

**Program interaction:**
```
Enter a price: 19.99
19.99
```

**What to do:**
1. Create a file called `text_to_float.py`
2. Get input from the user
3. Convert it to `float()`
4. Print the result
5. Run it and test

**Hint:** `float()` handles decimal numbers.

---

## Exercise 3: Add Two Numbers (The Fix!)

Finally fix the problem from Input Exercise 8!

Create a program that adds two numbers entered by the user.

**Program interaction:**
```
Enter first number: 5
Enter second number: 3
Result: 8
```

**What to do:**
1. Create a file called `add_numbers.py`
2. Get two numbers from the user
3. Convert both to `int()`
4. Add them
5. Print the result
6. Run it and verify it works

**Hint:** Convert immediately after `input()`.

---

## Exercise 4: Subtract and Multiply

Create a program that performs three operations on two user-entered numbers.

**Program interaction:**
```
Enter first number: 10
Enter second number: 3
Sum: 13
Difference: 7
Product: 30
```

**What to do:**
1. Create a file called `math_operations.py`
2. Get two numbers from the user
3. Convert both to `int()`
4. Calculate sum, difference, and product
5. Print all three results
6. Run it

**Hint:** You'll need three print statements for the three results.

---

## Exercise 5: Convert Number to Text

Create a program that builds a message by converting a number to text.

**Program interaction:**
```
Enter a number: 42
The answer is 42
```

**What to do:**
1. Create a file called `number_to_text.py`
2. Get a number from the user
3. Convert it to `int()` and store in a variable
4. Use `str()` to convert it back to text for display
5. Build a message combining text and the converted number
6. Print the message

**Hint:** Use `+` to combine text strings.

---

## Exercise 6: Temperature Converter

Create a program that converts temperature in Celsius to Fahrenheit.

Formula: F = (C × 9/5) + 32

**Program interaction:**
```
Enter temperature in Celsius: 0
32.0 degrees Fahrenheit
```

**What to do:**
1. Create a file called `celsius_to_fahrenheit.py`
2. Get Celsius temperature from user
3. Convert to `float()`
4. Apply the formula
5. Print the result with `str()` in the message
6. Run it and test with 0, 100, and other values

**Hint:** You'll need to do math and then convert the result to text for display.

---

## Exercise 7: Building a Profile (Revisited)

Create a program that collects user information and builds a formatted profile.

**Program interaction:**
```
Name: Alice
Age: 28
Height (meters): 1.65

Profile:
Name: Alice
Age: 28
Height: 1.65 meters
```

**What to do:**
1. Create a file called `profile_converter.py`
2. Get name (text), age (convert to int), height (convert to float)
3. Build formatted message using `str()` to convert numbers
4. Print the profile nicely
5. Run it

**Hint:** You'll mix text input and numeric input, converting as needed.

---

## Exercise 8: Simple Loan Calculator

Create a program that calculates simple loan interest.

Formula: Interest = Principal × Rate × Time

**Program interaction:**
```
Loan amount: 1000
Interest rate (%): 5
Time (years): 2
Interest: $100.0
```

**What to do:**
1. Create a file called `loan_calculator.py`
2. Get principal (convert to float)
3. Get rate (convert to float)
4. Get time (convert to int or float)
5. Calculate interest
6. Print result with `str()` conversion
7. Run it

**Hint:** All conversions happen right after `input()`.

---

## Exercise 9: Checking Types

Create a program that shows the type of different values.

**Expected output:**
```
Type of "5": <class 'str'>
Type of 5: <class 'int'>
Type of 5.0: <class 'float'>
Type of True: <class 'bool'>
```

**What to do:**
1. Create a file called `check_types.py`
2. Create variables with different types
3. Use `type()` to check each type
4. Print the results
5. Run it

**Hint:** `type()` returns the type. Print it directly.

---

## Exercise 10: Convert and Check Type

Create a program that shows conversion by comparing types before and after.

**Code structure:**
```python
text = "42"
print("Before:", type(text), text)

number = int(text)
print("After:", type(number), number)
```

**What to do:**
1. Create a file called `convert_and_check.py`
2. Start with text
3. Check its type
4. Convert to integer
5. Check the new type
6. Print both to compare
7. Run it

**Hint:** This shows the difference conversion makes.

---

## Exercise 11: Debug This

This code has an error. Run it, read the error, and fix it.

```python
price = input("Price: ")
quantity = input("Quantity: ")
total = price * quantity

print(total)
```

**Program interaction (after fix):**
```
Price: 10
Quantity: 3
30
```

**What to do:**
1. Create a file called `debug_conversion.py`
2. Copy the broken code
3. Run it and read the error
4. Predict what the problem is
5. Fix it by adding type conversion
6. Run it again

**Hint:** What's the type of `price` and `quantity` from `input()`?

---

## Exercise 12: Budget Calculator

Create a program that helps calculate a monthly budget.

**Program interaction:**
```
Monthly income: 3000
Rent: 1000
Food: 400
Utilities: 200
Entertainment: 300

Income: $3000.0
Expenses: $1900.0
Remaining: $1100.0
```

**What to do:**
1. Create a file called `budget_calculator.py`
2. Get income (convert to float)
3. Get multiple expenses (convert to float)
4. Calculate total expenses
5. Calculate remaining
6. Print formatted results with `str()` conversion
7. Run it

**Hint:** Add up all expenses, then subtract from income.

---

## Exercise 13: Data Type Converter

Create a program that converts a number from one type to another and shows the results.

**Program interaction:**
```
Enter a number: 42
As integer: 42
As float: 42.0
As text: 42
```

**What to do:**
1. Create a file called `type_converter.py`
2. Get a number from user (as text)
3. Convert to integer, float, and back to string
4. Print all versions
5. Run it

**Hint:** You're showing the same value in three different types.

---

## Exercise 14: Combining Operations

Create a program that uses multiple type conversions and mathematical operations.

**Program interaction:**
```
Enter two numbers:
First: 15
Second: 4

Sum: 19
Difference: 11
Product: 60
Average: 9.5
```

**What to do:**
1. Create a file called `combined_operations.py`
2. Get two numbers from user
3. Convert both to appropriate types
4. Perform addition, subtraction, multiplication, and average
5. Print all results with proper formatting
6. Run it

**Hint:** Average = (a + b) / 2. You might use `float()` for the average.

---

## Exercise 15: Real-World Application - Tip Calculator

Create a program that calculates tip and total bill.

**Program interaction:**
```
Bill amount: 50.00
Tip percentage: 20
Tip: $10.0
Total: $60.0
```

**What to do:**
1. Create a file called `tip_calculator.py`
2. Get bill amount (convert to float)
3. Get tip percentage (convert to int or float)
4. Calculate tip amount (bill × tip% / 100)
5. Calculate total (bill + tip)
6. Print both with `str()` conversion
7. Run it and test

**Hint:** Tip calculation: (bill × tip_percent) / 100

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Did I use type conversion correctly?
- ✓ Are the results mathematically correct?
- ✓ Did I convert at the right time?
- ✓ Can I explain why conversion was needed?

---

## Important Observations

**About Type Conversion:**
- `input()` always returns text—convert if you need numbers
- `int()` is for whole numbers
- `float()` is for decimal numbers
- `str()` is for converting numbers to text for display
- Conversion only works if the content is convertible
- Type matters: "5" and 5 are different

**About Using Types:**
- Know what type your data is
- Convert immediately after `input()` if you need numbers
- Convert back to text before displaying numbers in messages
- Use `type()` to debug

---

## Next Steps

Once you've completed these exercises:

1. You can convert text to numbers
2. You can convert numbers to text
3. You can do math with user input
4. You understand why types matter
5. You can use `type()` to debug

You're ready for Topic 6: **Arithmetic Operations**

In Arithmetic, you'll learn all the math operations Python supports (+, -, *, /, //, %, **) and the order they execute in.

Next lesson: making Python a powerful calculator!
