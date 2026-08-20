# Arithmetic: Performing Mathematical Operations - Lecture

## Why This Matters

You can now:
- Store numbers in variables
- Get numbers from users
- Convert text to numbers

But you can't actually *do math* yet. You can't build a real calculator, budget tracker, or physics simulator without arithmetic.

**Arithmetic operations** are how you perform calculations: adding, subtracting, multiplying, dividing, and more advanced operations.

This is foundational for:
- Calculators and financial apps
- Games (score tracking, health systems)
- Physics simulations
- Data analysis
- Any program that works with quantities

---

## The Mental Model: What Are Operators?

An **operator** is a symbol that tells Python to do something.

You've already seen one:
- `=` means "assign this value"
- `+` means "join these strings"

**Arithmetic operators** are special: they perform math.

Basic operators:
- `+` addition
- `-` subtraction
- `*` multiplication
- `/` division
- `//` floor division (division with no decimal)
- `%` modulo (remainder)
- `**` exponentiation (power)

Each does what you'd expect, with one critical rule: **order matters**.

---

## The Mental Model: Order of Operations

Math has rules about which operations happen first. Python follows the same rules.

**PEMDAS (or BODMAS):**
1. Parentheses (or Brackets)
2. Exponents (or Orders)
3. Multiplication and Division (left to right)
4. Addition and Subtraction (left to right)

Examples:

```python
2 + 3 * 4       # Multiply first, then add: 2 + 12 = 14 (not 20)
(2 + 3) * 4     # Parentheses first: 5 * 4 = 20
2 ** 3 * 4      # Exponent first: 8 * 4 = 32
10 / 2 * 5      # Left to right: (10 / 2) * 5 = 25
```

If you're unsure, use parentheses. They make your intent clear.

---

## The Mental Model: Basic Operators

**Addition (`+`)**
```python
5 + 3           # = 8
```

**Subtraction (`-`)**
```python
10 - 3          # = 7
```

**Multiplication (`*`)**
```python
4 * 5           # = 20
```

**Division (`/`)**
```python
10 / 2          # = 5.0 (always returns float)
```

Important: `/` always returns a float, even if the result is a whole number.

```python
10 / 2          # = 5.0 (not 5)
```

---

## The Mental Model: Advanced Operators

**Floor Division (`//`)**

Divides, then drops the decimal part.

```python
10 // 3         # = 3 (not 3.33...)
10 // 2         # = 5 (same as regular division if result is whole)
```

Useful for: counting complete groups, integer math.

**Modulo (`%`)**

Returns the *remainder* after division.

```python
10 % 3          # = 1 (10 divided by 3 is 3 remainder 1)
10 % 2          # = 0 (10 divided by 2 is 5 remainder 0)
7 % 3           # = 1 (7 divided by 3 is 2 remainder 1)
```

Useful for: checking if a number is even (num % 2 == 0), cycling through patterns, finding divisibility.

**Exponentiation (`**`)**

Raises a number to a power.

```python
2 ** 3          # = 8 (2 to the power of 3)
5 ** 2          # = 25 (5 squared)
10 ** 0         # = 1 (anything to power 0 is 1)
```

---

## The Mental Model: Storing Results

You can do math and store the result in a variable:

```python
result = 5 + 3
print(result)   # Prints: 8

area = 5 * 4
print(area)     # Prints: 20
```

This is how real programs work: calculate something, store it, use it later.

---

## The Mental Model: Updating Variables with Math

A common pattern: take a variable, do math with it, store the result back.

```python
score = 10
score = score + 5   # Add 5 to score, store it back
print(score)        # Prints: 15
```

This happens so often that Python has a shortcut:

```python
score = 10
score += 5          # Same as: score = score + 5
print(score)        # Prints: 15
```

Other shortcuts:
- `x -= 3` means `x = x - 3`
- `x *= 2` means `x = x * 2`
- `x /= 2` means `x = x / 2`

---

## The Mental Model: Integer vs. Float Results

When you do math, the result type depends on the input types:

```python
5 + 3           # Both integers → 8 (integer)
5.0 + 3         # One float → 8.0 (float)
5 / 2           # Division → 2.5 (always float)
5 // 2          # Floor division → 2 (integer)
```

This matters because:
- Integers are exact
- Floats have rounding errors (1/3 = 0.333... forever)
- Some operations (like `/`) always return floats

---

## The Mental Model: Negative Numbers

Math works with negative numbers:

```python
-5 + 3          # = -2
10 - 15         # = -5
-5 * -3         # = 15 (negative × negative = positive)
-10 / 2         # = -5.0
```

---

## The Mental Model: Real-World Applications

Arithmetic is everywhere in programs:

- **Calculators**: Add, subtract, multiply, divide
- **Games**: Track score, health, damage
- **Finance**: Interest, loans, budgets
- **Physics**: Speed = distance / time
- **Statistics**: Average = sum / count
- **Discounts**: Final price = price * (1 - discount%)

Every one of these uses arithmetic operators.

---

## Key Concepts to Remember

1. **Basic operators**: `+`, `-`, `*`, `/` do what you expect
2. **Advanced operators**: `//` (floor), `%` (remainder), `**` (power)
3. **Order matters**: Follow PEMDAS (parentheses, exponents, mult/div, add/sub)
4. **Division always returns float**: `10 / 2 = 5.0`, not `5`
5. **Floor division returns integer**: `10 // 3 = 3`
6. **Modulo returns remainder**: `10 % 3 = 1`
7. **Store results in variables**: You'll use them later
8. **Shortcuts exist**: `+=`, `-=`, `*=`, `/=` for updating variables
9. **Type matters**: Integer + integer ≠ float + float

---

## Common Misconceptions

**"Division always gives a whole number"**

False. In Python 3, `/` always returns a float. Use `//` if you want integer division.

```python
10 / 3          # = 3.333... (float)
10 // 3         # = 3 (integer)
```

**"Modulo is useless"**

False. It's incredibly useful for:
- Checking if even: `num % 2 == 0`
- Cycling: `index % list_length` 
- Finding divisibility

**"I have to use the exact operator symbols"**

True, mostly. But you can use spaces however you want:

```python
5+3             # Valid
5 + 3           # Valid
5  +  3         # Valid
5+ 3            # Valid (but ugly)
```

---

## Summary

Arithmetic operations let you:
- Perform calculations with numbers
- Build real programs that compute results
- Store and reuse calculated values
- Solve mathematical problems

Next: see arithmetic in action with real examples.
