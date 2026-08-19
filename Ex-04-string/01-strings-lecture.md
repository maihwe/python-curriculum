# Strings: Text Manipulation - Lecture

## Why This Matters

So far, you've worked with text as a *value*:

```python
name = "Alice"
print(name)
```

But text isn't just static data—you can *do things* with it. Think about real programs:

- A login system checks if the username contains a space (not allowed)
- A text editor counts the number of characters you've typed
- A search engine finds words inside documents
- A username validator ensures names are at least 3 characters long

A **string** is Python's name for text. Learning to *manipulate strings* means you can solve real text problems.

This is where text becomes powerful. Instead of just displaying it, you transform it, examine it, and use it to make decisions.

---

## The Mental Model: What Is a String?

A **string** is a sequence of characters.

Think of it like a chain:

```
"Hello"

┌───┬───┬───┬───┬───┐
│ H │ e │ l │ l │ o │
└───┴───┴───┴───┴───┘
```

Each character is connected in order. The string is the entire chain.

In Python, a string is:
- Text surrounded by quotes: `"Hello"` or `'Hello'`
- A sequence: characters appear in a specific order
- Immutable: once created, you can't change individual characters (but you can create new strings)

Strings can contain:
- Letters: `"abc"`
- Numbers: `"123"` (as text, not math)
- Special characters: `"!@#$"`
- Spaces: `"hello world"`
- Empty: `""` (nothing)

---

## The Mental Model: Strings vs. Numbers

This is critical—Python treats `"5"` and `5` completely differently:

**Text string:**
```python
text = "5"
```

**Number:**
```python
number = 5
```

When you combine them with `+`:
- `"5" + "3"` = `"53"` (joining text)
- `5 + 3` = `8` (math)

This is why Type Conversion (the next topic) matters. But for now: **strings are text, numbers are quantities**.

---

## The Mental Model: String Concatenation

You already know this from earlier: combining strings with `+`.

```python
first_name = "Alice"
last_name = "Johnson"
full_name = first_name + " " + last_name
```

Breaking it down:
- `first_name + " "` → combines `"Alice"` and `" "` (space) → `"Alice "`
- `"Alice " + last_name` → combines `"Alice "` and `"Johnson"` → `"Alice Johnson"`

The `+` operator *joins* strings together. This is called **concatenation**.

Notice: You added a space between names. Without it, you'd get `"AliceJohnson"` (no space).

---

## The Mental Model: String Length

Every string has a length—the number of characters.

```python
"Hello"     # 5 characters
"Hi"        # 2 characters
" "         # 1 character (a space)
""          # 0 characters (empty)
"Test 123"  # 8 characters (including the space)
```

You get the length using `len()`:

```python
len("Hello")      # Returns: 5
len("Hi")         # Returns: 2
len("Test 123")   # Returns: 8
```

`len()` counts every character, including spaces and special characters.

---

## The Mental Model: String Indexing

Strings are sequences. You can access individual characters using their position.

```python
word = "Python"

Position:  0  1  2  3  4  5
           P  y  t  h  o  n
```

To get a character at a specific position:

```python
word[0]     # Returns: "P" (first character)
word[1]     # Returns: "y" (second character)
word[5]     # Returns: "n" (last character)
```

**Critical:** Indexing starts at **0**, not 1. This confuses beginners.

- Position 0 = first character
- Position 1 = second character
- Position 2 = third character

And you can use negative indexing to count from the end:

```python
word[-1]    # Last character: "n"
word[-2]    # Second-to-last: "o"
word[-3]    # Third-to-last: "h"
```

---

## The Mental Model: String Slicing

You can get a piece of a string (a slice).

```python
word = "Python"

word[0:2]   # "Py" (from position 0 up to 2, not including 2)
word[2:6]   # "thon" (from position 2 up to 6)
word[1:4]   # "yth" (from position 1 up to 4)
```

The pattern is `string[start:end]`:
- `start`: where to begin (included)
- `end`: where to stop (not included)

This is called **slicing** and it's incredibly useful for extracting parts of strings.

---

## The Mental Model: String Methods

Strings have *methods*—actions you can perform on them.

A method is used like: `string.method_name()`

Some common string methods:

**`upper()`** — make it uppercase
```python
"hello".upper()  # Returns: "HELLO"
```

**`lower()`** — make it lowercase
```python
"HELLO".lower()  # Returns: "hello"
```

**`strip()`** — remove spaces at the beginning and end
```python
"  hello  ".strip()  # Returns: "hello"
```

**`replace(old, new)`** — replace text
```python
"hello world".replace("world", "Python")  # Returns: "hello Python"
```

**`split()`** — break string into pieces
```python
"apple,banana,cherry".split(",")  # Returns: ["apple", "banana", "cherry"]
```

**`find()`** — find a character's position
```python
"hello".find("l")  # Returns: 2 (position of first "l")
```

These methods are tools that save you time. We'll explore them in examples.

---

## The Mental Model: Why Strings Matter

Strings are everywhere in programs:

- User input is always strings (even if they type numbers)
- File contents are strings
- Usernames, passwords, emails are strings
- API responses are strings (often JSON, which is text)
- Data from databases are often strings

Learning to work with strings means you can:
- Validate user input (is it a valid email?)
- Transform data (convert names to usernames)
- Search text (find keywords in documents)
- Extract information (get the domain from an email)

Once you master strings, you unlock a huge range of programming tasks.

---

## Key Concepts to Remember

1. A **string** is a sequence of characters surrounded by quotes
2. **Concatenation** (`+`) joins strings together
3. **Length** (`len()`) counts characters
4. **Indexing** (`string[0]`) gets individual characters
5. **Slicing** (`string[0:3]`) gets parts of strings
6. **Methods** (`string.upper()`, etc.) perform actions on strings
7. Strings are immutable—you can't change them, only create new ones

---

## String Literals vs. String Variables

Important distinction:

```python
"Hello"           # String literal (the actual text)
message = "Hello" # String variable (a box containing text)
```

When you use a variable name (without quotes), Python looks up its value:

```python
message = "Hello"
print(message)     # Prints: Hello (the value)
print("message")   # Prints: message (the literal text)
```

This distinction matters for all string operations.

---

## Preview: String Formatting (Coming Later)

There's a powerful technique called **string formatting** that makes combining strings cleaner:

```python
# Old way (concatenation):
print("Hello, " + name + "! You are " + age + " years old.")

# New way (string formatting - coming later):
print(f"Hello, {name}! You are {age} years old.")
```

Both work. The second is cleaner. We'll learn it after Type Conversion.

---

## Summary

Strings are text. In Python, you can:
- Combine them
- Measure their length
- Access individual characters
- Extract pieces
- Perform actions with methods

These tools let you solve text-based problems. This is the foundation for everything from input validation to data parsing.

Next: see strings in action with real examples.
