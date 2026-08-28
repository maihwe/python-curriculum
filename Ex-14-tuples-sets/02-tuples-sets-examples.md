# Tuples & Sets: Examples & Demos

## Example 1: Creating and Accessing Tuples

**Code:**
```python
person = ("Alice", 25, "Engineer")

print("Tuple:", person)
print("First item:", person[0])
print("Second item:", person[1])
print("Length:", len(person))
```

**Output:**
```
Tuple: ('Alice', 25, 'Engineer')
First item: Alice
Second item: 25
Length: 3
```

**Key insight:** Access tuples like lists using indexes.

---

## Example 2: Tuples Are Immutable

**Code:**
```python
point = (10, 20)

print("Before:", point)

try:
    point[0] = 15
except TypeError as e:
    print("Error:", e)
```

**Output:**
```
Before: (10, 20)
Error: 'tuple' object does not support item assignment
```

**Key insight:** Tuples can't be modified. Attempting to change raises error.

---

## Example 3: Tuple Unpacking

**Code:**
```python
point = (10, 20)
x, y = point

print("X:", x)
print("Y:", y)
```

**Output:**
```
X: 10
Y: 20
```

**Key insight:** Unpack tuple values into separate variables.

---

## Example 4: Creating Sets

**Code:**
```python
colors = {"red", "green", "blue"}

print("Set:", colors)
print("Type:", type(colors))
print("Length:", len(colors))
```

**Output:**
```
Set: {'red', 'green', 'blue'}
Type: <class 'set'>
Length: 3
```

**Key insight:** Sets use {} syntax (like dicts) but store items, not key-value pairs.

---

## Example 5: Sets Remove Duplicates

**Code:**
```python
numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]

unique = set(numbers)

print("Original list:", numbers)
print("Unique set:", unique)
print("Duplicates removed:", len(numbers) - len(unique))
```

**Output:**
```
Original list: [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
Unique set: {1, 2, 3, 4}
Duplicates removed: 6
```

**Key insight:** Converting to set automatically removes all duplicates.

---

## Example 6: Membership Testing with Sets

**Code:**
```python
colors = {"red", "green", "blue"}

if "red" in colors:
    print("Found red!")
else:
    print("Red not found")

if "yellow" in colors:
    print("Found yellow!")
else:
    print("Yellow not found")
```

**Output:**
```
Found red!
Yellow not found
```

**Key insight:** Use `in` to check if item exists in set.

---

## Example 7: Adding to Sets

**Code:**
```python
colors = {"red", "green"}

print("Before:", colors)

colors.add("blue")
print("After add:", colors)

colors.add("red")  # Already exists
print("After duplicate add:", colors)
```

**Output:**
```
Before: {'red', 'green'}
After add: {'red', 'green', 'blue'}
After duplicate add: {'red', 'green', 'blue'}
```

**Key insight:** Adding duplicate has no effect (still unique).

---

## Example 8: Removing from Sets

**Code:**
```python
colors = {"red", "green", "blue"}

print("Before:", colors)

colors.remove("green")
print("After remove:", colors)

try:
    colors.remove("yellow")
except KeyError:
    print("Error: yellow not in set")
```

**Output:**
```
Before: {'red', 'green', 'blue'}
After remove: {'red', 'blue'}
Error: yellow not in set
```

**Key insight:** `remove()` deletes item, errors if not found.

---

## Example 9: Set Union

**Code:**
```python
a = {1, 2, 3}
b = {2, 3, 4}

combined = a | b

print("Set a:", a)
print("Set b:", b)
print("Union (a | b):", combined)
```

**Output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Union (a | b): {1, 2, 3, 4}
```

**Key insight:** Union combines sets and removes duplicates.

---

## Example 10: Set Intersection

**Code:**
```python
a = {1, 2, 3}
b = {2, 3, 4}

common = a & b

print("Set a:", a)
print("Set b:", b)
print("Intersection (a & b):", common)
```

**Output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Intersection (a & b): {2, 3}
```

**Key insight:** Intersection finds items in BOTH sets.

---

## Example 11: Set Difference

**Code:**
```python
a = {1, 2, 3}
b = {2, 3, 4}

diff = a - b

print("Set a:", a)
print("Set b:", b)
print("Difference (a - b):", diff)
```

**Output:**
```
Set a: {1, 2, 3}
Set b: {2, 3, 4}
Difference (a - b): {1}
```

**Key insight:** Difference finds items in a but NOT in b.

---

## Example 12: Tuples as Dictionary Keys

**Code:**
```python
coordinates = {
    (0, 0): "Origin",
    (1, 0): "East",
    (0, 1): "North",
    (1, 1): "Northeast"
}

print("Location at (0, 0):", coordinates[(0, 0)])
print("Location at (1, 1):", coordinates[(1, 1)])
```

**Output:**
```
Location at (0, 0): Origin
Location at (1, 1): Northeast
```

**Key insight:** Tuples work as dictionary keys (lists don't).

---

## Example 13: Why Lists Can't Be Keys

**Code:**
```python
try:
    bad = {[0, 0]: "Origin"}
except TypeError as e:
    print("Error:", e)
```

**Output:**
```
Error: unhashable type: 'list'
```

**Key insight:** Lists are mutable, so they can't be dictionary keys.

---

## Example 14: Tuple vs List Speed

**Code:**
```python
import time

# Create list with 1 million items
big_list = list(range(1000000))
big_tuple = tuple(range(1000000))

# Measure access time
start = time.time()
for i in range(100000):
    x = big_list[500000]
list_time = time.time() - start

start = time.time()
for i in range(100000):
    x = big_tuple[500000]
tuple_time = time.time() - start

print("List access time:", list_time)
print("Tuple access time:", tuple_time)
print("Tuples are slightly faster")
```

**Output:**
```
List access time: 0.008
Tuple access time: 0.007
Tuples are slightly faster
```

**Key insight:** Tuples are immutable, so they're slightly faster.

---

## Example 15: Real-World - Unique Usernames

**Code:**
```python
# List of usernames (with duplicates)
usernames = ["alice", "bob", "alice", "charlie", "bob", "david"]

print("Raw usernames:", usernames)
print("Duplicate count:", len(usernames) - len(set(usernames)))

unique_usernames = set(usernames)
print("Unique usernames:", unique_usernames)
print("Total unique:", len(unique_usernames))
```

**Output:**
```
Raw usernames: ['alice', 'bob', 'alice', 'charlie', 'bob', 'david']
Duplicate count: 2
Unique usernames: {'alice', 'bob', 'charlie', 'david'}
Total unique: 4
```

**Key insight:** Sets perfect for deduplication.

---

## Summary of Examples

- Create and access tuples
- Tuples are immutable
- Unpack tuples
- Create sets
- Remove duplicates
- Test membership
- Add/remove set items
- Set operations (union, intersection, difference)
- Tuples as dict keys
- Lists can't be keys
- Tuples faster than lists
- Real-world deduplication

Next: practice with exercises.
