# Comparisons: Testing Values - Lecture

## Why This Matters

So far, your programs do the same thing every time.

```python
name = input("What is your name? ")
print("Hello, " + name)
```

No matter what the user enters, the program does the same thing.

But real programs make *decisions*. They need to answer questions:

- "Is the password correct?"
- "Is the score high enough?"
- "Is the temperature too hot?"
- "Does the username already exist?"

**Comparisons** let you test whether something is true or false. Once you can compare, you can make decisions.

This is the bridge between "doing the same thing every time" and "making decisions based on data."

---

## The Mental Model: What Is a Comparison?

A **comparison** tests whether something is true or false.

It's a question:

```
Is 5 greater than 3?
Is "hello" equal to "hello"?
Is the score more than 100?
```

Each comparison has an answer: **True** or **False**.

Python has **comparison operators** that let you test relationships between values:

- `==` equal to
- `!=` not equal to
- `>` greater than
- `<` less than
- `>=` greater than or equal to
- `<=` less than or equal to

---

## The Mental Model: Equality (==)

The `==` operator tests if two values are equal.

```python
5 == 5          # True
5 == 3          # False
"hello" == "hello"  # True
"hello" == "Hello"  # False (case matters!)
```

**Critical:** Don't confuse `=` and `==`:
- `=` is assignment (store a value)
- `==` is comparison (test if equal)

```python
x = 5           # Assigns 5 to x
x == 5          # Tests if x is equal to 5
```

---

## The Mental Model: Inequality (!=)

The `!=` operator tests if two values are *not* equal.

```python
5 != 3          # True (5 is not equal to 3)
5 != 5          # False (5 is equal to 5)
"hello" != "hello"  # False (they're equal)
"hello" != "world"  # True (they're different)
```

It's the opposite of `==`.

---

## The Mental Model: Greater Than and Less Than

`>` tests if the left is greater than the right.

```python
5 > 3           # True
3 > 5           # False
5 > 5           # False (equal, not greater)
```

`<` tests if the left is less than the right.

```python
3 < 5           # True
5 < 3           # False
5 < 5           # False (equal, not less)
```

---

## The Mental Model: Greater/Less Than or Equal

`>=` tests if greater than or equal.

```python
5 >= 3          # True
5 >= 5          # True
5 >= 6          # False
```

`<=` tests if less than or equal.

```python
3 <= 5          # True
5 <= 5          # True
6 <= 5          # False
```

These are useful because you often need "at least" or "at most."

---

## The Mental Model: Comparisons Return True or False

A comparison doesn't do anything by itself—it returns a boolean value.

```python
result = 5 > 3
print(result)   # Prints: True
```

You can store the result in a variable, print it, or use it later (which we'll do with if/else next lesson).

---

## The Mental Model: Comparing Different Types

You can compare numbers:

```python
5 > 3           # True
5.5 > 5         # True
```

You can compare strings (by alphabetical order):

```python
"apple" < "banana"    # True (a comes before b)
"zebra" > "apple"     # True
```

You can compare booleans:

```python
True == True    # True
False == False  # True
True != False   # True
```

But comparing different types often doesn't make sense:

```python
5 == "5"        # False (number vs. text, even though they look the same)
```

This is important: `5` (number) and `"5"` (text) are NOT equal.

---

## The Mental Model: Chaining Comparisons

You can do multiple comparisons (we'll use these with logic operators next):

```python
age = 25

is_old_enough = age >= 18  # True
is_young = age < 65        # True
```

Each comparison is independent. Later, you'll combine them with `and`, `or`, `not`.

---

## Key Concepts to Remember

1. **`==`** tests equality
2. **`!=`** tests inequality
3. **`>`** tests greater than
4. **`<`** tests less than
5. **`>=`** tests greater than or equal
6. **`<=`** tests less than or equal
7. Comparisons return **True** or **False**
8. Don't confuse `=` (assignment) with `==` (comparison)
9. String comparison is alphabetical
10. Different types usually don't compare as equal (`5 != "5"`)

---

## Why This Matters for Programs

Comparisons enable decisions:

- Check if password is correct (comparison) → grant access or deny
- Check if score is high enough (comparison) → show congratulations or try again
- Check if number is in range (comparison) → process or reject
- Check if username is taken (comparison) → allow or ask for different one

Without comparisons, programs can't respond to different situations.

---

## Common Misconceptions

**"I can use = for comparison"**

No. `=` assigns values. `==` compares. This is a very common mistake.

```python
if x = 5:           # WRONG: SyntaxError
if x == 5:          # CORRECT
```

**"True and False are strings"**

No. `True` and `False` are boolean values (a special type). They're not text.

```python
type(True)      # Returns: <class 'bool'>
type("True")    # Returns: <class 'str'>
```

**"Comparisons do something"**

No. Comparisons just return True or False. By themselves, they don't *do* anything. You use the result (next lesson with if/else).

---

## Summary

Comparisons test whether something is true or false. They return boolean values (True/False). This is the foundation for making decisions in programs.

Next: use comparisons to control program flow with if/else statements.
