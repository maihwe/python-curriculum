# Logical Operators: Examples & Demos

## Example 1: `and` Operator - Both True

**Code:**
```python
age = 25
has_license = True

can_drive = age >= 18 and has_license

print("Age:", age)
print("Has license:", has_license)
print("Can drive:", can_drive)
```

**Output:**
```
Age: 25
Has license: True
Can drive: True
```

**Explanation:**

`age >= 18` → True

`has_license` → True

`True and True` → True

**Key insight:** Both conditions true = result is true.

---

## Example 2: `and` Operator - One False

**Code:**
```python
age = 25
has_license = False

can_drive = age >= 18 and has_license

print("Can drive:", can_drive)
```

**Output:**
```
Can drive: False
```

**Explanation:**

`age >= 18` → True

`has_license` → False

`True and False` → False

**Key insight:** If any condition is false, `and` is false.

---

## Example 3: `or` Operator - Both True

**Code:**
```python
score = 95
completed_extra_credit = True

gets_a = score >= 90 or completed_extra_credit

print("Score:", score)
print("Extra credit:", completed_extra_credit)
print("Gets A:", gets_a)
```

**Output:**
```
Score: 95
Extra credit: True
Gets A: True
```

**Explanation:**

`score >= 90` → True

`completed_extra_credit` → True

`True or True` → True

**Key insight:** If any condition is true, `or` is true.

---

## Example 4: `or` Operator - One False

**Code:**
```python
score = 85
completed_extra_credit = True

gets_a = score >= 90 or completed_extra_credit

print("Score:", score)
print("Extra credit:", completed_extra_credit)
print("Gets A:", gets_a)
```

**Output:**
```
Score: 85
Extra credit: True
Gets A: True
```

**Explanation:**

`score >= 90` → False

`completed_extra_credit` → True

`False or True` → True

**Key insight:** `or` only requires one to be true.

---

## Example 5: `or` Operator - Both False

**Code:**
```python
score = 70
completed_extra_credit = False

gets_a = score >= 90 or completed_extra_credit

print("Gets A:", gets_a)
```

**Output:**
```
Gets A: False
```

**Key insight:** `or` is false only if both are false.

---

## Example 6: `not` Operator

**Code:**
```python
is_banned = False

can_access = not is_banned

print("Is banned:", is_banned)
print("Can access:", can_access)
```

**Output:**
```
Is banned: False
Can access: True
```

**Explanation:**

`is_banned` → False

`not False` → True

**Key insight:** `not` reverses the boolean.

---

## Example 7: `not` Operator - Opposite Case

**Code:**
```python
is_banned = True

can_access = not is_banned

print("Is banned:", is_banned)
print("Can access:", can_access)
```

**Output:**
```
Is banned: True
Can access: False
```

**Key insight:** `not True` is False.

---

## Example 8: Chaining Multiple `and` Operators

**Code:**
```python
age = 25
has_license = True
has_insurance = True

can_drive = age >= 18 and has_license and has_insurance

print("Can drive legally:", can_drive)
```

**Output:**
```
Can drive legally: True
```

**Explanation:**

All three conditions must be true. If any is false, the result is false.

**Key insight:** You can chain `and` operators.

---

## Example 9: Using in If Statement

**Code:**
```python
username = "alice"
password = "secret"

entered_username = input("Username: ")
entered_password = input("Password: ")

if entered_username == username and entered_password == password:
    print("Login successful!")
else:
    print("Login failed")
```

**Program interaction (correct):**
```
Username: alice
Password: secret
Login successful!
```

**Program interaction (wrong):**
```
Username: alice
Password: wrong
Login failed
```

**Key insight:** `and` in if statement requires both conditions.

---

## Example 10: Using `or` in If Statement

**Code:**
```python
user_role = input("Your role (admin/owner/user): ")

if user_role == "admin" or user_role == "owner":
    print("Access granted")
else:
    print("Access denied")
```

**Program interaction:**
```
Your role (admin/owner/user): admin
Access granted
```

**Program interaction (user):**
```
Your role (admin/owner/user): user
Access denied
```

**Key insight:** `or` in if statement requires at least one.

---

## Example 11: Using `not` in If Statement

**Code:**
```python
is_banned = False

if not is_banned:
    print("You can post")
else:
    print("You are banned")
```

**Output:**
```
You can post
```

**Key insight:** `not` reverses the condition.

---

## Example 12: Complex Condition with Parentheses

**Code:**
```python
age = 20
has_license = True
has_emergency_permit = False

can_drive = (age >= 18 and has_license) or has_emergency_permit

print("Can drive:", can_drive)
```

**Output:**
```
Can drive: True
```

**Explanation:**

`(age >= 18 and has_license)` → `(True and True)` → True

`has_emergency_permit` → False

`True or False` → True

**Key insight:** Parentheses clarify complex conditions.

---

## Example 13: Range Check with `and`

**Code:**
```python
temperature = 72

if temperature >= 60 and temperature <= 85:
    print("Comfortable temperature")
else:
    print("Too hot or too cold")
```

**Output:**
```
Comfortable temperature
```

**Key insight:** Check if value is in range using `and`.

---

## Example 14: Real-World - E-Commerce Validation

**Code:**
```python
age = 25
has_payment = True
account_active = True

can_purchase = age >= 18 and has_payment and account_active

if can_purchase:
    print("Purchase approved")
else:
    print("Purchase denied")
```

**Output:**
```
Purchase approved
```

**Key insight:** Multiple conditions for real-world scenarios.

---

## Example 15: Short-Circuit Evaluation

**Code:**
```python
def check_first():
    print("Checking first condition...")
    return False

def check_second():
    print("Checking second condition...")
    return True

# With 'and'
result = check_first() and check_second()
print("Result:", result)
```

**Output:**
```
Checking first condition...
Result: False
```

**Notice:** "Checking second condition..." is NOT printed.

**Key insight:** Python stops evaluating once it knows the answer (short-circuit).

---

## Summary of Examples

- `and` requires both conditions true
- `or` requires at least one true
- `not` reverses true/false
- Use parentheses for clarity
- Logical operators work in if statements
- Short-circuit evaluation is efficient

Next: practice with exercises.
