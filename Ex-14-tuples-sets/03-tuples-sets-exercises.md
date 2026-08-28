# Tuples & Sets: Exercises & Practice

## Exercise 1: Create and Access Tuples

Create a program that creates a tuple and accesses items.

**Expected output:**
```
Tuple: (10, 20, 30)
First item: 10
Last item: 30
Length: 3
```

**What to do:**
1. Create a file called `simple_tuple.py`
2. Create tuple with 3 numbers
3. Print tuple
4. Print first item using index 0
5. Print last item using index -1
6. Print length
7. Run it

**Hint:** Use tuple[0] and tuple[-1].

---

## Exercise 2: Tuple Unpacking

Create a program that unpacks tuple into variables.

**Expected output:**
```
X: 10
Y: 20
```

**What to do:**
1. Create a file called `tuple_unpack.py`
2. Create tuple with 2 numbers: (10, 20)
3. Unpack: `x, y = tuple`
4. Print x and y separately
5. Run it

**Hint:** `a, b = (1, 2)` unpacks automatically.

---

## Exercise 3: Tuples Are Immutable

Create a program that tries to modify a tuple (and fails).

**Expected output:**
```
Error: 'tuple' object does not support item assignment
```

**What to do:**
1. Create a file called `tuple_immutable.py`
2. Create tuple
3. Try to change first item
4. Catch TypeError
5. Print error message
6. Run it

**Hint:** Use try/except to catch error.

---

## Exercise 4: Create Sets

Create a program that creates sets and shows them.

**Expected output:**
```
Set: {'red', 'green', 'blue'}
Length: 3
Type: <class 'set'>
```

**What to do:**
1. Create a file called `simple_set.py`
2. Create set with 3 colors
3. Print set
4. Print length
5. Print type
6. Run it

**Hint:** Use {item1, item2, item3} syntax.

---

## Exercise 5: Remove Duplicates

Create a program that removes duplicates from list using set.

**Expected output:**
```
Original: [1, 2, 2, 3, 3, 3]
Unique: {1, 2, 3}
Removed: 3 duplicates
```

**What to do:**
1. Create a file called `remove_duplicates.py`
2. Create list with duplicates
3. Convert to set
4. Print original and unique
5. Calculate duplicates removed
6. Run it

**Hint:** `len(list) - len(set(list))`.

---

## Exercise 6: Add to Set

Create a program that adds items to a set.

**Expected output:**
```
Before: {'red', 'green'}
After: {'red', 'green', 'blue'}
```

**What to do:**
1. Create a file called `add_to_set.py`
2. Create set with 2 colors
3. Print before
4. Add new color
5. Print after
6. Run it

**Hint:** Use `set.add(item)`.

---

## Exercise 7: Remove from Set

Create a program that removes items from a set.

**Expected output:**
```
Before: {'red', 'green', 'blue'}
After: {'red', 'blue'}
```

**What to do:**
1. Create a file called `remove_from_set.py`
2. Create set with 3 items
3. Print before
4. Remove one item
5. Print after
6. Run it

**Hint:** Use `set.remove(item)`.

---

## Exercise 8: Set Union

Create a program that combines two sets.

**Expected output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Union: {1, 2, 3, 4}
```

**What to do:**
1. Create a file called `set_union.py`
2. Create two sets
3. Print each set
4. Calculate union using |
5. Print union
6. Run it

**Hint:** `union = a | b`.

---

## Exercise 9: Set Intersection

Create a program that finds common items.

**Expected output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Common: {2, 3}
```

**What to do:**
1. Create a file called `set_intersection.py`
2. Create two sets
3. Print each set
4. Calculate intersection using &
5. Print common items
6. Run it

**Hint:** `common = a & b`.

---

## Exercise 10: Set Difference

Create a program that finds unique items.

**Expected output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Only in a: {1}
```

**What to do:**
1. Create a file called `set_difference.py`
2. Create two sets
3. Print each set
4. Calculate difference using -
5. Print items only in first set
6. Run it

**Hint:** `diff = a - b`.

---

## Exercise 11: Membership Testing

Create a program that checks if item exists in set.

**Program interaction:**
```
Is 'apple' in fruits? True
Is 'grape' in fruits? False
```

**What to do:**
1. Create a file called `set_membership.py`
2. Create set of fruits
3. Check if "apple" in set
4. Check if "grape" in set
5. Print results
6. Run it

**Hint:** Use `if item in set:`.

---

## Exercise 12: Tuple as Dictionary Key

Create a program that uses tuples as dict keys.

**Expected output:**
```
Location at (0, 0): Origin
Location at (1, 1): Northeast
```

**What to do:**
1. Create a file called `tuple_dict_keys.py`
2. Create dict with tuple keys
3. Add 3-4 coordinate entries
4. Print 2 entries
5. Run it

**Hint:** `dict[(0, 0)] = "Origin"`.

---

## Exercise 13: Real-World - Unique Emails

Create a program that deduplicates email list.

**Expected output:**
```
Total emails: 7
Unique emails: 5
Duplicates: 2
Unique list: {'alice@example.com', 'bob@example.com', ...}
```

**What to do:**
1. Create a file called `unique_emails.py`
2. Create list of emails (with duplicates)
3. Convert to set
4. Show original count, unique count, duplicates
5. Run it

**Hint:** `duplicates = len(list) - len(set(list))`.

---

## Exercise 14: Real-World - Common Skills

Create a program that finds common skills between people.

**Program interaction:**
```
Person A skills: {'Python', 'JavaScript', 'SQL'}
Person B skills: {'Python', 'Java', 'SQL'}
Common skills: {'Python', 'SQL'}
```

**What to do:**
1. Create a file called `common_skills.py`
2. Create 2 sets of skills
3. Print each person's skills
4. Find intersection (common)
5. Print common skills
6. Run it

**Hint:** Use & operator or `.intersection()`.

---

## Exercise 15: Real-World - Permission System

Create a program that checks user permissions.

**Expected output:**
```
User permissions: {'read', 'write'}
Allowed: {'read', 'write', 'delete'}
User can: {'read', 'write'}
User cannot: {'delete'}
```

**What to do:**
1. Create a file called `permissions.py`
2. Create set of user permissions
3. Create set of allowed permissions
4. Find what user has (intersection)
5. Find what user lacks (difference)
6. Print results
7. Run it

**Hint:** Use & and - operators.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Can I create tuples and sets?
- ✓ Do I understand immutability?
- ✓ Can I use sets to remove duplicates?
- ✓ Can I perform set operations?
- ✓ Do I know when to use each?

---

## Important Observations

**About Tuples:**
- Immutable (can't change)
- Can be dict keys
- Unpack into variables
- Slightly faster than lists
- Use when data shouldn't change

**About Sets:**
- Unordered
- Only unique items
- Fast membership testing
- Set operations (union, intersection, difference)
- Great for deduplication

**When to Use:**
- Tuple: fixed data, dict keys, multiple returns
- Set: unique items, membership testing, operations
- List: data might change, need indexing

---

## Next Steps

Once you've mastered tuples and sets:

1. You understand Python's data structure options
2. You can choose the right structure for each problem
3. You're ready for functions (reusable code)

You're making excellent progress! 🎉

**13 core topics complete → 2 more advanced topics to go!**

Next topic: **Topic 15: Functions** (reusable code blocks)
