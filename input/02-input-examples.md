# Input: Examples & Demos

## Example 1: Simple Input

**Code:**
```python
name = input("What is your name? ")
print(name)
```

**What happens when you run it:**

Your screen shows:
```
What is your name? 
```

The program waits. You type `Alice` and press Enter. Then:

```
What is your name? Alice
Alice
```

**Execution flow:**

Line 1: Display the prompt `What is your name? ` and wait for input

User types: `Alice` and presses Enter

Python stores `"Alice"` in the variable `name`

Line 2: Print what's in `name` → displays `Alice`

**Key insight:** `input()` displays a question and waits. The user decides when the program continues.

---

## Example 2: Input Stored in Variable, Used Multiple Times

**Code:**
```python
city = input("What is your favorite city? ")
print(city)
print(city)
print(city)
```

**Program interaction:**

```
What is your favorite city? Paris
Paris
Paris
Paris
```

**Execution flow:**

Line 1: Ask user for their favorite city and store it in `city`

User types: `Paris`

Lines 2-4: Print the variable three times

**Key insight:** Once you have input stored in a variable, you can use it as many times as you need, just like any other variable.

---

## Example 3: Multiple Inputs

**Code:**
```python
first_name = input("First name: ")
last_name = input("Last name: ")
age = input("Age: ")

print(first_name)
print(last_name)
print(age)
```

**Program interaction:**

```
First name: Alice
Last name: Johnson
Age: 28
Alice
Johnson
28
```

**Execution flow:**

Line 1: Ask for first name → user types `Alice` → stored

Line 2: Ask for last name → user types `Johnson` → stored

Line 3: Ask for age → user types `28` → stored

Lines 4-6: Print each piece of information

**Key insight:** You can ask for multiple pieces of information. The program pauses at each `input()` line and waits for the user.

---

## Example 4: Input and Print Together

**Code:**
```python
name = input("What is your name? ")
print("Hello, " + name)
```

**Program interaction:**

```
What is your name? Alice
Hello, Alice
```

**Execution flow:**

Line 1: Ask for name → user types `Alice` → stored in `name`

Line 2: Print `"Hello, "` combined with the value in `name`

**Key insight:** This is combining input with variables. You get information from the user and immediately use it.

---

## Example 5: Using Input Multiple Times

**Code:**
```python
person1 = input("First person's name: ")
person2 = input("Second person's name: ")

print(person1 + " and " + person2 + " are friends")
```

**Program interaction:**

```
First person's name: Alice
Second person's name: Bob
Alice and Bob are friends
```

**Execution flow:**

Line 1: Ask for first person → user types `Alice`

Line 2: Ask for second person → user types `Bob`

Line 3: Print a sentence combining both inputs

**Key insight:** You can ask for multiple pieces of input and then combine them in output.

---

## Example 6: Input Prompts Matter

Good prompts tell the user exactly what to enter.

**Code:**
```python
favorite_color = input("What is your favorite color? ")
favorite_animal = input("What is your favorite animal? ")
favorite_food = input("What is your favorite food? ")

print("Your favorites:")
print(favorite_color)
print(favorite_animal)
print(favorite_food)
```

**Program interaction:**

```
What is your favorite color? blue
What is your favorite animal? dog
What is your favorite food? pizza
Your favorites:
blue
dog
pizza
```

**Execution flow:**

Lines 1-3: Ask for three pieces of information

Lines 4-7: Display them nicely

**Key insight:** Clear prompts help users understand what information to provide.

---

## Example 7: Input as Text (Important!)

Remember: `input()` always returns text, even if the user types numbers.

**Code:**
```python
number1 = input("Enter a number: ")
number2 = input("Enter another number: ")

print(number1 + number2)
```

**Program interaction:**

```
Enter a number: 5
Enter another number: 3
53
```

**Wait, what?** You entered `5` and `3`, but got `53`, not `8`!

**Why?** Because `input()` returned the *text* `"5"` and `"3"`, not numbers. When you combine text with `+`, it joins them together, not adds them.

- `"5"` + `"3"` = `"53"` (text joining)
- `5` + `3` = `8` (math)

**Key insight:** This is a critical distinction. `input()` always gives text. If you need to do math, you'll need to convert the text to a number (we'll learn that soon).

---

## Example 8: Input and Variables Together (Full Example)

**Code:**
```python
print("Welcome to the Profile Maker!")
print()

name = input("What is your name? ")
age = input("How old are you? ")
city = input("What city are you from? ")

print()
print("Your Profile:")
print("Name: " + name)
print("Age: " + age)
print("City: " + city)
```

**Program interaction:**

```
Welcome to the Profile Maker!

What is your name? Alice
How old are you? 28
What city are you from? New York

Your Profile:
Name: Alice
Age: 28
City: New York
```

**Execution flow:**

Lines 1-2: Welcome message

Lines 4-6: Collect three pieces of input

Lines 8-11: Display them in a nice format

**Key insight:** This demonstrates the full power of input. You collect information from the user, store it in variables, and use it to create personalized output.

---

## Common Questions About Input

**Q: What if the user just presses Enter without typing anything?**

A: `input()` stores an empty string (nothing). If you try to use it, it's just empty text.

**Q: Can I ask for a number with `input()`?**

A: Yes, but `input()` gives you text. If you need to do math with it, you'll need to convert it (coming soon).

**Q: What if the user types something I didn't expect?**

A: `input()` takes whatever the user types. No validation happens automatically.

**Q: How do I know if a user actually typed something?**

A: You'll learn validation techniques later. For now, assume the user will type something reasonable.

**Q: Can I have a multi-line prompt?**

A: Yes, use `\n` inside the string (we'll learn this later). For now, keep prompts on one line.

---

## Summary of Examples

- `input()` displays a question and waits for the user
- The user's answer is stored in a variable
- `input()` always returns text
- You can ask for multiple pieces of input
- Input works perfectly with variables and print
- Good prompts tell users exactly what to enter

Next: practice these concepts with exercises.
