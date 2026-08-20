# Logical Operators: Combining Conditions - Lecture

## Why This Matters

So far, you can test single conditions:

```python
if age >= 18:
    print("Adult")
```

But real programs need to test *multiple conditions together*:

- "If age >= 18 **AND** has license → drive"
- "If score >= 90 **OR** completed extra credit → A grade"
- "If **NOT** banned → allow access"

**Logical operators** let you combine conditions. This is how you test complex real-world scenarios.

Without them, you'd need deeply nested if/else blocks. With them, you can write clean, readable conditions.

---

## The Mental Model: What Are Logical Operators?

Logical operators combine boolean values (True/False).

Python has three:

1. **`and`** — Both conditions must be true
2. **`or`** — At least one condition must be true
3. **`not`** — Reverses true/false

Each returns True or False.

---

## The Mental Model: `and` Operator

**`and`** means both conditions must be true.

```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("Can drive")
```

Flow:
- Is `age >= 18`? → True
- Is `has_license` true? → True
- Both are true, so `and` returns **True**
- Code runs

**Truth table for `and`:**

```
True  and  True   = True
True  and  False  = False
False and  True   = False
False and  False  = False
```

Only True + True = True. Everything else is False.

---

## The Mental Model: `or` Operator

**`or`** means at least one condition must be true.

```python
score = 85

if score >= 90 or completed_extra_credit:
    print("A grade")
```

Flow:
- Is `score >= 90`? → False
- Did they complete extra credit? → True (assume)
- At least one is true, so `or` returns **True**
- Code runs

**Truth table for `or`:**

```
True  or  True   = True
True  or  False  = True
False or  True   = True
False or  False  = False
```

False + False = False. Everything else is True.

---

## The Mental Model: `not` Operator

**`not`** reverses true/false.

```python
is_banned = False

if not is_banned:
    print("Access granted")
```

Flow:
- Is `is_banned` true? → False
- `not False` → **True**
- Code runs

**Truth table for `not`:**

```
not True  = False
not False = True
```

Simple reversal.

---

## The Mental Model: Combining Multiple Operators

You can chain them:

```python
age = 25
has_license = True
has_insurance = True

if age >= 18 and has_license and has_insurance:
    print("Can drive legally")
```

All three must be true.

Or mix `and` and `or`:

```python
if (age >= 18 and has_license) or has_emergency_permit:
    print("Can drive")
```

"Either: (adult AND licensed) OR has emergency permit"

---

## The Mental Model: Order of Operations

Just like math, logical operators have order:

1. **`not`** (highest)
2. **`and`**
3. **`or`** (lowest)

```python
True or False and False
```

This evaluates as:
1. `False and False` → False
2. `True or False` → True

Use parentheses to be clear:

```python
(True or False) and False  # False
True or (False and False)  # True
```

---

## The Mental Model: Short-Circuit Evaluation

Python stops evaluating as soon as it knows the answer.

```python
age = 10

if age >= 18 and has_license:
    print("Can drive")
```

Python checks: is `age >= 18`? → False

It stops. It doesn't even check `has_license` because `and` needs both to be true.

This is called **short-circuit evaluation**. It's efficient.

---

## The Mental Model: Real-World Examples

**Login:** username correct **AND** password correct

```python
if username == "alice" and password == "secret":
    print("Login successful")
```

**Access:** admin **OR** owner

```python
if is_admin or is_owner:
    print("Access granted")
```

**Validation:** age 18-65 **AND** has license **AND** passed test

```python
if 18 <= age <= 65 and has_license and passed_test:
    print("Approved")
```

---

## Key Concepts to Remember

1. **`and`** — Both must be true
2. **`or`** — At least one must be true
3. **`not`** — Reverses true/false
4. Logical operators return True or False
5. Order: `not`, `and`, `or`
6. Use parentheses for clarity
7. Python stops evaluating once answer is known

---

## Common Misconceptions

**"`and` means add conditions"**

No. It means *both* must be true. If either is false, the result is false.

**"I can write `age >= 18 and <= 65`"**

No. You need: `age >= 18 and age <= 65`

Each condition must be complete.

**"`or` means choose one"**

Not exactly. `or` means "at least one." Could be both.

**"Logical operators are hard"**

They're just True/False tables. Think of them as gates: `and` requires all doors open. `or` requires at least one. `not` flips the lock.

---

## Summary

Logical operators combine conditions. This lets you test complex scenarios with clean, readable code.

Instead of deeply nested if/else blocks, you write:

```python
if condition1 and condition2 and condition3:
    # Do something
```

Much cleaner.

Next: see logical operators in action.
