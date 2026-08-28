# Dictionaries: Storing Data by Name - Lecture

## Why This Matters

Lists work great when you access items by number (index):

```python
person = ["Alice", 25, "Engineer"]
print(person[0])   # Alice (what is 0?)
print(person[1])   # 25 (what is 1?)
print(person[2])   # Engineer (what is 2?)
```

But this is confusing. You have to remember: "index 0 is name, 1 is age, 2 is job."

What if you could access by name instead?

```python
person = {"name": "Alice", "age": 25, "job": "Engineer"}
print(person["name"])   # Alice (clear!)
print(person["age"])    # 25 (clear!)
print(person["job"])    # Engineer (clear!)
```

This is a **dictionary**. It stores data using keys instead of indexes.

Dictionaries are essential for organizing complex data.

---

## The Mental Model: What Is a Dictionary?

A dictionary is like a **real dictionary or phonebook**.

In a phonebook:
- "Alice" → 555-1234
- "Bob" → 555-5678
- "Charlie" → 555-9012

In a Python dictionary:
- `"name"` → `"Alice"`
- `"age"` → 25
- `"job"` → `"Engineer"`

You look up by key to get value.

```python
person = {
    "name": "Alice",
    "age": 25,
    "job": "Engineer"
}

print(person["name"])  # Look up "name" → get "Alice"
print(person["age"])   # Look up "age" → get 25
```

---

## The Mental Model: Creating Dictionaries

**Empty dictionary:**
```python
empty = {}
```

**With data:**
```python
person = {
    "name": "Alice",
    "age": 25,
    "job": "Engineer"
}
```

**Keys must be strings (usually)**:
```python
scores = {
    "Alice": 85,
    "Bob": 92,
    "Charlie": 78
}
```

---

## The Mental Model: Accessing Values

Access by key (not index):

```python
person = {"name": "Alice", "age": 25}

print(person["name"])   # "Alice"
print(person["age"])    # 25
```

If key doesn't exist, you get an error. Use `in` to check:

```python
if "name" in person:
    print(person["name"])
else:
    print("Key not found")
```

---

## The Mental Model: Adding Items

Add new key-value pairs:

```python
person = {"name": "Alice"}

person["age"] = 25
person["job"] = "Engineer"

print(person)
# {'name': 'Alice', 'age': 25, 'job': 'Engineer'}
```

---

## The Mental Model: Changing Values

Update existing keys:

```python
person = {"name": "Alice", "age": 25}

person["age"] = 26  # Birthday!
print(person)
# {'name': 'Alice', 'age': 26}
```

---

## The Mental Model: Removing Items

**`del`** removes a key-value pair:

```python
person = {"name": "Alice", "age": 25, "job": "Engineer"}

del person["job"]
print(person)
# {'name': 'Alice', 'age': 25}
```

**`pop()`** removes and returns value:

```python
person = {"name": "Alice", "age": 25}

age = person.pop("age")
print(age)      # 25
print(person)   # {'name': 'Alice'}
```

---

## The Mental Model: Looping Over Dictionaries

Loop over keys:

```python
person = {"name": "Alice", "age": 25, "job": "Engineer"}

for key in person:
    print(key, ":", person[key])
```

**Output:**
```
name : Alice
age : 25
job : Engineer
```

Or loop over items:

```python
for key, value in person.items():
    print(key, ":", value)
```

---

## The Mental Model: Useful Methods

**`.keys()`** — Get all keys

```python
person = {"name": "Alice", "age": 25}
print(person.keys())   # dict_keys(['name', 'age'])
```

**`.values()`** — Get all values

```python
print(person.values()) # dict_values(['Alice', 25])
```

**`.items()`** — Get key-value pairs

```python
print(person.items())
# dict_items([('name', 'Alice'), ('age', 25)])
```

**`.get()`** — Safe access (returns None if missing)

```python
print(person.get("name"))      # "Alice"
print(person.get("missing"))   # None
print(person.get("missing", "N/A"))  # "N/A" (default)
```

---

## The Mental Model: Dictionaries vs Lists

**List:** Ordered, access by number

```python
colors = ["red", "green", "blue"]
print(colors[0])  # red
```

**Dictionary:** Unordered, access by name

```python
colors = {"primary": "red", "secondary": "green"}
print(colors["primary"])  # red
```

Use **lists** when order matters.  
Use **dictionaries** when you need named access.

---

## Key Concepts to Remember

1. **Dictionary stores key-value pairs**
2. **Access by key, not index**
3. **Keys are usually strings**
4. **Add items: `dict[key] = value`**
5. **Remove items: `del dict[key]`**
6. **Check existence: `if key in dict:`**
7. **Loop with `for key in dict:` or `.items()`**
8. **`.keys()`, `.values()`, `.items()` for inspection**
9. **`.get()` for safe access**
10. **`.pop()` to remove and return**

---

## Common Misconceptions

**"Dictionaries have indexes like lists"**

No. They use keys, not indexes. Keys are names.

**"Dictionary order is guaranteed"**

No (well, in modern Python 3.7+ it preserves insertion order, but don't rely on it).

**"Keys must be strings"**

Usually, but can be numbers or other immutable types.

**"I can use any key name"**

Yes, but use meaningful names. "name" not "n".

---

## Real-World Uses

- **Contact info:** `{"name": "Alice", "phone": "555-1234", "email": "..."}`
- **Product:** `{"id": 123, "name": "Widget", "price": 19.99}`
- **Settings:** `{"theme": "dark", "language": "English", "notifications": True}`
- **Database row:** Store each record as a dictionary
- **API response:** Most APIs return dictionaries (JSON)

---

## Summary

Dictionaries let you store and access data using meaningful names (keys) instead of numbers (indexes).

Instead of:
```python
person = ["Alice", 25, "Engineer"]
print(person[0])   # What is 0?
```

You write:
```python
person = {"name": "Alice", "age": 25, "job": "Engineer"}
print(person["name"])  # Clear!
```

Much more readable. Much more powerful.

Next: see dictionaries in action.
