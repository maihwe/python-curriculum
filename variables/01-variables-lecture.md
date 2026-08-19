# Variables: Storing Information - Lecture

## Why This Matters

In the Hello World lesson, you printed text that was *hardcoded*—baked right into your code.

```python
print("Hello, World!")
```

But real programs need to *store information* and use it multiple times. Think about it:

- A calculator needs to remember the numbers you entered
- A weather app needs to store the temperature
- A game needs to remember your score
- A to-do list needs to remember your tasks

A **variable** is how programs store information so they can use it later.

This is the foundation for everything else. Once you understand variables, you can build programs that remember things, change things, and make decisions based on stored information.

---

## The Mental Model: What Is a Variable?

Think of a variable like a **labeled box**.

Imagine you're organizing your room. You have several boxes:

```
┌─────────────────┐
│  age            │
│  25             │
└─────────────────┘

┌─────────────────┐
│  name           │
│  "Alice"        │
└─────────────────┘

┌─────────────────┐
│  score          │
│  1050           │
└─────────────────┘
```

Each box has a **label** (the variable name) and **contents** (the value stored inside).

When you need to use that information, you refer to the label, not the contents. You don't have to remember what's inside—you just use the label.

A **variable** in Python is exactly this:
- A **name** (the label on the box)
- A **value** (what's stored inside)

Python remembers what's in each box. You just refer to the label.

---

## The Mental Model: Creating a Variable

Here's how you create a variable:

```python
name = "Alice"
```

Breaking this down:
- `name` — the label (what you'll call it)
- `=` — means "store this value in this box"
- `"Alice"` — the value (what goes in the box)

Think of `=` as an arrow pointing *left*: "Take what's on the right and put it in the box labeled on the left."

```
name ← "Alice"
```

The variable `name` now contains the text `"Alice"`.

---

## The Mental Model: Using a Variable

Once you create a variable, you can use it anywhere in your program.

```python
name = "Alice"
print(name)
```

What happens:
1. Python creates a box labeled `name`
2. Python puts `"Alice"` inside it
3. When you write `print(name)`, Python says: "What's in the box called `name`?"
4. Python finds `"Alice"` inside
5. Python displays it

Notice: We didn't print `"Alice"` directly. We printed the *variable* `name`. Python looked up what was inside and printed that.

---

## The Mental Model: Variables Store Any Type of Information

Variables can store different *types* of information:

```python
age = 25              # A whole number
price = 19.99         # A decimal number
name = "Bob"          # Text
is_student = True     # True or False
```

We'll learn more about types later. For now, just know: variables are flexible. They can hold numbers, text, or true/false values.

---

## The Mental Model: Variables Can Change

This is crucial: **The value in a variable can change.**

```python
score = 0
print(score)     # Displays: 0

score = 100
print(score)     # Displays: 100

score = 50
print(score)     # Displays: 50
```

Each time you assign a new value with `=`, the old value is forgotten. The box gets a new item.

This is why they're called "variables"—they *vary*. They change.

---

## Key Insight: Variable Names vs. Variable Values

This is critical to understand:

**Without quotes** = Python looks up the variable

```python
print(name)    # Python looks inside the variable 'name'
```

**With quotes** = Python treats it as literal text

```python
print("name")  # Python displays the text: name
```

Example:

```python
name = "Alice"

print(name)      # Displays: Alice
print("name")    # Displays: name
```

The quotes tell Python: "This is literal text, not a variable reference."

---

## Naming Variables: The Rules

You can't name variables anything you want. Python has rules:

### Rule 1: Variable names must start with a letter or underscore

✓ Valid:
```python
name = "Alice"
_age = 25
myScore = 100
```

✗ Invalid:
```python
25name = "Alice"    # Starts with a number
@username = "Bob"   # Starts with @
```

---

### Rule 2: Variable names can contain letters, numbers, and underscores

✓ Valid:
```python
user_name = "Alice"
score123 = 50
_private = True
```

✗ Invalid:
```python
user-name = "Alice"    # Hyphens not allowed
user name = "Bob"      # Spaces not allowed
user.name = "Charlie"  # Periods not allowed
```

---

### Rule 3: Variable names are case-sensitive

Python treats these as three different variables:

```python
name = "Alice"
Name = "Bob"
NAME = "Charlie"
```

Each is a separate box with a separate label.

---

## Naming Variables: The Convention

Programmers follow a *convention* (not a rule, but a style guide): use lowercase with underscores between words.

This is called **snake_case**.

✓ Recommended (Python style):
```python
first_name = "Alice"
user_age = 25
is_student = True
total_score = 1050
```

✗ Discouraged in Python:
```python
firstName = "Alice"      # camelCase - don't do this in Python
FirstName = "Alice"      # PascalCase - Python uses this for classes
FIRSTNAME = "Alice"      # ALLCAPS - Python uses this for constants
```

Follow the convention. Other Python programmers will expect it.

---

## Summary of Mental Models

1. A **variable** is a labeled box storing a value
2. You create variables with `name = value`
3. Python looks up variables when you use them (no quotes)
4. Text values must have quotes; numbers and true/false don't
5. Variables can change—each `=` replaces the old value
6. Variable names follow rules and conventions
7. Names are case-sensitive

Next: see these concepts in action with examples.
