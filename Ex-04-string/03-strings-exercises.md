# Strings: Exercises & Practice

## Exercise 1: Simple Concatenation

Create a program that combines two strings.

**Code to write:**
```python
greeting = "Hello"
name = "Alice"
# Combine them with concatenation
```

**Expected output:**
```
Hello Alice
```

**What to do:**
1. Create a file called `concatenation.py`
2. Create two variables with string values
3. Use `+` to combine them
4. Print the result
5. Run it

**Hint:** Don't forget the space between the strings.

---

## Exercise 2: String Length

Create a program that prints a word and its length.

**Expected output:**
```
Python
6
```

**What to do:**
1. Create a file called `string_length.py`
2. Create a variable with a word
3. Use `len()` to get its length
4. Print both the word and its length
5. Run it

**Hint:** `len()` counts every character.

---

## Exercise 3: Accessing Characters

Create a program that prints individual characters from a word.

**Expected output:**
```
First: P
Last: n
Middle: h
```

**Code structure:**
```python
word = "Python"
print("First:", word[0])
print("Last:", word[?])
print("Middle:", word[?])
```

**What to do:**
1. Create a file called `character_access.py`
2. Figure out which positions to use
3. Print the first, last, and middle characters
4. Run it

**Hint:** The first position is 0. The last position is 5 (since the word is 6 characters). The middle would be position 2 or 3.

---

## Exercise 4: Slicing a String

Create a program that extracts parts of a string.

**Expected output:**
```
Pyt
tho
on
```

**What to do:**
1. Create a file called `slicing.py`
2. Create a variable with a word
3. Use slicing `[start:end]` to extract:
   - First 3 characters
   - Middle 3 characters
   - Last 2 characters
4. Print each slice
5. Run it

**Hint:** Remember: `[0:3]` means from 0 up to (but not including) 3.

---

## Exercise 5: Converting to Uppercase

Create a program that takes user input and converts it to uppercase.

**Program interaction:**
```
Enter a word: hello
HELLO
```

**What to do:**
1. Create a file called `to_uppercase.py`
2. Ask the user for input
3. Use `.upper()` to convert it
4. Print the result
5. Run it and test with different words

**Hint:** Use `input()` to get the word, then apply `.upper()`.

---

## Exercise 6: Converting to Lowercase

Create a program that takes user input and converts it to lowercase.

**Program interaction:**
```
Enter a word: HELLO
hello
```

**What to do:**
1. Create a file called `to_lowercase.py`
2. Ask for user input
3. Use `.lower()` to convert it
4. Print the result

**Hint:** This is similar to Exercise 5, but use `.lower()` instead.

---

## Exercise 7: Cleaning Input

Create a program that cleans extra spaces from user input.

**Program interaction:**
```
Enter text:   hello world   
Cleaned: hello world
```

**What to do:**
1. Create a file called `clean_input.py`
2. Ask for input (user can type with spaces at start/end)
3. Use `.strip()` to remove spaces
4. Print original and cleaned versions
5. Run it and verify the spaces are gone

**Hint:** `.strip()` removes whitespace from beginning and end.

---

## Exercise 8: Replacing Text

Create a program that replaces one word with another.

**Expected output:**
```
Original: I like apples
New: I like oranges
```

**What to do:**
1. Create a file called `replace_text.py`
2. Create a sentence
3. Use `.replace("apples", "oranges")` to change it
4. Print both versions
5. Run it

**Hint:** `.replace(old, new)` returns a new string.

---

## Exercise 9: Finding Position

Create a program that finds the position of a character.

**Expected output:**
```
Word: Python
Position of 'o': 4
Position of 'y': 1
```

**What to do:**
1. Create a file called `find_position.py`
2. Create a word
3. Use `.find()` to locate characters
4. Print the results
5. Run it

**Hint:** `.find()` returns the position. Remember: positions start at 0.

---

## Exercise 10: Chaining Methods

Create a program that applies multiple methods to a string.

**Program interaction:**
```
Enter your name: alice johnson
Username: ALICE_JOHNSON
```

**What to do:**
1. Create a file called `chain_methods.py`
2. Get user input
3. Apply `.strip()` to clean spaces
4. Apply `.upper()` to make uppercase
5. Apply `.replace(" ", "_")` to replace spaces with underscores
6. Print the result
7. Run it

**Hint:** You can use the result of one method as input to the next.

---

## Exercise 11: Building a Sentence

Create a program that builds a sentence from parts.

**Program interaction:**
```
Enter subject: Alice
Enter verb: jumped
Enter object: fence
Result: Alice jumped fence
```

**What to do:**
1. Create a file called `build_sentence.py`
2. Ask for three words (subject, verb, object)
3. Combine them into a sentence using concatenation
4. Print the result
5. Run it

**Hint:** Don't forget spaces between words.

---

## Exercise 12: String Analysis

Create a program that analyzes a string and provides information about it.

**Program interaction:**
```
Enter text: Hello World
Length: 11
First character: H
Last character: d
Uppercase: HELLO WORLD
Lowercase: hello world
```

**What to do:**
1. Create a file called `string_analysis.py`
2. Ask for user input
3. Print:
   - The length using `len()`
   - First character using `[0]`
   - Last character using `[-1]`
   - Uppercase version using `.upper()`
   - Lowercase version using `.lower()`
4. Run it and test with different inputs

**Hint:** You're combining everything you've learned in this lesson.

---

## Exercise 13: Debug This

This code has an error. Run it, read the error, and fix it.

```python
message = "Python"
print(message[10])
```

**What to do:**
1. Create a file called `debug_string.py`
2. Copy the code
3. Run it and read the error message
4. Understand why it fails (hint: position doesn't exist)
5. Fix it by using a valid position
6. Run it again

**Hint:** The word "Python" only has positions 0-5. Position 10 doesn't exist.

---

## Exercise 14: Slicing Challenge

Create a program that extracts specific parts of a longer string.

**Code:**
```python
sentence = "The quick brown fox"

# Extract these parts:
# "quick"
# "brown"
# "fox"
# "The quick"
```

**What to do:**
1. Create a file called `slicing_challenge.py`
2. Use slicing to extract each word
3. Figure out the correct positions
4. Print each extraction
5. Run it

**Expected output:**
```
quick
brown
fox
The quick
```

**Hint:** Count the positions carefully. Remember `[start:end]` where end is not included.

---

## Exercise 15: User Input Validation Preview

Create a program that checks if user input is valid.

**Program interaction:**
```
Enter username: alice123
Username: alice123
Length: 8
```

**What to do:**
1. Create a file called `username_validator.py`
2. Ask for a username
3. Print the username
4. Print its length
5. (Later: we'll add logic to check if it's valid. For now, just display it.)

**Hint:** This prepares you for the next topics where you'll make decisions based on string properties.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Did the output match the expected result?
- ✓ Can I explain what each method does?
- ✓ Can I predict what will happen with different input?

---

## Important Observations

**About Strings:**
- They're sequences of characters
- Indexing starts at 0
- Slicing doesn't include the end position
- Methods return new strings (they don't change the original)
- The `in` operator checks if something is in a string

**About Methods:**
- `.upper()` and `.lower()` change case
- `.strip()` removes whitespace from ends
- `.replace()` swaps text
- `.split()` breaks strings apart
- `.find()` locates text

---

## Next Steps

Once you've completed these exercises:

1. You can combine strings
2. You can measure and access string parts
3. You can apply methods to transform strings
4. You understand the difference between strings and what you can do with them
5. You can solve real text problems

You're ready for Topic 5: **Type Conversion**

In Type Conversion, you'll learn how to change strings into numbers and back—this solves the problem from Exercise 8 of Input where `5 + 3 = "53"` (text problem).

Next lesson: making strings become numbers and numbers become strings!
