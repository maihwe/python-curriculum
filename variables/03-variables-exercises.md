# Variables: Exercises & Practice

## Exercise 1: Create and Print a Variable

Create a variable to store your favorite color. Print it.

**Expected output:**
```
blue
```

(Replace "blue" with your actual favorite color.)

**What to do:**
1. Create a file called `color.py`
2. Create a variable called `favorite_color` with your favorite color
3. Print the variable
4. Run it

**Hint:** Remember to use quotes around the color name.

---

## Exercise 2: Multiple Variables

Create three variables:
- One for your name
- One for your age
- One for your favorite food

Print all three, each on its own line.

**Expected output:**
```
Alice
25
Pizza
```

**What to do:**
1. Create a file called `about_me.py`
2. Create three variables (use snake_case names)
3. Print each variable on its own line
4. Run it

**Hint:** Each `print()` statement creates a new line.

---

## Exercise 3: Variables Change

Create a variable `points` and set it to `0`. Print it. Then change it to `100`. Print it again.

**Expected output:**
```
0
100
```

**What to do:**
1. Create a file called `points.py`
2. Create a variable `points = 0` and print it
3. Change `points` to `100`
4. Print it again
5. Run it

**Hint:** Reassigning a variable with `=` replaces the old value.

---

## Exercise 4: Debug This

This code has an error. Run it, read the error message, and fix it.

```python
city = London
print(city)
```

After you fix it, it should print:
```
London
```

**What to do:**
1. Create a file called `debug_city.py`
2. Copy the broken code
3. Run it and read the error
4. Fix it
5. Run it again to verify

**Hint:** The error message will tell you exactly what's wrong. Look for quotes.

---

## Exercise 5: Reuse Variables Multiple Times

Create a variable `greeting` with the text `"Hello!"`. Print it five times.

**Expected output:**
```
Hello!
Hello!
Hello!
Hello!
Hello!
```

**What to do:**
1. Create a file called `greeting.py`
2. Create a variable `greeting = "Hello!"`
3. Write five `print(greeting)` statements
4. Run it

**Hint:** You only create the variable once, but use it five times.

---

## Exercise 6: Spot the Errors

For each piece of code, predict what error will occur. Then run it to verify. Then fix it.

**Code A:**
```python
my_name = "Alice"
print(my name)
```

**Code B:**
```python
score = 100
print(scor)
```

**Code C:**
```python
print(username)
username = "Bob"
```

**What to do:**

For each code:
1. Create a file (`error_a.py`, `error_b.py`, `error_c.py`)
2. Copy the broken code
3. Before running, write down what error you predict
4. Run it
5. Compare your prediction to the actual error
6. Fix the code
7. Run it again to verify

**Hint:** Read the error messages carefully. They tell you exactly what Python doesn't understand.

---

## Exercise 7: Create Variables for a Story

Create variables for a character in a story:
- `character_name` — the character's name
- `character_age` — their age
- `character_job` — what they do

Then print them, each on its own line.

**Example output:**
```
Alice
30
Teacher
```

**What to do:**
1. Create a file called `character.py`
2. Create three variables (use snake_case)
3. Print each one
4. Run it

**Hint:** Choose realistic values for your character.

---

## Exercise 8: Variable Name Validation

Which of these are valid variable names? Write them down first. Then create a Python file and test each one to see if Python accepts it.

```
my_score
2ndPlace
first_name
user_name_1
_private
MyVariable
my score
is_available
special$char
name-1
```

**What to do:**
1. Look at each name and decide if it's valid based on Python's rules
2. Create a file called `test_names.py`
3. Try to create each one:
```python
my_score = 100
2ndPlace = 50
# ... etc
```
4. See which ones Python rejects
5. Read the error messages

**Challenge:** Fix the invalid names by renaming them to follow Python's rules and snake_case convention.

---

## Exercise 9: Change and Reuse

Create a variable, print it, change it, print it again. Do this three times with three different variables.

**Example output:**
```
0
100
Alice
Bob
Monday
Friday
```

**What to do:**
1. Create a file called `change_and_reuse.py`
2. For three different variables:
   - Create the variable with an initial value
   - Print it
   - Change it to a new value
   - Print it again
3. Run it

**Hint:** Each variable goes through the same cycle: create → print → change → print.

---

## Exercise 10: Print with Commas

In the examples, you saw this:

```python
print("Text", variable)
```

This prints both the text and the variable's value, separated by a space.

Try this:

**Code:**
```python
name = "Alice"
age = 25
city = "New York"

print("Name:", name)
print("Age:", age)
print("City:", city)
```

**What to do:**
1. Create a file called `print_with_commas.py`
2. Create three variables
3. Use `print()` with commas to display them nicely
4. Run it

**Expected output:**
```
Name: Alice
Age: 25
City: New York
```

**Key insight:** This is a preview of something more powerful coming next. For now, know that commas in `print()` separate things with spaces.

---

## Exercise 11: Fix the Logic Error

This code runs without errors, but the output is wrong. Figure out what's wrong and fix it.

```python
first_name = "Alice"
last_name = "Johnson"
temp = first_name
first_name = last_name
last_name = temp

print(first_name)
print(last_name)
```

**Expected output:**
```
Johnson
Alice
```

**What to do:**
1. Create a file called `logic_error.py`
2. Copy the code and run it
3. Look at the output
4. Figure out what's happening
5. Verify the output matches the expected output

**Hint:** This is actually working correctly—it's demonstrating "swapping" values. The output should be `Johnson` then `Alice`. If you got different output, something went wrong.

---

## Exercise 12: Multiple Assignments

Create three variables for items and their prices. Then print them in a nice format.

**Example code:**
```python
item1 = "Apple"
price1 = 1.50

item2 = "Banana"
price2 = 0.75

item3 = "Orange"
price3 = 2.00

print(item1, "-", price1)
print(item2, "-", price2)
print(item3, "-", price3)
```

**What to do:**
1. Create a file called `shopping.py`
2. Follow the example (or create your own items)
3. Use `print()` with commas and hyphens to format nicely
4. Run it

**Expected output:**
```
Apple - 1.5
Banana - 0.75
Orange - 2.0
```

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Did the output match what was expected?
- ✓ Did I use proper variable naming (snake_case)?
- ✓ Can I explain what each line does?
- ✓ Do I understand why the variable name matters?

If you got an error, read it carefully. It's telling you exactly what to fix.

---

## Next Steps

Once you've completed these exercises:

1. You can create variables with correct syntax
2. You can use variables multiple times
3. You can change variables
4. You understand variable naming rules
5. You can read and fix error messages
6. You understand the difference between variable names and text

You're ready for the next concept: **Input** — how to ask the user to enter information. This is where variables become truly powerful.
