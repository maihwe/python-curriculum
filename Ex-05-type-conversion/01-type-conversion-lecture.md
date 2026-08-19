# Type Conversion: Changing Data Types - Lecture

## Why This Matters

Remember this problem from Input Exercise 8?

```python
number1 = input("Enter first number: ")
number2 = input("Enter second number: ")
print(number1 + number2)
```

You entered `5` and `3`, but got `53`, not `8`.

Why? Because `input()` returns **text** (strings), and when you combine text with `+`, you get text joined together, not math.

```
"5" + "3" = "53"  (text joining)
5 + 3 = 8         (math)
```

**Type conversion** solves this problem. It's how you change one type of data into another type.

You need this for:
- Converting user input (text) into numbers for math
- Converting numbers to text for display
- Checking what type of data you have
- Building programs that work with mixed data types

---

## The Mental Model: What Are Data Types?

Python has different *types* of data. Each type behaves differently:

**Strings (text):**
```python
"hello"
"5"
"3.14"
```

Behavior:
- Combined with `+` = joined together
- Can contain letters, numbers, symbols
- Can be empty: `""`

**Integers (whole numbers):**
```python
5
-10
0
1000
```

Behavior:
- Combined with `+` = added
- Can be positive or negative
- No decimal point

**Floats (decimal numbers):**
```python
3.14
-2.5
0.0
1000.99
```

Behavior:
- Combined with `+` = added
- Can be positive or negative
- Has a decimal point

**Booleans (true/false):**
```python
True
False
```

Behavior:
- Only two values
- Used for decisions
- (We'll learn more about these later)

---

## The Mental Model: Why Types Matter

The same symbol `+` means different things depending on type:

```python
"5" + "3"   # Text: "5" and "3" joined → "53"
5 + 3       # Numbers: 5 and 3 added → 8
```

This is critical: Python needs to know **what type** your data is to know how to handle it.

```python
name = "Alice"          # Type: string
age = 25                # Type: integer
height = 5.5            # Type: float
is_student = True       # Type: boolean
```

When you use a variable, Python looks at its *type* to decide what operations are allowed.

---

## The Mental Model: Converting Types

**Type conversion** means changing from one type to another.

The main conversions:

**`int()` — Convert to integer (whole number)**

```python
int("5")        # "5" (text) → 5 (number)
int("123")      # "123" (text) → 123 (number)
int(3.14)       # 3.14 (float) → 3 (integer, drops decimal)
```

**`float()` — Convert to float (decimal number)**

```python
float("3.14")   # "3.14" (text) → 3.14 (number)
float("5")      # "5" (text) → 5.0 (number with decimal)
float(10)       # 10 (integer) → 10.0 (float)
```

**`str()` — Convert to string (text)**

```python
str(5)          # 5 (number) → "5" (text)
str(3.14)       # 3.14 (number) → "3.14" (text)
str(True)       # True (boolean) → "True" (text)
```

These are *functions* that take a value and return it in a different type.

---

## The Mental Model: Why Conversion Needed

Here's the flow for a calculator:

```
User types: 5
    ↓
input() returns: "5" (text, because input always returns text)
    ↓
You want to do math, so you need: 5 (number)
    ↓
int("5") converts text to number
    ↓
Now you can do math: 5 + 3 = 8
```

Type conversion is the bridge between text and numbers.

---

## The Mental Model: Common Conversion Patterns

**Pattern 1: Get input, convert to number, do math**

```python
number_text = input("Enter a number: ")    # Returns "5" (text)
number = int(number_text)                   # Convert to 5 (number)
result = number + 10                        # Do math
print(result)                               # Print 15
```

**Pattern 2: Do math, convert to text for display**

```python
age = 25                # Number
message = "You are " + str(age) + " years old"  # Convert for display
print(message)          # Prints: You are 25 years old
```

**Pattern 3: Combine user input with text**

```python
name = input("What is your name? ")     # Text
age_text = input("How old are you? ")   # Text
age = int(age_text)                     # Convert to number

print(name + " is " + str(age) + " years old")
```

These patterns solve real problems.

---

## The Mental Model: What If Conversion Fails?

What happens if you try to convert invalid text to a number?

```python
int("hello")    # This will crash!
```

Python can't convert "hello" to a number because "hello" isn't a number.

This is important to remember: **Type conversion only works if the text is actually a number.**

```python
int("5")        # Works: "5" is a number in text form
int("5.5")      # Fails: can't convert to integer (it's a decimal)
int("hello")    # Fails: not a number at all
```

(Later, you'll learn error handling to deal with these failures gracefully.)

---

## The Mental Model: Checking Types

You can check what type a value is using `type()`:

```python
type("hello")       # Returns: <class 'str'>
type(5)             # Returns: <class 'int'>
type(3.14)          # Returns: <class 'float'>
type(True)          # Returns: <class 'bool'>
```

This is useful for debugging: "Why isn't my math working? Oh, it's a string, not a number!"

---

## Key Concepts to Remember

1. **Data types** include: string, integer, float, boolean
2. **Type conversion** changes data from one type to another
3. **`int()`** converts to integer
4. **`float()`** converts to float
5. **`str()`** converts to string
6. **`type()`** tells you what type something is
7. **Conversion only works** if the text is actually convertible
8. **User input is always text**, so convert it if you need numbers

---

## Why This Matters for Programs

Real programs work with mixed types:

- User enters text: "5" (string)
- You need to do math: 5 (integer)
- You need to display results: "The answer is 8" (string)

Type conversion is the tool that lets you move smoothly between these.

Without type conversion, you'd be stuck. Input gives you strings. Math needs numbers. Display needs strings. Type conversion lets you bridge the gap.

---

## Preview: String Formatting (After This)

Once you master type conversion, you'll learn cleaner ways to combine numbers and text:

```python
# Old way (type conversion):
"The answer is " + str(result)

# New way (string formatting - coming soon):
f"The answer is {result}"
```

Both work. The second is cleaner. We'll learn it after arithmetic operations.

---

## Summary

- Different data types behave differently
- `int()` converts to numbers
- `float()` converts to decimal numbers
- `str()` converts to text
- Type conversion solves the "text problem" from earlier
- User input is always text, so you often need to convert it

Next: see type conversion in action.
