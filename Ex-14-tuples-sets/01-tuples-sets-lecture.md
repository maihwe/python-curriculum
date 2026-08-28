# Tuples & Sets: Immutable Collections and Unique Data - Lecture

## Why This Matters

So far, you know lists:

```python
colors = ["red", "green", "blue"]
colors[0] = "yellow"  # You can change it
colors.append("purple")  # You can add to it
```

Lists are flexible. But sometimes you DON'T want flexibility. You want data that:
- Can't be accidentally changed
- Contains only unique items
- Works as dictionary keys

**Tuples** and **Sets** solve these problems.

---

## The Mental Model: What Is a Tuple?

A **tuple** is like a list, but frozen.

```
List:  ["apple", "banana", "cherry"]  ← Can modify
Tuple: ("apple", "banana", "cherry")  ← Cannot modify
```

Once created, a tuple never changes. You can't add, remove, or modify items.

**Why?**
- Guarantees data integrity (immutable)
- Faster than lists (optimization)
- Can be used as dictionary keys
- Signals "this data shouldn't change"

---

## The Mental Model: What Is a Set?

A **set** is like a list, but:
- Unordered (no indexes)
- Contains only unique items (no duplicates)
- Great for membership testing

```python
numbers = [1, 2, 2, 3, 3, 3, 4]
unique = set(numbers)
print(unique)  # {1, 2, 3, 4}  ← Duplicates removed!
```

Sets automatically eliminate duplicates.

---

## The Mental Model: Creating Tuples

**Tuple with parentheses:**
```python
point = (10, 20)
person = ("Alice", 25, "Engineer")
```

**Tuple without parentheses (Python allows it):**
```python
point = 10, 20
name = "Alice", 25
```

**Empty tuple:**
```python
empty = ()
```

**Single-item tuple (needs comma!):**
```python
single = (42,)  # Note the comma!
wrong = (42)    # This is just a number, not a tuple
```

---

## The Mental Model: Accessing Tuples

Access tuples like lists (using indexes):

```python
person = ("Alice", 25, "Engineer")
print(person[0])   # "Alice"
print(person[1])   # 25
print(person[-1])  # "Engineer"
```

But you can't modify:

```python
person[0] = "Bob"  # ERROR! Tuples are immutable
```

---

## The Mental Model: Creating Sets

**Set with braces:**
```python
colors = {"red", "green", "blue"}
```

**Set from list:**
```python
numbers = [1, 2, 2, 3, 3]
unique = set(numbers)
print(unique)  # {1, 2, 3}
```

**Empty set (tricky!):**
```python
empty = set()  # NOT {} (that's an empty dict)
```

---

## The Mental Model: Set Operations

Sets have unique operations:

**Union (combine, remove duplicates):**
```python
a = {1, 2, 3}
b = {2, 3, 4}
combined = a | b  # {1, 2, 3, 4}
```

**Intersection (common items):**
```python
common = a & b  # {2, 3}
```

**Difference (items in a but not b):**
```python
diff = a - b  # {1}
```

---

## The Mental Model: Membership Testing

Sets are FAST for checking membership:

```python
colors = {"red", "green", "blue"}

if "red" in colors:
    print("Found it!")
```

This is much faster with sets than lists (for large collections).

---

## The Mental Model: Tuples as Dictionary Keys

You can use tuples as dictionary keys (but not lists):

```python
coordinates = {
    (0, 0): "Origin",
    (1, 0): "East",
    (0, 1): "North",
    (1, 1): "Northeast"
}

print(coordinates[(0, 0)])  # "Origin"
```

Lists can't be keys (they're mutable):

```python
bad = {[0, 0]: "Origin"}  # ERROR! Lists can't be keys
```

---

## Key Concepts to Remember

1. **Tuple** = immutable (frozen) sequence
2. **Set** = unordered, unique items only
3. **Tuples use ()**, sets use {}
4. **Can't modify tuples** (immutable)
5. **Can't access sets by index** (unordered)
6. **Tuples can be dict keys**, sets can't
7. **Sets remove duplicates** automatically
8. **Membership testing** is fast with sets
9. **Set operations**: union |, intersection &, difference -
10. **Tuple unpacking**: `a, b = (1, 2)` → a=1, b=2

---

## Common Misconceptions

**"Tuples are just read-only lists"**

Not quite. They're immutable (can't change), but they also signal intent: "this data shouldn't change."

**"Sets are like lists but unordered"**

Partially true, but sets ONLY contain unique items and have different operations (union, intersection).

**"I should use tuples instead of lists"**

No. Use lists when data changes. Use tuples when data shouldn't change.

**"Empty set is {}"**

No! {} is an empty dict. Use set() for empty set.

---

## When to Use Each

**Use Tuples when:**
- Data shouldn't change
- You need dict keys
- Returning multiple values
- Protecting data integrity

**Use Sets when:**
- You need unique items only
- You need set operations (union, intersection)
- Testing membership (fast lookup)
- Removing duplicates

**Use Lists when:**
- Data might change
- Order matters
- You access by index
- You need flexibility

---

## Real-World Uses

**Tuples:**
- Coordinates: (latitude, longitude)
- RGB colors: (255, 128, 0)
- Returning multiple values from function
- Immutable configuration

**Sets:**
- Storing unique usernames
- Finding common tags between posts
- Removing duplicate data
- Permission checking

---

## Summary

**Tuples** are frozen lists—immutable, hashable, perfect for keys and protecting data.

**Sets** are unique collections—great for eliminating duplicates and set operations.

Both solve problems that lists can't.

Next: see them in action.
