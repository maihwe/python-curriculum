# Strings: Examples & Demos

## Example 1: String Concatenation (Joining)

**Code:**
```python
first_name = "Alice"
last_name = "Johnson"
full_name = first_name + " " + last_name

print(full_name)
```

**Execution flow:**

Line 1: Store `"Alice"` in `first_name`

Line 2: Store `"Johnson"` in `last_name`

Line 3: Combine them with a space in between, store in `full_name`

Line 4: Print the result

**Output:**
```
Alice Johnson
```

**Key insight:** The `+` operator joins strings. Notice we added `" "` (a space string) in the middle. Without it, we'd get `"AliceJohnson"`.

---

## Example 2: String Length

**Code:**
```python
word = "Python"
length = len(word)

print(word)
print(length)
```

**Execution flow:**

Line 1: Store `"Python"` in `word`

Line 2: Get the length (number of characters) using `len()`, store in `length`

Line 3: Print the word

Line 4: Print the length

**Output:**
```
Python
6
```

**Key insight:** `len()` counts every character. `"Python"` has 6 characters: P-y-t-h-o-n.

---

## Example 3: Accessing Characters (Indexing)

**Code:**
```python
word = "Python"

print(word[0])   # First character
print(word[1])   # Second character
print(word[2])   # Third character
print(word[5])   # Last character
```

**Execution flow:**

- `word[0]` → Position 0 → `"P"` (first character)
- `word[1]` → Position 1 → `"y"` (second character)
- `word[2]` → Position 2 → `"t"` (third character)
- `word[5]` → Position 5 → `"n"` (last character, because positions start at 0)

**Output:**
```
P
y
t
n
```

**Key insight:** Indexing starts at 0. The first character is at position 0, not position 1.

---

## Example 4: Negative Indexing

**Code:**
```python
word = "Python"

print(word[-1])   # Last character
print(word[-2])   # Second-to-last
print(word[-3])   # Third-to-last
```

**Execution flow:**

- `word[-1]` → Last character → `"n"`
- `word[-2]` → Second-to-last → `"o"`
- `word[-3]` → Third-to-last → `"h"`

**Output:**
```
n
o
h
```

**Key insight:** Negative indexing counts from the end. `-1` is the last character, `-2` is second-to-last, etc.

---

## Example 5: String Slicing

**Code:**
```python
word = "Python"

print(word[0:2])   # First 2 characters
print(word[1:4])   # Characters 1, 2, 3
print(word[2:6])   # Characters 2 to end
```

**Execution flow:**

- `word[0:2]` → From position 0 up to (but not including) 2 → `"Py"`
- `word[1:4]` → From position 1 up to (but not including) 4 → `"yth"`
- `word[2:6]` → From position 2 to 6 → `"thon"`

**Output:**
```
Py
yth
thon
```

**Key insight:** Slicing is `[start:end]`. The start is included, the end is not included.

---

## Example 6: String Method - upper()

**Code:**
```python
message = "hello world"

uppercase = message.upper()

print(message)
print(uppercase)
```

**Execution flow:**

Line 1: Store `"hello world"` in `message`

Line 3: Call the `upper()` method on `message`, store result in `uppercase`

Line 5: Print original message

Line 6: Print uppercase version

**Output:**
```
hello world
HELLO WORLD
```

**Key insight:** Methods are actions you perform on strings. The `.upper()` method creates a new string with all uppercase letters.

---

## Example 7: String Method - lower()

**Code:**
```python
message = "HELLO WORLD"

lowercase = message.lower()

print(message)
print(lowercase)
```

**Execution flow:**

Line 1: Store `"HELLO WORLD"` in `message`

Line 3: Call the `lower()` method, store result

**Output:**
```
HELLO WORLD
hello world
```

**Key insight:** `.lower()` creates a new string with all lowercase letters.

---

## Example 8: String Method - strip()

**Code:**
```python
message = "   hello   "

cleaned = message.strip()

print("Original: '" + message + "'")
print("Cleaned: '" + cleaned + "'")
```

**Note:** The quotes help you see the spaces clearly.

**Execution flow:**

Line 1: Store text with spaces on both ends

Line 3: Call `.strip()` to remove spaces at beginning and end

**Output:**
```
Original: '   hello   '
Cleaned: 'hello'
```

**Key insight:** `.strip()` removes whitespace (spaces, tabs, newlines) from the beginning and end of a string. Useful for cleaning user input.

---

## Example 9: String Method - replace()

**Code:**
```python
sentence = "I like apples"

new_sentence = sentence.replace("apples", "oranges")

print(sentence)
print(new_sentence)
```

**Execution flow:**

Line 1: Store original sentence

Line 3: Call `.replace()` to swap one word for another

**Output:**
```
I like apples
I like oranges
```

**Key insight:** `.replace(old, new)` finds the text you specify and replaces it. It returns a new string without changing the original.

---

## Example 10: String Method - split()

**Code:**
```python
fruits = "apple,banana,cherry"

fruit_list = fruits.split(",")

print(fruits)
print(fruit_list)
```

**Execution flow:**

Line 1: Store a string with items separated by commas

Line 3: Call `.split(",")` to break the string into pieces at each comma

**Output:**
```
apple,banana,cherry
['apple', 'banana', 'cherry']
```

**Key insight:** `.split()` breaks a string into a list (we'll learn lists soon). Very useful for parsing data.

---

## Example 11: String Method - find()

**Code:**
```python
word = "hello"

position = word.find("l")

print(word)
print("Position of 'l':", position)
```

**Execution flow:**

Line 1: Store `"hello"`

Line 3: Find the position of the first "l"

**Output:**
```
hello
Position of 'l': 2
```

**Key insight:** `.find()` returns the position of the first occurrence of a character. Remember: positions start at 0. Position 2 is the third character.

---

## Example 12: Combining Multiple Operations

**Code:**
```python
user_input = "  john doe  "

# Clean it
cleaned = user_input.strip()

# Make it uppercase
uppercase = cleaned.upper()

# Replace space with underscore
username = uppercase.replace(" ", "_")

print("Original:", user_input)
print("Final username:", username)
```

**Execution flow:**

Line 1: User enters `"  john doe  "` (with extra spaces)

Line 4: `.strip()` removes spaces → `"john doe"`

Line 7: `.upper()` makes uppercase → `"JOHN DOE"`

Line 10: `.replace()` replaces space with underscore → `"JOHN_DOE"`

**Output:**
```
Original:   john doe  
Final username: JOHN_DOE
```

**Key insight:** You can chain operations. Each method takes the result of the previous one.

---

## Example 13: String Concatenation with Input

**Code:**
```python
name = input("What is your name? ")
greeting = "Hello, " + name.upper() + "!"

print(greeting)
```

**Program interaction:**

```
What is your name? alice
Hello, ALICE!
```

**Execution flow:**

Line 1: Get user input, store in `name` → `"alice"`

Line 2: Combine text, uppercase the name, store in `greeting`

Line 4: Print the result

**Output:**
```
Hello, ALICE!
```

**Key insight:** You can apply methods to variables. `name.upper()` applies the method to whatever is in `name`.

---

## Example 14: String in Conditional (Preview)

This is a preview of what comes next—checking if a string contains something.

**Code:**
```python
word = "Python"

if "y" in word:
    print("'y' is in the word")
else:
    print("'y' is not in the word")
```

**Output:**
```
'y' is in the word
```

**Key insight:** The `in` operator checks if a character or substring exists in a string. This is a powerful tool.

---

## Common Questions

**Q: Can I use single or double quotes?**

A: Yes. `"hello"` and `'hello'` are identical. Pick one and be consistent.

**Q: What if I use quotes inside a string?**

A: Use the opposite quote type:
```python
message = 'He said "Hi"'   # Double quotes inside single quotes
message = "It's here"      # Single quote inside double quotes
```

**Q: Are methods the same as functions?**

A: Similar but different. Methods are called on objects: `string.method()`. Functions are called on their own: `function()`. We'll clarify this later.

**Q: Do string methods change the original string?**

A: No. Strings are immutable. Methods return new strings. The original stays the same.

```python
message = "hello"
message.upper()    # Returns "HELLO" but doesn't change message
print(message)     # Still prints: hello
```

---

## Summary of Examples

- Concatenation (`+`) joins strings
- Length (`len()`) counts characters
- Indexing (`[n]`) gets individual characters
- Slicing (`[start:end]`) gets parts of strings
- Methods (`.upper()`, `.lower()`, etc.) perform actions
- The `in` operator checks if something is in a string

Next: practice these concepts with exercises.
