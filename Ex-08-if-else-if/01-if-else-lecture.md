# If/Else: Making Decisions - Lecture

## Why This Matters

You can now compare values and get True or False.

But comparisons alone don't do anything. You just get an answer:

```python
age = 25
is_adult = age >= 18
print(is_adult)    # Prints: True
```

So what? The program doesn't *respond* to the comparison.

**If/Else statements** let you *do different things* based on whether a comparison is True or False.

This is where programs become intelligent:

- "If password is correct, log in. Else, show error."
- "If score is high enough, show congratulations. Else, show try again."
- "If user is adult, show content. Else, show warning."
- "If item is in stock, process order. Else, show out of stock."

Without if/else, programs are just automated scripts. With if/else, they respond to conditions.

---

## The Mental Model: What Is an If/Else Statement?

An if/else statement is a **fork in the road**.

Imagine:

```
Does the password match?
    ↓
   Yes → Log in the user
    ↓
    No → Show error message
```

The program checks a condition. If true, it does one thing. If false, it does another.

In code:

```python
password = input("Enter password: ")

if password == "secret":
    print("Access granted!")
else:
    print("Access denied!")
```

If the password is "secret", the program goes one way. If it's not, the program goes another way.

---

## The Mental Model: Basic If Statement

The simplest form: **if something is true, do this.**

```python
age = 25

if age >= 18:
    print("You are an adult")
```

Flow:
1. Check: is `age >= 18`?
2. If True → print the message
3. If False → skip the print (do nothing)

You only run the code inside the if block if the condition is True.

---

## The Mental Model: If/Else Statement

Add an alternative: **if true, do this. Else, do that.**

```python
age = 15

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

Flow:
1. Check: is `age >= 18`?
2. If True → print "You are an adult"
3. If False → print "You are a minor"

Every code path is covered. Either the if runs, or the else runs. Never both.

---

## The Mental Model: If/Elif/Else

For multiple conditions: **if this, else if that, else something else.**

```python
score = 85

if score >= 90:
    print("A - Excellent")
elif score >= 80:
    print("B - Good")
elif score >= 70:
    print("C - Okay")
else:
    print("F - Fail")
```

Flow:
1. Is `score >= 90`? If yes, print "A" and stop.
2. If no, is `score >= 80`? If yes, print "B" and stop.
3. If no, is `score >= 70`? If yes, print "C" and stop.
4. If none are true, print "F".

The program checks conditions in order. As soon as one is true, it runs that block and stops. The else at the end catches anything that didn't match.

---

## The Mental Model: Indentation Matters

Python uses **indentation** (spaces at the start of a line) to know which code is inside the if/else block.

```python
if age >= 18:
    print("You are an adult")      # This is INSIDE the if
    print("You can vote")          # This is INSIDE the if

print("Done")                      # This is OUTSIDE the if
```

The indented lines only run if the condition is true. The non-indented line always runs.

This is critical: if you don't indent correctly, your program won't work as expected.

---

## The Mental Model: Indentation Rules

Always indent code inside if/else blocks:

```python
if condition:
    # This code runs if condition is True
    statement1
    statement2
else:
    # This code runs if condition is False
    statement3
    statement4

# This always runs (not indented)
statement5
```

Use 4 spaces per indentation level (this is Python convention).

---

## The Mental Model: Nested If/Else

You can have if/else inside if/else:

```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("You can drive")
    else:
        print("You need a license")
else:
    print("You are too young to drive")
```

The inner if/else only runs if the outer if is true.

---

## The Mental Model: Common Mistake - Using = Instead of ==

Easy mistake:

```python
if password = "secret":    # WRONG: Assignment, not comparison
    print("Correct")
```

This assigns "secret" to password (if it compiles at all). You want to compare:

```python
if password == "secret":   # CORRECT: Comparison
    print("Correct")
```

Remember: `=` is assignment. `==` is comparison.

---

## The Mental Model: Boolean Variables in If/Else

You can use boolean variables directly:

```python
is_adult = age >= 18

if is_adult:
    print("You can vote")
else:
    print("Too young to vote")
```

Or even simpler:

```python
if age >= 18:
    print("You can vote")
```

Both work. The second is cleaner.

---

## Key Concepts to Remember

1. **if** statement: Do something if condition is true
2. **else** clause: Do something if condition is false
3. **elif** clause: Check another condition if first is false
4. **Indentation** is critical—it defines which code is inside the block
5. Conditions are compared using `==`, `!=`, `>`, `<`, `>=`, `<=`
6. Only one path runs (if, elif, or else—never multiple)
7. The else is optional
8. You can nest if/else inside if/else

---

## Real-World Applications

If/Else appears everywhere in programs:

- **Login systems**: If correct password, log in. Else, show error.
- **Games**: If player has enough points, level up. Else, show score.
- **E-commerce**: If item in stock, process order. Else, show out of stock.
- **Banking**: If sufficient funds, withdraw. Else, show error.
- **Thermostats**: If too cold, heat. If too hot, cool. Else, maintain.
- **Validators**: If valid email, accept. Else, show error.

---

## Common Misconceptions

**"Else if is one word"**

No, it's two words (or one word: `elif`). Use `elif` in Python.

**"Both if and else run"**

No. Exactly one block runs (unless there are multiple elif). They're alternatives, not both.

**"I need an else"**

No. If/else is optional. You can have just `if`. But if you want different behavior for false, you need else.

**"If statements slow down code"**

Negligibly. If/else is fundamental to programming. It's not an optimization to avoid them.

---

## Summary

If/Else statements make programs intelligent. They check conditions and run different code based on whether conditions are true or false.

This is the transition from "script that does the same thing every time" to "program that responds to input and conditions."

Next: see if/else in action with real examples.
