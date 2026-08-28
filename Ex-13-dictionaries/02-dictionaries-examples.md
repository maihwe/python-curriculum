# Dictionaries: Examples & Demos

## Example 1: Creating and Accessing a Dictionary

**Code:**
```python
person = {
    "name": "Alice",
    "age": 25,
    "city": "New York"
}

print("Dictionary:", person)
print("Name:", person["name"])
print("Age:", person["age"])
print("City:", person["city"])
```

**Output:**
```
Dictionary: {'name': 'Alice', 'age': 25, 'city': 'New York'}
Name: Alice
Age: 25
City: New York
```

**Key insight:** Access by key, not index.

---

## Example 2: Adding New Items

**Code:**
```python
person = {"name": "Alice", "age": 25}
print("Before:", person)

person["city"] = "New York"
person["job"] = "Engineer"

print("After:", person)
```

**Output:**
```
Before: {'name': 'Alice', 'age': 25}
After: {'name': 'Alice', 'age': 25, 'city': 'New York', 'job': 'Engineer'}
```

**Key insight:** Dictionaries grow dynamically.

---

## Example 3: Changing Values

**Code:**
```python
person = {"name": "Alice", "age": 25}
print("Before:", person)

person["age"] = 26
person["name"] = "Alicia"

print("After:", person)
```

**Output:**
```
Before: {'name': 'Alice', 'age': 25}
After: {'name': 'Alicia', 'age': 26}
```

**Key insight:** Update by assigning to key.

---

## Example 4: Checking if Key Exists

**Code:**
```python
person = {"name": "Alice", "age": 25}

if "name" in person:
    print("Name found:", person["name"])
else:
    print("Name not found")

if "email" in person:
    print("Email found:", person["email"])
else:
    print("Email not found")
```

**Output:**
```
Name found: Alice
Email not found
```

**Key insight:** Use `in` to check before accessing.

---

## Example 5: Removing Items with del

**Code:**
```python
person = {"name": "Alice", "age": 25, "city": "NYC"}
print("Before:", person)

del person["city"]

print("After:", person)
```

**Output:**
```
Before: {'name': 'Alice', 'age': 25, 'city': 'NYC'}
After: {'name': 'Alice', 'age': 25}
```

**Key insight:** `del` removes key-value pair.

---

## Example 6: Using pop()

**Code:**
```python
person = {"name": "Alice", "age": 25}
print("Before:", person)

age = person.pop("age")
print("Removed:", age)
print("After:", person)
```

**Output:**
```
Before: {'name': 'Alice', 'age': 25}
Removed: 25
After: {'name': 'Alice'}
```

**Key insight:** `pop()` removes and returns value.

---

## Example 7: Looping Over Keys

**Code:**
```python
scores = {
    "Alice": 85,
    "Bob": 92,
    "Charlie": 78
}

print("Scores:")
for name in scores:
    print(name, ":", scores[name])
```

**Output:**
```
Scores:
Alice : 85
Bob : 92
Charlie : 78
```

**Key insight:** Loop over keys with `for key in dict:`.

---

## Example 8: Looping Over Items

**Code:**
```python
scores = {
    "Alice": 85,
    "Bob": 92,
    "Charlie": 78
}

print("Scores:")
for name, score in scores.items():
    print(name, ":", score)
```

**Output:**
```
Scores:
Alice : 85
Bob : 92
Charlie : 78
```

**Key insight:** `.items()` gives key-value pairs directly.

---

## Example 9: Getting Keys and Values

**Code:**
```python
person = {"name": "Alice", "age": 25, "city": "NYC"}

print("Keys:", list(person.keys()))
print("Values:", list(person.values()))
print("Items:", list(person.items()))
```

**Output:**
```
Keys: ['name', 'age', 'city']
Values: ['Alice', 25, 'NYC']
Items: [('name', 'Alice'), ('age', 25), ('city', 'NYC')]
```

**Key insight:** Methods to inspect dictionary.

---

## Example 10: Using get() for Safe Access

**Code:**
```python
person = {"name": "Alice", "age": 25}

print("Name:", person.get("name"))
print("Email:", person.get("email"))
print("Email (default):", person.get("email", "not provided"))
```

**Output:**
```
Name: Alice
Email: None
Email (default): not provided
```

**Key insight:** `.get()` returns None if missing (safe).

---

## Example 11: Dictionary of Lists

**Code:**
```python
grades = {
    "Alice": [85, 90, 88],
    "Bob": [92, 95, 89],
    "Charlie": [78, 82, 80]
}

print("Alice's grades:", grades["Alice"])
print("Alice's average:", sum(grades["Alice"]) / len(grades["Alice"]))
```

**Output:**
```
Alice's grades: [85, 90, 88]
Alice's average: 87.66666666666667
```

**Key insight:** Dictionaries can contain lists as values.

---

## Example 12: List of Dictionaries

**Code:**
```python
people = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 28}
]

for person in people:
    print(person["name"], "is", person["age"], "years old")
```

**Output:**
```
Alice is 25 years old
Bob is 30 years old
Charlie is 28 years old
```

**Key insight:** List containing dictionaries.

---

## Example 13: Counting with Dictionary

**Code:**
```python
text = "hello"
letter_count = {}

for letter in text:
    if letter in letter_count:
        letter_count[letter] += 1
    else:
        letter_count[letter] = 1

print(letter_count)
```

**Output:**
```
{'h': 1, 'e': 1, 'l': 2, 'o': 1}
```

**Key insight:** Use dictionary to tally occurrences.

---

## Example 14: Merging Dictionaries

**Code:**
```python
person = {"name": "Alice", "age": 25}
address = {"city": "NYC", "zip": "10001"}

# Merge
person.update(address)

print(person)
```

**Output:**
```
{'name': 'Alice', 'age': 25, 'city': 'NYC', 'zip': '10001'}
```

**Key insight:** `.update()` combines dictionaries.

---

## Example 15: Real-World - Contact Database

**Code:**
```python
contacts = {
    "Alice": {"phone": "555-1234", "email": "alice@example.com"},
    "Bob": {"phone": "555-5678", "email": "bob@example.com"},
    "Charlie": {"phone": "555-9012", "email": "charlie@example.com"}
}

name = "Alice"
if name in contacts:
    contact = contacts[name]
    print(name + "'s phone:", contact["phone"])
    print(name + "'s email:", contact["email"])
```

**Output:**
```
Alice's phone: 555-1234
Alice's email: alice@example.com
```

**Key insight:** Dictionaries perfect for real-world data.

---

## Summary of Examples

- Create and access by key
- Add, change, remove items
- Check membership with `in`
- Loop over keys or items
- Inspect with `.keys()`, `.values()`, `.items()`
- Safe access with `.get()`
- Nest dictionaries and lists
- Count occurrences
- Store complex data

Next: practice with exercises.
