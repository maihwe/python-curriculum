# Dictionaries: Exercises & Practice

## Exercise 1: Create and Access Dictionary

Create a program that creates a dictionary and accesses values.

**Expected output:**
```
Person: {'name': 'Alice', 'age': 25, 'city': 'NYC'}
Name: Alice
Age: 25
```

**What to do:**
1. Create a file called `simple_dict.py`
2. Create dictionary with 3 key-value pairs
3. Print dictionary
4. Print two values using keys
5. Run it

**Hint:** Use `dict[key]` to access.

---

## Exercise 2: Adding Items to Dictionary

Create a program that adds new keys.

**Expected output:**
```
Before: {'name': 'Alice', 'age': 25}
After: {'name': 'Alice', 'age': 25, 'city': 'NYC', 'job': 'Engineer'}
```

**What to do:**
1. Create a file called `add_to_dict.py`
2. Create dictionary with 2 items
3. Print before
4. Add 2 new keys
5. Print after
6. Run it

**Hint:** Use `dict[key] = value` to add.

---

## Exercise 3: Updating Values

Create a program that changes existing values.

**Expected output:**
```
Before: {'name': 'Alice', 'age': 25}
After: {'name': 'Alicia', 'age': 26}
```

**What to do:**
1. Create a file called `update_dict.py`
2. Create dictionary
3. Print before
4. Update 2 values
5. Print after
6. Run it

**Hint:** Assign to existing key to update.

---

## Exercise 4: Checking Key Existence

Create a program that checks if keys exist.

**Program interaction:**
```
Is 'name' in person? True
Is 'email' in person? False
```

**What to do:**
1. Create a file called `check_key.py`
2. Create dictionary
3. Check if "name" exists
4. Check if "email" exists
5. Print results
6. Run it

**Hint:** Use `if key in dict:`.

---

## Exercise 5: Deleting Items

Create a program that removes keys.

**Expected output:**
```
Before: {'name': 'Alice', 'age': 25, 'city': 'NYC'}
After: {'name': 'Alice', 'age': 25}
```

**What to do:**
1. Create a file called `delete_key.py`
2. Create dictionary
3. Print before
4. Delete a key
5. Print after
6. Run it

**Hint:** Use `del dict[key]`.

---

## Exercise 6: Using pop()

Create a program that removes and returns value.

**Expected output:**
```
Removed: 25
After: {'name': 'Alice'}
```

**What to do:**
1. Create a file called `pop_key.py`
2. Create dictionary
3. Pop a key and store in variable
4. Print removed value
5. Print dictionary after
6. Run it

**Hint:** `value = dict.pop(key)`.

---

## Exercise 7: Looping Over Dictionary

Create a program that prints all key-value pairs.

**Expected output:**
```
Scores:
Alice : 85
Bob : 92
Charlie : 78
```

**What to do:**
1. Create a file called `loop_dict.py`
2. Create dictionary of scores
3. Print "Scores:"
4. Loop: `for name in scores:`
5. Print each pair
6. Run it

**Hint:** Use `for key in dict:`.

---

## Exercise 8: Using .items()

Create a program that loops with `.items()`.

**Expected output:**
```
Person:
name : Alice
age : 25
city : NYC
```

**What to do:**
1. Create a file called `dict_items.py`
2. Create dictionary
3. Loop with `.items()`
4. Print each key-value pair
5. Run it

**Hint:** `for key, value in dict.items():`.

---

## Exercise 9: Getting Keys and Values

Create a program that shows all keys and values.

**Expected output:**
```
Keys: ['name', 'age', 'city']
Values: ['Alice', 25, 'NYC']
```

**What to do:**
1. Create a file called `dict_inspection.py`
2. Create dictionary
3. Use `.keys()` to show all keys
4. Use `.values()` to show all values
5. Run it

**Hint:** Convert to list for printing.

---

## Exercise 10: Safe Access with get()

Create a program that uses `.get()`.

**Program interaction:**
```
Phone: 555-1234
Email: not provided
```

**What to do:**
1. Create a file called `safe_access.py`
2. Create dictionary with some keys
3. Use `.get()` for existing key
4. Use `.get()` for missing key with default
5. Print results
6. Run it

**Hint:** `.get(key, default)`.

---

## Exercise 11: Dictionary of Lists

Create a program with lists as values.

**Expected output:**
```
Alice's scores: [85, 90, 88]
Bob's scores: [92, 95, 89]
Average: 91.33333333333333
```

**What to do:**
1. Create a file called `dict_lists.py`
2. Create dictionary where values are lists
3. Print scores for two people
4. Calculate average for one person
5. Run it

**Hint:** `dict[key]` returns the list.

---

## Exercise 12: List of Dictionaries

Create a program with list of dictionaries.

**Expected output:**
```
Alice is 25 years old
Bob is 30 years old
Charlie is 28 years old
```

**What to do:**
1. Create a file called `list_dicts.py`
2. Create list of dictionaries
3. Loop through list
4. Print info from each
5. Run it

**Hint:** `for person in people: person[key]`.

---

## Exercise 13: Real-World - Student Database

Create a program storing student info.

**Program interaction:**
```
Student Database
1. Add student
2. Show student
3. List all
4. Exit

Choose: 1
Name: Alice
Math grade: 85
English grade: 90
Student added!

Choose: 2
Name: Alice
Math: 85
English: 90

Choose: 3
Alice: Math=85, English=90

Choose: 4
Goodbye!
```

**What to do:**
1. Create a file called `student_db.py`
2. Create empty dictionary
3. Implement menu loop
4. Option 1: add student (nested dict)
5. Option 2: show student
6. Option 3: list all students
7. Option 4: exit
8. Run it

**Hint:** Dictionary of dictionaries.

---

## Exercise 14: Counting with Dictionary

Create a program that counts items.

**Program interaction:**
```
Text: hello world
Character counts: {'h': 1, 'e': 1, 'l': 3, 'o': 2, ' ': 1, 'w': 1, 'r': 1, 'd': 1}
```

**What to do:**
1. Create a file called `character_count.py`
2. Get text from user
3. Create empty dictionary
4. Loop through characters
5. Count each character
6. Print results
7. Run it

**Hint:** Check if key exists, increment or create.

---

## Exercise 15: Real-World - Product Inventory

Create a program managing inventory.

**Program interaction:**
```
Inventory Menu
1. Add product
2. Remove stock
3. Check stock
4. Show all
5. Exit

Choose: 1
Product name: Widget
Stock: 100
Product added!

Choose: 3
Product: Widget
Current stock: 100

Choose: 2
Product: Widget
Remove how much: 25
New stock: 75

Choose: 4
Widget: 75 units

Choose: 5
Goodbye!
```

**What to do:**
1. Create a file called `inventory.py`
2. Create dictionary for products
3. Implement menu loop
4. Option 1: add product with stock
5. Option 2: remove stock
6. Option 3: check stock
7. Option 4: list all
8. Option 5: exit
9. Run it

**Hint:** Values are stock quantities.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Can I create a dictionary?
- ✓ Can I access values by key?
- ✓ Can I add and remove keys?
- ✓ Can I loop over a dictionary?
- ✓ Do I understand when to use dict vs list?

---

## Important Observations

**About Dictionaries:**
- Store key-value pairs
- Access by key, not index
- Keys are usually strings
- Dynamic (add/remove as needed)
- Great for named access
- Perfect for real-world data

---

## Next Steps

Once you've mastered dictionaries:

1. You can store complex data structures
2. You can organize data meaningfully
3. You can build real applications
4. You're ready for functions

You're making excellent progress! 🎉

You've now learned the **four basic data types:**
- Strings
- Numbers
- Lists
- Dictionaries

With these, you can solve most beginner problems.
