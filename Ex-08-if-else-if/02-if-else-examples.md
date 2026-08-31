# If/Else: Examples & Demos

## Example 1: Simple If Statement

**Code:**
```python
age = 25

if age >= 18:
    print("You are an adult")
```

**Execution flow:**

Line 1: `age = 25`

Line 3: Check: is `25 >= 18`? → True

Line 4: The condition is true, so print the message

**Output:**
```
You are an adult
```

**What if age was 15?**

```python
age = 15

if age >= 18:
    print("You are an adult")
```

Line 3: Check: is `15 >= 18`? → False

Line 4: The condition is false, so skip this block

**Output:**
```
(nothing printed)
```

**Key insight:** If block only runs if condition is true.

---

## Example 2: If/Else Statement

**Code:**
```python
age = 15

if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

**Execution flow:**

Line 1: `age = 15`

Line 3: Check: is `15 >= 18`? → False

Line 4: Condition is false, skip this block

Line 5-6: Run the else block

**Output:**
```
You are a minor
```

**Key insight:** Exactly one block runs. If true → first block. If false → else block.

---

## Example 3: If/Elif/Else

**Code:**
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

**Execution flow:**

Line 1: `score = 85`

Line 3: Is `85 >= 90`? → False, skip this block

Line 5: Is `85 >= 80`? → True, run this block

Line 6: Print "B - Good"

Line 7-11: Skip (we already found a match)

**Output:**
```
B - Good
```

**Key insight:** Elif checks another condition. As soon as one is true, we stop checking.

---

## Example 4: Password Check

**Code:**
```python
password = input("Enter password: ")

if password == "secret":
    print("Access granted!")
else:
    print("Access denied!")
```

**Program interaction (correct):**
```
Enter password: secret
Access granted!
```

**Program interaction (incorrect):**
```
Enter password: wrong
Access denied!
```

**Key insight:** Real-world use: comparing user input to correct value.

---

## Example 5: Multiple Conditions with Nested If

**Code:**
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

**Execution flow:**

Line 1-2: Set variables

Line 4: Is `25 >= 18`? → True

Line 5: (Inside the if) Is `has_license` true? → True

Line 6: Print "You can drive"

Lines 8-11: Skip

**Output:**
```
You can drive
```

**What if has_license was False?**

Line 5: Is `has_license` true? → False

Lines 6: Skip

Line 8: Print "You need a license"

**Output:**
```
You need a license
```

**Key insight:** Nested if/else for multiple conditions.

---

## Example 6: Comparing Strings

**Code:**
```python
username = input("Enter username: ")

if username == "admin":
    print("Welcome, admin!")
elif username == "guest":
    print("Welcome, guest!")
else:
    print("Unknown user")
```

**Program interaction:**
```
Enter username: admin
Welcome, admin!
```

**Key insight:** If/else works with any comparison.

---

## Example 7: Comparing Numbers (Range Check)

**Code:**
```python
score = int(input("Enter score: "))

if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else:
    print("F")
```

**Program interaction:**
```
Enter score: 85
B
```

**Key insight:** Multiple elif allows checking many ranges.

---

## Example 8: Boolean Comparison

**Code:**
```python
age = 25
is_adult = age >= 18

if is_adult:
    print("You are an adult")
else:
    print("You are a minor")
```

**Output:**
```
You are an adult
```

**Key insight:** Boolean variables can be used directly in if statements.

---

## Example 9: Checking if Not Equal

**Code:**
```python
color = input("What is your favorite color? ")

if color != "red":
    print("That's not red")
else:
    print("You like red!")
```

**Program interaction:**
```
What is your favorite color? blue
That's not red
```

**Key insight:** `!=` checks if NOT equal.

---

## Example 10: Checking Multiple Conditions (Preview - and/or coming next)

**Code:**
```python
age = 25
has_license = True

if age >= 18:
    if has_license:
        print("Can drive")
```

**Output:**
```
Can drive
```

**Note:** This is nested if. Later, you can use `and` to combine conditions.

**Key insight:** Nested if/else for multiple conditions.

---

## Example 11: Real-World - Login System

**Code:**
```python
stored_username = "alice"
stored_password = "secret123"

username = input("Username: ")
password = input("Password: ")

if username == stored_username:
    if password == stored_password:
        print("Login successful!")
    else:
        print("Wrong password")nb n
else:
    print("User not found")
```

**Program interaction (success):**
```
Username: alice
Password: secret123
Login successful!
```

**Program interaction (wrong password):**
```
Username: alice
Password: wrong
Wrong password
```

**Program interaction (user not found):**
```
Username: bob
Password: anything
User not found
```

**Key insight:** Real-world nested if/else for login validation.

---

## Example 12: Real-World - Bank Withdrawal

**Code:**
```python
balance = 1000
withdrawal = int(input("Enter withdrawal amount: "))

if withdrawal > balance:
    print("Insufficient funds")
elif withdrawal <= 0:
    print("Invalid amount")
else:
    balance = balance - withdrawal
    print("Withdrawal successful")
    print("New balance:", balance)
```

**Program interaction (success):**
```
Enter withdrawal amount: 200
Withdrawal successful
New balance: 800
```

**Program interaction (insufficient):**
```
Enter withdrawal amount: 2000
Insufficient funds
```

**Key insight:** Multiple conditions in sequence.

---

## Example 13: Real-World - Temperature Control

**Code:**
```python
temperature = int(input("Enter temperature: "))

if temperature < 60:
    print("Turn on heater")
elif temperature > 85:
    print("Turn on air conditioning")
else:
    print("Temperature is comfortable")
```

**Program interaction (cold):**
```
Enter temperature: 50
Turn on heater
```

**Program interaction (hot):**
```
Enter temperature: 90
Turn on air conditioning
```

**Program interaction (comfortable):**
```
Enter temperature: 72
Temperature is comfortable
```

**Key insight:** Three different outcomes based on ranges.

---

## Example 14: Real-World - Coupon Code Validator

**Code:**
```python
coupon = input("Enter coupon code: ")
price = 100

if coupon == "SAVE10":
    discount = price * 0.10
    final_price = price - discount
    print("Coupon valid! Save $" + str(discount))
    print("Final price: $" + str(final_price))
elif coupon == "SAVE20":
    discount = price * 0.20
    final_price = price - discount
    print("Coupon valid! Save $" + str(discount))
    print("Final price: $" + str(final_price))
else:
    print("Invalid coupon code")
```

**Program interaction:**
```
Enter coupon code: SAVE10
Coupon valid! Save $10.0
Final price: $90.0
```

**Key insight:** If/elif/else with calculations.

---

## Example 15: Common Mistake - Indentation

**Wrong:**
```python
age = 20

if age >= 18:
print("Adult")      # ERROR: Not indented!
```

**Correct:**
```python
age = 20

if age >= 18:
    print("Adult")  # Properly indented
```

**Key insight:** Indentation is critical. Python will error without it.

---

## Summary of Examples

- If statement: do something if true
- If/else: do one thing if true, another if false
- If/elif/else: check multiple conditions in sequence
- Nested if: conditions within conditions
- Always indent code inside if/else blocks
- String and number comparisons work the same way
- Real-world uses: login, validation, calculations

Next: practice with exercises.
