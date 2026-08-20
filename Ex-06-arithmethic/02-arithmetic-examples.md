# Arithmetic: Examples & Demos

## Example 1: Basic Addition

**Code:**
```python
a = 5
b = 3
result = a + b

print(result)
```

**Execution flow:**

Line 1: Store `5` in `a`

Line 2: Store `3` in `b`

Line 3: Add them, store in `result` → `5 + 3 = 8`

Line 5: Print the result

**Output:**
```
8
```

**Key insight:** Math operations work just like you'd expect. The result is stored in a variable.

---

## Example 2: All Basic Operations

**Code:**
```python
a = 10
b = 3

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
```

**Output:**
```
Addition: 13
Subtraction: 7
Multiplication: 30
Division: 3.3333333333333335
```

**Key insight:** Notice division returns a float with many decimals. This is normal.

---

## Example 3: Floor Division vs. Regular Division

**Code:**
```python
a = 10
b = 3

regular = a / b
floor = a // b

print("Regular division:", regular)
print("Floor division:", floor)
```

**Output:**
```
Regular division: 3.3333333333333335
Floor division: 3
```

**Key insight:** `/` gives exact decimal. `//` drops the decimal part. Use `//` when you need whole numbers.

---

## Example 4: Modulo (Remainder)

**Code:**
```python
a = 10
b = 3

remainder = a % b

print("10 divided by 3 is 3 remainder", remainder)
```

**Output:**
```
10 divided by 3 is 3 remainder 1
```

**Explanation:**

10 ÷ 3 = 3 remainder 1

Because 3 × 3 = 9, and 10 - 9 = 1

**Key insight:** Modulo gives you the remainder. Useful for checking evenness, cycling, patterns.

---

## Example 5: Exponentiation (Powers)

**Code:**
```python
print("2 to power 3:", 2 ** 3)
print("5 squared:", 5 ** 2)
print("10 to power 0:", 10 ** 0)
print("2 to power 10:", 2 ** 10)
```

**Output:**
```
2 to power 3: 8
5 squared: 25
10 to power 0: 1
2 to power 10: 1024
```

**Key insight:** `**` raises to a power. Anything to power 0 is 1.

---

## Example 6: Order of Operations

**Code:**
```python
# Without parentheses (follows PEMDAS)
result1 = 2 + 3 * 4
print("2 + 3 * 4 =", result1)

# With parentheses (changes order)
result2 = (2 + 3) * 4
print("(2 + 3) * 4 =", result2)

# Complex order
result3 = 2 ** 3 * 4 + 1
print("2 ** 3 * 4 + 1 =", result3)
```

**Output:**
```
2 + 3 * 4 = 14
(2 + 3) * 4 = 20
2 ** 3 * 4 + 1 = 33
```

**Explanation:**

First: `2 + 3 * 4`
- Multiply first: 3 * 4 = 12
- Then add: 2 + 12 = 14

Second: `(2 + 3) * 4`
- Parentheses first: 2 + 3 = 5
- Then multiply: 5 * 4 = 20

Third: `2 ** 3 * 4 + 1`
- Exponent first: 2 ** 3 = 8
- Then multiply: 8 * 4 = 32
- Then add: 32 + 1 = 33

**Key insight:** Order matters! Use parentheses when unsure.

---

## Example 7: Storing and Reusing Results

**Code:**
```python
# Calculate area of a rectangle
length = 5
width = 3
area = length * width

print("Length:", length)
print("Width:", width)
print("Area:", area)
```

**Output:**
```
Length: 5
Width: 3
Area: 15
```

**Key insight:** You calculate once, then reuse the result multiple times.

---

## Example 8: Updating Variables

**Code:**
```python
score = 10
print("Starting score:", score)

score = score + 5
print("After getting 5 points:", score)

score = score * 2
print("After doubling:", score)
```

**Output:**
```
Starting score: 10
After getting 5 points: 15
After doubling: 30
```

**Explanation:**

Line 1: `score = 10`

Line 4: `score = score + 5` means "take what's in score (10), add 5, store it back" → 15

Line 7: `score = score * 2` means "take what's in score (15), multiply by 2, store it back" → 30

**Key insight:** You can update variables by doing math on themselves.

---

## Example 9: Using Shortcuts (+=, -=, etc.)

**Code:**
```python
score = 10

score += 5      # Same as: score = score + 5
print("After += 5:", score)

score *= 2      # Same as: score = score * 2
print("After *= 2:", score)

score -= 10     # Same as: score = score - 10
print("After -= 10:", score)
```

**Output:**
```
After += 5: 15
After *= 2: 30
After -= 10: 20
```

**Key insight:** `+=`, `-=`, `*=`, etc. are shortcuts for updating variables.

---

## Example 10: Real Calculator with User Input

**Code:**
```python
print("Simple Calculator")
print()

num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

sum_result = num1 + num2
diff_result = num1 - num2
product_result = num1 * num2
quotient_result = num1 / num2

print()
print("Sum:", sum_result)
print("Difference:", diff_result)
print("Product:", product_result)
print("Quotient:", quotient_result)
```

**Program interaction:**
```
Simple Calculator

Enter first number: 10
Enter second number: 3

Sum: 13.0
Difference: 7.0
Product: 30.0
Quotient: 3.3333333333333335
```

**Key insight:** Combine input, type conversion, and arithmetic to build a real calculator.

---

## Example 11: Calculating Area and Perimeter

**Code:**
```python
# Rectangle dimensions
length = 5
width = 3

# Calculate area and perimeter
area = length * width
perimeter = 2 * (length + width)

print("Rectangle:")
print("Length:", length)
print("Width:", width)
print("Area:", area)
print("Perimeter:", perimeter)
```

**Output:**
```
Rectangle:
Length: 5
Width: 3
Area: 15
Perimeter: 16
```

**Explanation:**

Area = length × width = 5 × 3 = 15

Perimeter = 2 × (length + width) = 2 × (5 + 3) = 2 × 8 = 16

**Key insight:** Real-world formulas use arithmetic operators.

---

## Example 12: Checking Even and Odd

**Code:**
```python
num = 7

if num % 2 == 0:
    print(num, "is even")
else:
    print(num, "is odd")
```

**Output:**
```
7 is odd
```

**Explanation:**

`num % 2` gives the remainder when divided by 2.

- If remainder is 0 → even
- If remainder is 1 → odd

7 % 2 = 1 (remainder), so 7 is odd.

**Key insight:** Modulo is useful for checking divisibility and patterns.

---

## Example 13: Complex Formula - Compound Interest

**Code:**
```python
principal = 1000        # Starting amount
rate = 0.05             # 5% annual rate
time = 2                # years

# Formula: A = P(1 + r)^t
amount = principal * (1 + rate) ** time

print("Principal: $" + str(principal))
print("Rate: " + str(rate * 100) + "%")
print("Time: " + str(time) + " years")
print("Final amount: $" + str(amount))
```

**Output:**
```
Principal: $1000
Rate: 5.0%
Time: 2 years
Final amount: $1102.5
```

**Explanation:**

A = 1000 × (1 + 0.05)²
A = 1000 × (1.05)²
A = 1000 × 1.1025
A = 1102.5

**Key insight:** Complex formulas are just combinations of basic operations.

---

## Example 14: Temperature Conversion Revisited

**Code:**
```python
celsius = 0
fahrenheit = (celsius * 9/5) + 32

print(str(celsius) + "°C = " + str(fahrenheit) + "°F")

celsius = 100
fahrenheit = (celsius * 9/5) + 32

print(str(celsius) + "°C = " + str(fahrenheit) + "°F")
```

**Output:**
```
0°C = 32.0°F
100°C = 212.0°F
```

**Key insight:** Formulas use all operators together.

---

## Example 15: Handling Float Precision

**Code:**
```python
result1 = 1/3
result2 = 1/10
result3 = 0.1 + 0.2

print("1/3 =", result1)
print("1/10 =", result2)
print("0.1 + 0.2 =", result3)
```

**Output:**
```
1/3 = 0.3333333333333333
1/10 = 0.1
0.1 + 0.2 = 0.30000000000000004
```

**Why the weird number for 0.1 + 0.2?**

Computers can't store all decimal numbers perfectly. This is a limitation of how floats work. It's usually not a problem, but be aware.

**Key insight:** Floats have tiny precision errors. This is normal and usually doesn't matter.

---

## Summary of Examples

- All basic operations work as expected
- Division (`/`) always returns float
- Floor division (`//`) returns integer
- Modulo (`%`) returns remainder
- Exponentiation (`**`) raises to power
- Order of operations matters (use parentheses if unsure)
- Store results in variables
- Update variables with shortcuts
- Combine operations for complex calculations

Next: practice with exercises.
