# Type Conversion: Examples & Demos

## Example 1: The Problem We're Solving

Remember this problem?

**Code:**
```python
number1 = input("Enter first number: ")
number2 = input("Enter second number: ")
print(number1 + number2)
```

**Program interaction:**
```
Enter first number: 5
Enter second number: 3
53
```

**Why it's wrong:**

`input()` returns text. `"5" + "3"` joins text → `"53"`, not math.

**Execution flow:**

Line 1: `input()` returns `"5"` (text)

Line 2: `input()` returns `"3"` (text)

Line 3: `"5" + "3"` joins text → `"53"`

Now we'll fix it with type conversion.

---

## Example 2: Converting Text to Integer

**Code:**
```python
number_text = input("Enter a number: ")
number = int(number_text)

print(number_text)
print(number)
```

**Program interaction:**
```
Enter a number: 5
5
5
```

**Wait, they look the same!** But they're different types.

**Execution flow:**

Line 1: `input()` returns `"5"` (text/string)

Line 2: `int("5")` converts to `5` (integer/number)

Line 3: Print the text (displays: 5)

Line 4: Print the number (displays: 5)

They display the same, but internally they're different.

**Key insight:** The first is text `"5"`, the second is number `5`. Same display, different type.

---

## Example 3: Now Math Works!

**Code:**
```python
number1 = int(input("Enter first number: "))
number2 = int(input("Enter second number: "))
result = number1 + number2

print(result)
```

**Program interaction:**
```
Enter first number: 5
Enter second number: 3
8
```

**Now it's correct!**

**Execution flow:**

Line 1: `input()` returns `"5"` (text) → `int()` converts to `5` (number)

Line 2: `input()` returns `"3"` (text) → `int()` converts to `3` (number)

Line 3: `5 + 3` = `8` (math)

Line 5: Print `8`

**Key insight:** By converting to `int()` first, we can do math.

---

## Example 4: Converting to Float

**Code:**
```python
price_text = input("Enter price: ")
price = float(price_text)

print("Price:", price)
```

**Program interaction:**
```
Enter price: 19.99
Price: 19.99
```

**Execution flow:**

Line 1: `input()` returns `"19.99"` (text)

Line 2: `float()` converts to `19.99` (decimal number)

Line 3: Print the result

**Key insight:** `float()` handles decimal numbers. `int()` only handles whole numbers.

---

## Example 5: Converting Number to Text

**Code:**
```python
age = 25
message = "You are " + str(age) + " years old"

print(message)
```

**Output:**
```
You are 25 years old
```

**Execution flow:**

Line 1: `age = 25` (number)

Line 2: 
- `str(25)` converts number to `"25"` (text)
- `"You are " + "25" + " years old"` joins text
- Result: `"You are 25 years old"`

Line 4: Print the message

**Key insight:** When combining numbers with text using `+`, convert the number to text first.

---

## Example 6: Converting Integer to Float and Back

**Code:**
```python
whole_number = 5
decimal_number = float(whole_number)

print(whole_number)
print(decimal_number)
```

**Output:**
```
5
5.0
```

**Execution flow:**

Line 1: `whole_number = 5` (integer)

Line 2: `float(5)` converts to `5.0` (float)

Line 3: Print the integer (displays: 5)

Line 4: Print the float (displays: 5.0)

**Key insight:** `int()` drops the decimal. `float()` adds a decimal.

---

## Example 7: Real Calculation with Input

**Code:**
```python
print("Simple Calculator")

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

sum_result = num1 + num2
diff_result = num1 - num2
product_result = num1 * num2

print("Sum:", sum_result)
print("Difference:", diff_result)
print("Product:", product_result)
```

**Program interaction:**
```
Simple Calculator
Enter first number: 10
Enter second number: 3
Sum: 13
Difference: 7
Product: 30
```

**Execution flow:**

Line 3: Get first number, convert to integer

Line 4: Get second number, convert to integer

Lines 6-8: Do math with the numbers

Lines 10-12: Print results

**Key insight:** Type conversion enables real calculations.

---

## Example 8: Building a Message with Multiple Types

**Code:**
```python
name = input("What is your name? ")
age = int(input("How old are you? "))
height = float(input("What is your height in meters? "))

message = name + " is " + str(age) + " years old and " + str(height) + " meters tall"

print(message)
```

**Program interaction:**
```
What is your name? Alice
How old are you? 28
What is your height in meters? 1.65
Alice is 28 years old and 1.65 meters tall
```

**Execution flow:**

Line 1: Get name (text)

Line 2: Get age, convert to integer

Line 3: Get height, convert to float

Line 5: Build message by converting numbers to text and joining with `+`

Line 7: Print message

**Key insight:** Real programs use multiple types and convert as needed.

---

## Example 9: Checking Types

**Code:**
```python
text = "5"
number = 5

print(type(text))
print(type(number))
```

**Output:**
```
<class 'str'>
<class 'int'>
```

**Execution flow:**

Line 1: `text = "5"` (string)

Line 2: `number = 5` (integer)

Line 4: `type(text)` returns the type of `text`

Line 5: `type(number)` returns the type of `number`

**Key insight:** `type()` tells you what type something is. Useful for debugging.

---

## Example 10: What Happens When Conversion Fails

**Code:**
```python
text = "hello"
number = int(text)

print(number)
```

**Error:**
```
Traceback (most recent call last):
  File "example.py", line 2, in <module>
    number = int(text)
ValueError: invalid literal for int() with base 10: 'hello'
```

**What happens:**

Python tries to convert `"hello"` to a number, but it can't because "hello" isn't a number in text form.

**Key insight:** Type conversion only works if the content is actually convertible. Later, you'll learn error handling to deal with this.

---

## Example 11: Converting Between Types in Sequence

**Code:**
```python
# Start with a string
text = "42"

# Convert to integer
integer = int(text)

# Convert integer to float
decimal = float(integer)

# Convert back to string
result = str(decimal)

print(text)
print(integer)
print(decimal)
print(result)
```

**Output:**
```
42
42
42.0
42.0
```

**Execution flow:**

Line 3: text = `"42"` (string)

Line 6: integer = `42` (integer, converted from string)

Line 9: decimal = `42.0` (float, converted from integer)

Line 12: result = `"42.0"` (string, converted from float)

**Key insight:** You can chain conversions. Type A → Type B → Type C.

---

## Example 12: Practical Example - Order Total

**Code:**
```python
print("Order Calculator")
print()

item_price_text = input("Item price: ")
quantity_text = input("Quantity: ")

item_price = float(item_price_text)
quantity = int(quantity_text)

total = item_price * quantity

print("Total: $" + str(total))
```

**Program interaction:**
```
Order Calculator

Item price: 19.99
Quantity: 3
Total: $59.97
```

**Execution flow:**

Line 3: Get price as text

Line 4: Get quantity as text

Line 6: Convert price to float for math

Line 7: Convert quantity to integer for math

Line 9: Multiply (now we can do math)

Line 11: Convert result back to text for display

**Key insight:** This is a complete real-world example using type conversion.

---

## Common Questions

**Q: Do I always need to convert input?**

A: Only if you need to do math or comparisons with numbers. If you're just displaying it, text is fine.

**Q: Can I convert `"5.5"` to an integer?**

A: Yes, but it drops the decimal: `int("5.5")` → `ValueError`. Actually, you'd need `int(float("5.5"))` → `5`.

**Q: What if I forget to convert?**

A: Python will error or give unexpected results. Common mistake: trying to add user input (text) as if it's a number.

**Q: Can I convert `"3.14"` to an integer?**

A: Not directly. You'd need to do `int(float("3.14"))` → `3`. Go through float first.

---

## Summary of Examples

- `int()` converts text to whole numbers
- `float()` converts text to decimal numbers
- `str()` converts numbers to text
- `type()` shows you what type something is
- Type conversion enables math with user input
- Conversion only works if the text is actually convertible

Next: practice these concepts with exercises.
