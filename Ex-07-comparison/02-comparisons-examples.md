# Comparisons: Examples & Demos

## Example 1: Equality Comparison

**Code:**
```python
a = 5
b = 5
c = 3

print(a == b)   # 5 equals 5?
print(a == c)   # 5 equals 3?
```

**Output:**
```
True
False
```

**Execution flow:**

Line 3: `a == b` compares 5 and 5 → they're equal → True

Line 4: `a == c` compares 5 and 3 → they're not equal → False

**Key insight:** `==` tests if two values are the same.

---

## Example 2: Inequality Comparison

**Code:**
```python
a = 5
b = 3

print(a != b)   # 5 not equal to 3?
print(a != 5)   # 5 not equal to 5?
```

**Output:**
```
True
False
```

**Explanation:**

Line 3: `a != b` → `5 != 3` → True (they are different)

Line 4: `a != 5` → `5 != 5` → False (they are equal, so not-equal is false)

**Key insight:** `!=` is the opposite of `==`.

---

## Example 3: Greater Than

**Code:**
```python
a = 10
b = 5

print(a > b)    # 10 greater than 5?
print(b > a)    # 5 greater than 10?
print(a > a)    # 10 greater than 10?
```

**Output:**
```
True
False
False
```

**Explanation:**

Line 3: `10 > 5` → True (10 is greater)

Line 4: `5 > 10` → False (5 is not greater)

Line 5: `10 > 10` → False (equal, not greater)

**Key insight:** `>` tests strictly greater than (not equal).

---

## Example 4: Less Than

**Code:**
```python
a = 5
b = 10

print(a < b)    # 5 less than 10?
print(b < a)    # 10 less than 5?
print(a < a)    # 5 less than 5?
```

**Output:**
```
True
False
False
```

**Key insight:** `<` is the opposite of `>`.

---

## Example 5: Greater Than or Equal

**Code:**
```python
a = 5

print(a >= 3)   # 5 >= 3?
print(a >= 5)   # 5 >= 5?
print(a >= 7)   # 5 >= 7?
```

**Output:**
```
True
True
False
```

**Explanation:**

Line 2: `5 >= 3` → True (5 is greater than 3)

Line 3: `5 >= 5` → True (5 equals 5, so >= is true)

Line 4: `5 >= 7` → False (5 is less than 7)

**Key insight:** `>=` includes both "greater than" and "equal to".

---

## Example 6: Less Than or Equal

**Code:**
```python
a = 5

print(a <= 7)   # 5 <= 7?
print(a <= 5)   # 5 <= 5?
print(a <= 3)   # 5 <= 3?
```

**Output:**
```
True
True
False
```

**Key insight:** `<=` is the opposite of `>=`.

---

## Example 7: Storing Comparison Results

**Code:**
```python
age = 25

is_adult = age >= 18
is_senior = age >= 65

print("Is adult?", is_adult)
print("Is senior?", is_senior)
```

**Output:**
```
Is adult? True
Is senior? False
```

**Explanation:**

Line 3: `age >= 18` → `25 >= 18` → True, store in `is_adult`

Line 4: `age >= 65` → `25 >= 65` → False, store in `is_senior`

**Key insight:** You can store comparison results in variables.

---

## Example 8: String Comparison

**Code:**
```python
name1 = "Alice"
name2 = "Alice"
name3 = "Bob"

print(name1 == name2)   # Alice equals Alice?
print(name1 == name3)   # Alice equals Bob?
print(name1 != name3)   # Alice not equal Bob?
```

**Output:**
```
True
False
True
```

**Key insight:** You can compare strings for equality.

---

## Example 9: String Comparison is Case-Sensitive

**Code:**
```python
password = "Secret123"
guess1 = "Secret123"
guess2 = "secret123"

print(password == guess1)   # Correct password?
print(password == guess2)   # Wrong case?
```

**Output:**
```
True
False
```

**Explanation:**

Line 3: "Secret123" equals "Secret123" → True (exact match)

Line 4: "Secret123" equals "secret123" → False (different cases)

**Key insight:** Comparisons are case-sensitive.

---

## Example 10: Alphabetical Comparison

**Code:**
```python
print("apple" < "banana")   # a comes before b?
print("zebra" > "apple")    # z comes after a?
print("cat" < "dog")        # c comes before d?
```

**Output:**
```
True
True
True
```

**Explanation:**

Strings are compared alphabetically (like a dictionary).

**Key insight:** `<` and `>` with strings use alphabetical order.

---

## Example 11: Comparing Different Types

**Code:**
```python
print(5 == 5)       # Number equals number?
print("5" == "5")   # String equals string?
print(5 == "5")     # Number equals string?
```

**Output:**
```
True
True
False
```

**Explanation:**

Line 1: `5 == 5` → True (both numbers)

Line 2: `"5" == "5"` → True (both text)

Line 3: `5 == "5"` → False (number ≠ string, even though they look similar)

**Key insight:** Type matters. `5` and `"5"` are different.

---

## Example 12: Real-World - Age Check

**Code:**
```python
age = int(input("Enter your age: "))

can_vote = age >= 18
can_drive = age >= 16
is_child = age < 13

print("Can vote:", can_vote)
print("Can drive:", can_drive)
print("Is child:", is_child)
```

**Program interaction:**
```
Enter your age: 20
Can vote: True
Can drive: True
Is child: False
```

**Key insight:** Comparisons with user input let you check conditions.

---

## Example 13: Score Grading

**Code:**
```python
score = int(input("Enter score: "))

is_passing = score >= 60
is_good = score >= 80
is_excellent = score >= 90

print("Score:", score)
print("Passing?", is_passing)
print("Good?", is_good)
print("Excellent?", is_excellent)
```

**Program interaction:**
```
Enter score: 85
Score: 85
Passing? True
Good? True
Excellent? False
```

**Key insight:** Multiple comparisons on the same value.

---

## Example 14: Range Checking

**Code:**
```python
num = 15

in_range = num >= 10 and num <= 20

print("Is", num, "between 10 and 20?", in_range)
```

**Output:**
```
Is 15 between 10 and 20? True
```

**Note:** This uses `and` which we'll learn next. For now, notice you can combine comparisons.

**Key insight:** You can check if something is in a range.

---

## Example 15: Boolean Value is a Type

**Code:**
```python
result = 5 > 3

print(result)
print(type(result))
```

**Output:**
```
True
<class 'bool'>
```

**Explanation:**

Line 1: `5 > 3` returns `True` (a boolean value)

Line 2: `type(True)` returns the type

**Key insight:** Boolean is a data type, just like int, float, and str.

---

## Summary of Examples

- `==` tests equality
- `!=` tests inequality
- `>` and `<` test greater/less
- `>=` and `<=` test with equality
- Comparisons return True or False
- You can store results in variables
- Different types don't usually equal (5 ≠ "5")
- Strings compare alphabetically
- Comparisons are case-sensitive

Next: use comparisons to control program flow.
