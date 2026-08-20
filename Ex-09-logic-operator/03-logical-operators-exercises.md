# Logical Operators: Exercises & Practice

## Exercise 1: Simple `and` Statement

Create a program that checks if both conditions are true.

**Program interaction:**
```
Enter age: 25
Do you have a license? (yes/no): yes
Can drive? True
```

**What to do:**
1. Create a file called `and_operator.py`
2. Get age from user
3. Get license status from user
4. Check if both are valid
5. Print result

**Hint:** Use `and` to combine conditions.

---

## Exercise 2: Simple `or` Statement

Create a program that checks if at least one condition is true.

**Program interaction:**
```
Do you have admin role? (yes/no): no
Do you have owner role? (yes/no): yes
Has access? True
```

**What to do:**
1. Create a file called `or_operator.py`
2. Get two role statuses from user
3. Check if at least one is true
4. Print result

**Hint:** Use `or` to combine conditions.

---

## Exercise 3: `not` Operator

Create a program that uses `not` to reverse a condition.

**Program interaction:**
```
Is user banned? (yes/no): no
Can access platform? True
```

**What to do:**
1. Create a file called `not_operator.py`
2. Get banned status from user
3. Use `not` to reverse it
4. Print result

**Hint:** `not` flips the boolean.

---

## Exercise 4: Multiple Conditions with `and`

Create a program that checks three conditions.

**Program interaction:**
```
Age: 25
License: yes
Insurance: yes
Can drive legally? True
```

**What to do:**
1. Create a file called `multiple_and.py`
2. Get three inputs (age, license, insurance)
3. Check all three with `and`
4. Print if can drive legally
5. Test with different combinations

**Hint:** Chain `and` operators.

---

## Exercise 5: Real-World - Login System

Create a program that validates login with username AND password.

**Program interaction (success):**
```
Enter username: alice
Enter password: secret123
Login successful!
```

**Program interaction (wrong username):**
```
Enter username: bob
Enter password: secret123
Login failed
```

**What to do:**
1. Create a file called `login_system.py`
2. Set correct username and password in code
3. Get input from user
4. Check both with `and`
5. Print success or failure

**Hint:** Both must match.

---

## Exercise 6: Grade Calculation with `or`

Create a program that gives an A if score >= 90 OR extra credit completed.

**Program interaction:**
```
Enter score: 85
Extra credit completed? (yes/no): yes
Grade: A
```

**What to do:**
1. Create a file called `grade_or.py`
2. Get score from user
3. Get extra credit status
4. Check if score >= 90 OR extra credit completed
5. Print A or B grade

**Hint:** Use `or` to allow either condition.

---

## Exercise 7: Age and Subscription Check

Create a program that checks age AND subscription status.

**Program interaction:**
```
Enter age: 30
Are you subscribed? (yes/no): yes
Content available? True
```

**What to do:**
1. Create a file called `subscription.py`
2. Get age from user
3. Get subscription status
4. Check if age >= 18 AND subscribed
5. Print if content is available

**Hint:** Both conditions must be true.

---

## Exercise 8: Temperature Comfort with `and` and Range

Create a program that checks if temperature is comfortable (60-80 degrees).

**Program interaction:**
```
Enter temperature: 72
Is comfortable? True
```

**What to do:**
1. Create a file called `temperature_comfort.py`
2. Get temperature from user
3. Check if temperature >= 60 AND temperature <= 80
4. Print if comfortable
5. Test with 50, 72, 90

**Hint:** Use `and` to check both bounds.

---

## Exercise 9: Access Control with `or`

Create a program that allows access if user is admin OR owner OR super_user.

**Program interaction:**
```
Enter role (admin/owner/user/super_user): owner
Access granted
```

**What to do:**
1. Create a file called `access_control.py`
2. Get role from user
3. Check if role is admin OR owner OR super_user
4. Print access granted or denied
5. Test with different roles

**Hint:** Chain `or` operators.

---

## Exercise 10: Combining `and` and `or`

Create a program that checks: (age >= 18 AND license) OR emergency_permit.

**Program interaction:**
```
Age: 16
Has license: no
Has emergency permit: yes
Can drive? True
```

**What to do:**
1. Create a file called `combined_logic.py`
2. Get three inputs
3. Check (age >= 18 and license) or emergency_permit
4. Print result
5. Test with different combinations

**Hint:** Use parentheses for clarity.

---

## Exercise 11: `not` with Conditional

Create a program that uses `not` in an if statement.

**Program interaction:**
```
Is the site under maintenance? (yes/no): no
Site is online
```

**What to do:**
1. Create a file called `not_conditional.py`
2. Get maintenance status from user
3. If NOT under maintenance, print "Site is online"
4. Else, print "Site is down for maintenance"

**Hint:** Use `if not condition:`.

---

## Exercise 12: Real-World - Bank Account Access

Create a program that allows access if account is active AND not locked AND has sufficient balance.

**Program interaction:**
```
Is account active? (yes/no): yes
Is account locked? (yes/no): no
Balance: 500
Access allowed? True
```

**What to do:**
1. Create a file called `bank_access.py`
2. Get three statuses from user
3. Check all with `and` (account active AND NOT locked AND balance > 0)
4. Print if access allowed

**Hint:** Use `not` for locked status.

---

## Exercise 13: Content Filter

Create a program that filters content based on multiple rules.

**Program interaction:**
```
Is content approved? (yes/no): yes
Is author verified? (yes/no): yes
Content can be posted? True
```

**What to do:**
1. Create a file called `content_filter.py`
2. Get approval and verification status
3. Check if both are true with `and`
4. Print if content can be posted

**Hint:** Both conditions required.

---

## Exercise 14: Discount Eligibility

Create a program that checks if customer qualifies for discount (member OR high spender).

**Program interaction:**
```
Is member? (yes/no): no
Total spending: 500
Qualifies for discount? True
```

**What to do:**
1. Create a file called `discount_eligible.py`
2. Get member status and spending amount
3. Check if member OR spending > 300 with `or`
4. Print if qualifies for discount

**Hint:** Either condition is sufficient.

---

## Exercise 15: Complex Real-World - Loan Application

Create a program that approves loan if:
- Age >= 21 AND credit_score >= 600 AND employed

**Program interaction (approved):**
```
Age: 30
Credit score: 750
Employed: yes
Loan approved!
```

**Program interaction (denied):**
```
Age: 30
Credit score: 550
Employed: yes
Loan denied
```

**What to do:**
1. Create a file called `loan_application.py`
2. Get all three inputs
3. Check all three with `and`
4. Print approved or denied
5. Test with different combinations

**Hint:** All three must be true.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Does it return correct True/False?
- ✓ Did I use the right operator (and/or/not)?
- ✓ Do I understand when each is used?

---

## Important Observations

**About Logical Operators:**
- `and`: both must be true
- `or`: at least one must be true
- `not`: reverses true/false
- Order: `not`, `and`, `or`
- Use parentheses for clarity
- They work great in if statements

---

## Next Steps

Once you've completed these exercises:

1. You can combine multiple conditions
2. You understand `and`, `or`, `not`
3. You can write complex if statements
4. You can validate multiple requirements

You're ready for Topic 10: **While Loops**

While loops let you repeat code over and over, which is the foundation for real programs.

Next lesson: repeating actions!
