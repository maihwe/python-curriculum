# If/Else: Exercises & Practice

## Exercise 1: Simple If Statement

Create a program that prints a message if a condition is true.

**Program interaction:**
```
Enter age: 25
You are an adult
```

**What to do:**
1. Create a file called `simple_if.py`
2. Get age from user
3. If age >= 18, print "You are an adult"
4. Run it with different ages

**Hint:** Only print if condition is true.

---

## Exercise 2: If/Else Statement

Create a program that runs different code based on a condition.

**Program interaction (adult):**
```
Enter age: 25
You are an adult
```

**Program interaction (minor):**
```
Enter age: 15
You are a minor
```

**What to do:**
1. Create a file called `if_else_age.py`
2. Get age from user
3. If age >= 18, print "You are an adult"
4. Else, print "You are a minor"
5. Run it

**Hint:** One block runs if true, other if false.

---

## Exercise 3: String Comparison

Create a program that checks if a password is correct.

**Program interaction (correct):**
```
Enter password: secret
Access granted!
```

**Program interaction (wrong):**
```
Enter password: wrong
Access denied!
```

**What to do:**
1. Create a file called `password.py`
2. Set correct password in code (e.g., "secret")
3. Get password from user
4. If it matches, print "Access granted!"
5. Else, print "Access denied!"

**Hint:** Use == to compare strings.

---

## Exercise 4: Multiple Conditions with Elif

Create a program that grades a score.

**Program interaction:**
```
Enter score: 85
Grade: B
```

Grades:
- >= 90: A
- >= 80: B
- >= 70: C
- >= 60: D
- < 60: F

**What to do:**
1. Create a file called `grading.py`
2. Get score from user (convert to int)
3. Use if/elif/else to determine grade
4. Print the grade
5. Run it with different scores

**Hint:** Check conditions in order from highest to lowest.

---

## Exercise 5: Nested If/Else

Create a program that checks two conditions.

**Program interaction (can drive):**
```
Enter age: 25
Do you have a driver's license? (yes/no): yes
You can drive!
```

**Program interaction (too young):**
```
Enter age: 15
Do you have a driver's license? (yes/no): yes
You are too young to drive
```

**What to do:**
1. Create a file called `nested_if.py`
2. Get age from user
3. If age >= 16:
   - Get license status
   - If has license, print "You can drive!"
   - Else, print "You need a license"
4. Else, print "You are too young to drive"

**Hint:** Nested if/else goes inside another if/else.

---

## Exercise 6: Comparing Numbers

Create a program that compares two numbers.

**Program interaction:**
```
Enter first number: 10
Enter second number: 5
10 is greater than 5
```

**What to do:**
1. Create a file called `compare_numbers.py`
2. Get two numbers from user
3. If first > second, print "first is greater than second"
4. Elif second > first, print "second is greater than first"
5. Else, print "They are equal"

**Hint:** Test all three cases.

---

## Exercise 7: Real World - Discounts

Create a program that calculates discounts based on purchase amount.

**Program interaction:**
```
Enter purchase amount: $150
Discount: 10%
Final price: $135.0
```

Discount rules:
- >= $100: 10% off
- >= $50: 5% off
- < $50: No discount

**What to do:**
1. Create a file called `discount.py`
2. Get purchase amount from user (convert to float)
3. Use if/elif/else to determine discount percentage
4. Calculate discount amount
5. Calculate final price
6. Print results

**Hint:** percentage_off = amount * (percentage / 100)

---

## Exercise 8: Even or Odd

Create a program that checks if a number is even or odd.

**Program interaction:**
```
Enter a number: 7
7 is odd
```

**What to do:**
1. Create a file called `even_odd.py`
2. Get a number from user
3. Use modulo: if num % 2 == 0, it's even
4. Else, it's odd
5. Print result

**Hint:** num % 2 gives remainder. 0 means even, 1 means odd.

---

## Exercise 9: Real World - Age Restrictions

Create a program that checks what content a user can access.

**Program interaction:**
```
Enter your age: 16
Your age: 16
Can watch PG-13? True
Can watch R-rated? False
Can watch NC-17? False
```

**What to do:**
1. Create a file called `age_restrictions.py`
2. Get age from user
3. Check various age restrictions:
   - PG-13: age >= 10 (or always available)
   - R-rated: age >= 17
   - NC-17: age >= 18
4. Print what they can watch
5. Run it with different ages

**Hint:** Multiple if statements (not elif, since they're not mutually exclusive).

---

## Exercise 10: Real World - Store Hours

Create a program that checks if store is open.

**Program interaction:**
```
Enter hour (0-23): 15
Store is open (9am-6pm)
```

**Program interaction (closed):**
```
Enter hour (0-23): 8
Store is closed
```

**What to do:**
1. Create a file called `store_hours.py`
2. Get hour from user (0-23 format)
3. If hour >= 9 and hour < 18, print "Store is open"
4. Else, print "Store is closed"
5. Run it

**Hint:** Need to check if hour is in range 9-17 (before 6pm).

---

## Exercise 11: Real World - Login System

Create a program that validates username and password.

**Program interaction (success):**
```
Enter username: alice
Enter password: secret123
Login successful!
```

**Program interaction (wrong password):**
```
Enter username: alice
Enter password: wrong
Wrong password
```

**Program interaction (user not found):**
```
Enter username: bob
Enter password: anything
User not found
```

**What to do:**
1. Create a file called `login.py`
2. Set correct username and password in code
3. Get input from user
4. If username matches:
   - If password matches: print "Login successful!"
   - Else: print "Wrong password"
5. Else: print "User not found"

**Hint:** Nested if/else for two validations.

---

## Exercise 12: Debug This

This code has a logic error. Find and fix it.

```python
score = 85

if score >= 90:
    print("A")
if score >= 80:
    print("B")
if score >= 70:
    print("C")
```

**What to do:**
1. Create a file called `debug_if.py`
2. Copy the code
3. Run it - notice it prints "B" and "C" (both!)
4. Fix it by using elif instead of multiple if statements
5. Run it again - should only print "B"

**Hint:** The issue is using multiple if instead of if/elif/else. Multiple if statements all run.

---

## Exercise 13: Coupon Validator

Create a program that validates coupon codes.

**Program interaction (valid):**
```
Enter coupon code: SAVE10
Coupon valid!
You save 10%
```

**Program interaction (invalid):**
```
Enter coupon code: INVALID
Invalid coupon code
```

**What to do:**
1. Create a file called `coupon.py`
2. Set valid coupons in your code (e.g., "SAVE10", "SAVE20")
3. Get coupon from user
4. Check if it matches valid coupons
5. Print appropriate message
6. Run it

**Hint:** Use elif for multiple valid coupons.

---

## Exercise 14: Number Range Checker

Create a program that checks if a number is in a range.

**Program interaction:**
```
Enter a number: 15
15 is between 1 and 100
```

**Program interaction (out of range):**
```
Enter a number: 150
150 is outside the range
```

**What to do:**
1. Create a file called `range_check.py`
2. Get a number from user
3. If number is between 1 and 100, print it's in range
4. Else, print it's outside the range
5. Run it

**Hint:** Check if num >= 1 and num <= 100.

---

## Exercise 15: Real World - ATM Withdrawal

Create a program that simulates ATM withdrawal with validations.

**Program interaction (success):**
```
Current balance: $1000
Enter withdrawal amount: $200
Withdrawal successful
New balance: $800
```

**Program interaction (insufficient funds):**
```
Current balance: $1000
Enter withdrawal amount: $2000
Insufficient funds
```

**Program interaction (invalid amount):**
```
Current balance: $1000
Enter withdrawal amount: $-50
Invalid amount
```

**What to do:**
1. Create a file called `atm.py`
2. Set starting balance in code
3. Get withdrawal amount from user
4. Check if amount is valid (> 0)
5. If valid, check if funds are sufficient
6. If sufficient, complete withdrawal and show new balance
7. Print appropriate messages for each case

**Hint:** Check validity first, then sufficient funds.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Does it print the correct message?
- ✓ Did I indent correctly?
- ✓ Did I use if/elif/else correctly?
- ✓ Can I predict the output before running?
- ✓ Does it handle all cases?

---

## Important Observations

**About If/Else:**
- Exactly one block runs (unless it's nested)
- Always indent the code inside blocks
- Use == for comparison, not =
- Elif checks another condition if first is false
- You can nest if/else inside if/else
- Order matters with elif (check specific conditions first)

---

## Completed!

You've now learned:
1. Hello World (executing code)
2. Variables (storing data)
3. Input (getting user data)
4. Strings (working with text)
5. Type Conversion (changing data types)
6. Arithmetic (doing math)
7. Comparisons (testing relationships)
8. If/Else (making decisions)

**This is a complete foundation!** You can now write real programs that:
- Get input from users
- Store and manipulate data
- Make decisions based on conditions
- Perform calculations
- Display results

You're ready to sell this as a course!

Next topics (when you're ready):
- Logical operators (and, or, not)
- Loops (while, for)
- Lists and dictionaries
- Functions
- And much more!
