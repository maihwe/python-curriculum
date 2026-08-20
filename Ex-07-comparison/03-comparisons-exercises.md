# Comparisons: Exercises & Practice

## Exercise 1: Simple Equality

Create a program that compares two numbers for equality.

**Program interaction:**
```
Enter first number: 5
Enter second number: 5
5 == 5? True
```

**What to do:**
1. Create a file called `equality.py`
2. Get two numbers from user
3. Compare them with `==`
4. Print the result
5. Run it and test with equal and unequal numbers

**Hint:** Convert input to `int()`.

---

## Exercise 2: All Comparison Operators

Create a program that uses all six comparison operators on two numbers.

**Program interaction:**
```
Enter first number: 10
Enter second number: 5
10 == 5? False
10 != 5? True
10 > 5? True
10 < 5? False
10 >= 5? True
10 <= 5? False
```

**What to do:**
1. Create a file called `all_comparisons.py`
2. Get two numbers from user
3. Test with all six operators: ==, !=, >, <, >=, <=
4. Print all results
5. Run it

**Hint:** You'll need six print statements.

---

## Exercise 3: Storing Comparison Results

Create a program that stores comparison results in variables.

**Program interaction:**
```
Enter your age: 25
Is adult (>= 18)? True
Is senior (>= 65)? False
```

**What to do:**
1. Create a file called `age_check.py`
2. Get age from user
3. Create two boolean variables:
   - `is_adult = age >= 18`
   - `is_senior = age >= 65`
4. Print both results
5. Run it and test with different ages

**Hint:** Store comparison results directly in variables.

---

## Exercise 4: String Equality

Create a program that compares strings.

**Program interaction:**
```
Enter username: Alice
Is username "Alice"? True
Is username "alice" (lowercase)? False
```

**What to do:**
1. Create a file called `string_equality.py`
2. Get a string from user
3. Compare with == to exact strings
4. Show case-sensitivity
5. Run it

**Hint:** "Alice" and "alice" are different.

---

## Exercise 5: Password Check

Create a program that checks if a password is correct.

**Program interaction:**
```
Enter password: SecretPass123
Is password correct? False
```

(When run again with correct password:)
```
Enter password: MySecretPass
Is password correct? True
```

**What to do:**
1. Create a file called `password_check.py`
2. Set a correct password in your code (e.g., "MySecretPass")
3. Get password from user
4. Compare with `==`
5. Print if correct
6. Run it

**Hint:** Store the correct password in a variable, then compare.

---

## Exercise 6: Range Checking - Single Bound

Create a program that checks if a score is passing.

**Program interaction:**
```
Enter score: 75
Is passing (>= 60)? True
```

**What to do:**
1. Create a file called `passing_score.py`
2. Get score from user
3. Check if `score >= 60`
4. Print result
5. Run it with scores like 50, 60, 75, 100

**Hint:** This prepares for range checking.

---

## Exercise 7: Multiple Bounds (Preview of "and")

Create a program that checks multiple conditions.

**Program interaction:**
```
Enter a number: 15
Is between 10 and 20?
10 <= 15? True
15 <= 20? True
```

**What to do:**
1. Create a file called `between.py`
2. Get a number from user
3. Check `number >= 10` (call it `is_at_least_10`)
4. Check `number <= 20` (call it `is_at_most_20`)
5. Print both
6. Run it

**Hint:** You're checking two conditions separately (we'll combine them next).

---

## Exercise 8: Grading Script

Create a program that determines a grade based on score.

**Program interaction:**
```
Enter score: 85
Score: 85
Is A (>= 90)? False
Is B (>= 80)? True
Is C (>= 70)? True
Is D (>= 60)? True
Is F (< 60)? False
```

**What to do:**
1. Create a file called `grading.py`
2. Get score from user
3. Test multiple grade thresholds
4. Print which grade category it falls in
5. Run it

**Hint:** Multiple comparisons on same value.

---

## Exercise 9: Comparing Strings Alphabetically

Create a program that compares words alphabetically.

**Program interaction:**
```
Enter first word: apple
Enter second word: banana
"apple" < "banana"? True
"apple" > "banana"? False
```

**What to do:**
1. Create a file called `alphabetical.py`
2. Get two words from user
3. Compare with < and >
4. Print results
5. Run it and test with different words

**Hint:** Strings compare using alphabetical order.

---

## Exercise 10: Type Comparison

Create a program that demonstrates type differences.

**Program interaction:**
```
5 == "5"? False
5 == 5? True
"hello" == "hello"? True
"Hello" == "hello"? False
```

**What to do:**
1. Create a file called `type_comparison.py`
2. Create variables of different types
3. Compare them
4. Print results to show when comparisons are true/false
5. Run it

**Hint:** Pay attention to quotes and type differences.

---

## Exercise 11: Real World - Speed Check

Create a program that checks if a speed is within limit.

**Program interaction:**
```
Enter speed (mph): 50
Speed limit: 55 mph
Over limit? False
Speed is safe.
```

Then try 60:
```
Enter speed (mph): 60
Speed limit: 55 mph
Over limit? True
Speed is too fast!
```

**What to do:**
1. Create a file called `speed_check.py`
2. Set speed limit in code (e.g., 55)
3. Get actual speed from user
4. Compare: `is_over = actual_speed > speed_limit`
5. Print appropriate message based on comparison
6. Run it

**Hint:** This is a real-world use case.

---

## Exercise 12: Account Balance Check

Create a program that checks if account has sufficient funds.

**Program interaction:**
```
Account balance: $1000
Withdrawal amount: $500
Sufficient funds? True
Can withdraw.
```

Then try:
```
Account balance: $200
Withdrawal amount: $300
Sufficient funds? False
Insufficient funds!
```

**What to do:**
1. Create a file called `account_check.py`
2. Get balance and withdrawal amount from user
3. Compare: `has_funds = balance >= withdrawal_amount`
4. Print result with appropriate message
5. Run it

**Hint:** Real-world bank check.

---

## Exercise 13: Debug This

This code has an error. Find and fix it.

```python
age = 25
can_vote = age == 18

print("Can vote?", can_vote)
```

**What to do:**
1. Create a file called `debug_comparison.py`
2. Copy the code
3. Run it and predict output (should be False)
4. Fix the logic: should check if age >= 18, not ==18
5. Run it again

**Hint:** You need `>=` not `==`.

---

## Exercise 14: Inventory Check

Create a program that checks if items are in stock.

**Program interaction:**
```
Minimum stock required: 10
Current stock: 5
Low stock? True
Order more items!
```

**What to do:**
1. Create a file called `inventory.py`
2. Set minimum stock in code
3. Get current stock from user
4. Compare: `is_low = current < minimum`
5. Print appropriate message
6. Run it

**Hint:** `<` checks if below minimum.

---

## Exercise 15: User Validation

Create a program that validates a username.

**Program interaction:**
```
Enter username: alice123
Username is "alice123"? True
Exact match: Yes
```

Then try:
```
Enter username: alice
Username is "alice123"? False
Exact match: No
```

**What to do:**
1. Create a file called `username_validation.py`
2. Set required username in code
3. Get user input
4. Compare for exact match
5. Print result
6. Run it

**Hint:** String equality check.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Do comparisons return correct True/False?
- ✓ Did I use the right operator?
- ✓ Can I predict output before running?
- ✓ Do I understand what each operator does?

---

## Important Observations

**About Comparisons:**
- `==` is for comparison, `=` is for assignment
- All six operators are important
- Comparisons always return True or False
- Type matters: 5 ≠ "5"
- Strings compare alphabetically
- Case matters: "Alice" ≠ "alice"

---

## Next Steps

Once you've completed these exercises:

1. You can compare values
2. You understand all six operators
3. You can store comparison results
4. You can use comparisons in real programs
5. You understand type differences in comparisons

You're ready for Topic 8: **If/Else Statements**

If/Else uses comparisons to make decisions. It's where programs become truly dynamic—running different code based on conditions.

Next lesson: making your programs intelligent!
