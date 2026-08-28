# Lists: Collections of Data - Lecture

## Why This Matters

So far, you can store one piece of data at a time:

```python
name1 = "Alice"
name2 = "Bob"
name3 = "Charlie"
```

But what if you have 100 names? Or 1,000?

You'd write 1,000 variable names. That's terrible.

A **list** is a container that holds multiple items in order. This lets you store, access, and process collections of data.

Lists are fundamental. Every real program uses them.

---

## The Mental Model: What Is a List?

A list is like a **filing cabinet with numbered drawers**.

```
┌─────────┐
│ 0:"Alice"│
├─────────┤
│ 1:"Bob"  │
├─────────┤
│ 2:"Charlie"│
├─────────┤
│ 3:"David"│
└─────────┘
```

Each drawer holds one item. Each has a number (called an **index**).

You access items by number:

```python
names = ["Alice", "Bob", "Charlie", "David"]
print(names[0])   # "Alice"  (index 0)
print(names[1])   # "Bob"    (index 1)
print(names[2])   # "Charlie" (index 2)
```

---

## The Mental Model: Creating Lists

Three ways to create a list:

**Empty list:**
```python
empty = []
```

**List with items:**
```python
fruits = ["apple", "banana", "cherry"]
```

**List from input:**
```python
numbers = [1, 2, 3, 4, 5]
```

Lists can hold any data type:
- Strings: `["Alice", "Bob"]`
- Numbers: `[1, 2, 3]`
- Mixed: `["Alice", 25, 3.14]`
- Even lists: `[[1, 2], [3, 4]]`

---

## The Mental Model: Indexing (Accessing Items)

Lists are **zero-indexed**. The first item is at index 0.

```python
fruits = ["apple", "banana", "cherry"]
```

```
Index:  0         1          2
Item:   "apple"   "banana"   "cherry"
```

Access by index:

```python
print(fruits[0])   # "apple"
print(fruits[1])   # "banana"
print(fruits[2])   # "cherry"
```

**Important:** `fruits[3]` causes an error (index out of range).

---

## The Mental Model: Negative Indexing

You can count from the end using negative numbers:

```python
fruits = ["apple", "banana", "cherry"]
```

```
Index:  0         1          2      -3  -2  -1
Item:   "apple"   "banana"   "cherry"
```

```python
print(fruits[-1])   # "cherry"  (last item)
print(fruits[-2])   # "banana"  (second to last)
print(fruits[-3])   # "apple"   (third to last)
```

---

## The Mental Model: List Length

The `len()` function tells you how many items in a list:

```python
fruits = ["apple", "banana", "cherry"]
print(len(fruits))   # 3

numbers = [10, 20, 30, 40, 50]
print(len(numbers))  # 5
```

The last valid index is always `len(list) - 1`.

---

## The Mental Model: Adding Items

**`append()`** adds item to the end:

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)  # ["apple", "banana", "cherry"]
```

**`insert()`** adds item at specific position:

```python
fruits = ["apple", "banana", "cherry"]
fruits.insert(1, "grape")
print(fruits)  # ["apple", "grape", "banana", "cherry"]
```

---

## The Mental Model: Removing Items

**`remove()`** removes by value:

```python
fruits = ["apple", "banana", "cherry"]
fruits.remove("banana")
print(fruits)  # ["apple", "cherry"]
```

**`pop()`** removes by index (and returns the item):

```python
fruits = ["apple", "banana", "cherry"]
removed = fruits.pop(1)
print(removed)  # "banana"
print(fruits)   # ["apple", "cherry"]
```

---

## The Mental Model: Looping Over Lists

You rarely access items by index. Instead, you **loop**:

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

**Output:**
```
apple
banana
cherry
```

The loop variable (`fruit`) automatically takes each item.

---

## The Mental Model: Slicing

**Slicing** extracts a portion of a list:

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(numbers[2:5])    # [2, 3, 4]  (index 2 to 4, not including 5)
print(numbers[:3])     # [0, 1, 2]  (start to index 2)
print(numbers[7:])     # [7, 8, 9]  (index 7 to end)
print(numbers[::2])    # [0, 2, 4, 6, 8]  (every 2nd item)
```

Slicing creates a **new list**. It doesn't modify the original.

---

## The Mental Model: Checking Membership

The **`in`** operator checks if item exists:

```python
fruits = ["apple", "banana", "cherry"]

if "apple" in fruits:
    print("Found it!")
else:
    print("Not found")
```

---

## Key Concepts to Remember

1. **List is a container** holding multiple items
2. **Zero-indexed** — first item is at index 0
3. **Access by index** — `list[0]`, `list[1]`, etc.
4. **Negative indexing** — count from end with -1, -2, etc.
5. **`len()`** returns number of items
6. **`append()`** adds to end
7. **`insert()`** adds at position
8. **`remove()`** removes by value
9. **`pop()`** removes by index
10. **Loop with `for`** to process each item
11. **Slicing** extracts portions
12. **`in`** checks membership

---

## Common Misconceptions

**"Lists are like variables"**

No. A variable holds ONE item. A list holds MANY items.

**"I can access any index"**

No. Only 0 to len(list)-1. Out of range causes error.

**"Indexing starts at 1"**

No. Python uses zero-indexing. First item is at index 0.

**"Looping requires indexes"**

No. `for item in list:` is better than accessing by index.

**"I have to know list size when creating it"**

No. Lists grow dynamically with `append()`.

---

## Real-World Uses

- **Store user names** in game
- **Keep shopping list** of items
- **Track test scores** for a student
- **Store coordinates** for a path
- **Process file lines** one by one
- **Build a queue** for processing

---

## Summary

Lists let you store and work with collections of data. This is essential for any real program.

Instead of:
```python
name1 = "Alice"
name2 = "Bob"
```

You write:
```python
names = ["Alice", "Bob"]
```

Much cleaner. Much more powerful.

Next: see lists in action.
