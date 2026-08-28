# Lists: Exercises & Practice

## Exercise 1: Create and Access List

Create a program that creates a list and prints items.

**Expected output:**
```
List: ['apple', 'banana', 'cherry']
First item: apple
Last item: cherry
```

**What to do:**
1. Create a file called `simple_list.py`
2. Create list: `fruits = ["apple", "banana", "cherry"]`
3. Print the list
4. Print first item using index 0
5. Print last item using index -1
6. Run it

**Hint:** Use `fruits[0]` and `fruits[-1]`.

---

## Exercise 2: List Length

Create a program that tells you list length.

**Expected output:**
```
Students: ['Alice', 'Bob', 'Charlie', 'David']
Count: 4
```

**What to do:**
1. Create a file called `list_length.py`
2. Create list of 4 student names
3. Print the list
4. Print length using `len()`
5. Run it

**Hint:** `len(list)` gives count.

---

## Exercise 3: Append Items

Create a program that adds items to a list.

**Expected output:**
```
Before: ['apple', 'banana']
After: ['apple', 'banana', 'cherry', 'date']
```

**What to do:**
1. Create a file called `append_items.py`
2. Create list with 2 items
3. Print before
4. Append 2 more items
5. Print after
6. Run it

**Hint:** Use `list.append()`.

---

## Exercise 4: Insert at Position

Create a program that inserts item at specific position.

**Expected output:**
```
Before: ['apple', 'banana', 'cherry']
After: ['apple', 'grape', 'banana', 'cherry']
```

**What to do:**
1. Create a file called `insert_item.py`
2. Create list with 3 items
3. Print before
4. Insert item at index 1
5. Print after
6. Run it

**Hint:** Use `list.insert(index, item)`.

---

## Exercise 5: Remove by Value

Create a program that removes item by name.

**Expected output:**
```
Before: ['apple', 'banana', 'cherry', 'date']
After: ['apple', 'cherry', 'date']
```

**What to do:**
1. Create a file called `remove_item.py`
2. Create list with 4 items
3. Print before
4. Remove "banana"
5. Print after
6. Run it

**Hint:** Use `list.remove(item)`.

---

## Exercise 6: Pop Item

Create a program that removes and returns item by index.

**Expected output:**
```
Before: ['apple', 'banana', 'cherry']
Removed: banana
After: ['apple', 'cherry']
```

**What to do:**
1. Create a file called `pop_item.py`
2. Create list with 3 items
3. Print before
4. Pop item at index 1 and store in variable
5. Print removed item
6. Print after
7. Run it

**Hint:** Use `item = list.pop(index)`.

---

## Exercise 7: Loop Over List

Create a program that prints each item in list.

**Expected output:**
```
Fruits:
- apple
- banana
- cherry
```

**What to do:**
1. Create a file called `loop_list.py`
2. Create list of 3 fruits
3. Print "Fruits:"
4. Loop: `for fruit in fruits:`
5. Print each with "-" prefix
6. Run it

**Hint:** Use `for item in list:`.

---

## Exercise 8: Accumulate in Loop

Create a program that sums numbers in list.

**Expected output:**
```
Numbers: [10, 20, 30, 40]
Sum: 100
```

**What to do:**
1. Create a file called `sum_loop.py`
2. Create list of 4 numbers
3. Initialize total to 0
4. Loop: add each to total
5. Print sum
6. Run it

**Hint:** Use `for num in numbers: total += num`.

---

## Exercise 9: Check Membership

Create a program that checks if item exists in list.

**Program interaction:**
```
Is 'apple' in fruits? True
Is 'grape' in fruits? False
```

**What to do:**
1. Create a file called `check_membership.py`
2. Create list of 3 fruits
3. Check if "apple" in list
4. Check if "grape" in list
5. Print results
6. Run it

**Hint:** Use `if item in list:`.

---

## Exercise 10: Find Index

Create a program that finds index of item.

**Expected output:**
```
Index of 'banana': 1
```

**What to do:**
1. Create a file called `find_index.py`
2. Create list of fruits
3. Use `list.index(item)` to find position
4. Print index
5. Run it

**Hint:** `list.index("item")` returns index.

---

## Exercise 11: Slice a List

Create a program that extracts portion of list.

**Expected output:**
```
Original: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
First 3: [0, 1, 2]
Middle: [3, 4, 5, 6]
Last 3: [7, 8, 9]
```

**What to do:**
1. Create a file called `slice_list.py`
2. Create list of numbers 0-9
3. Print original
4. Print slice [0:3]
5. Print slice [3:7]
6. Print slice [7:]
7. Run it

**Hint:** Use `list[start:stop]` syntax.

---

## Exercise 12: Real-World - Grades

Create a program that processes grade list.

**Expected output:**
```
Scores: [85, 92, 78, 95, 88]
Highest: 95
Lowest: 78
Average: 87.6
```

**What to do:**
1. Create a file called `grades.py`
2. Create list of 5 test scores
3. Use `max()` to find highest
4. Use `min()` to find lowest
5. Use `sum()` to find total
6. Calculate average
7. Run it

**Hint:** `max()`, `min()`, `sum()` work on lists.

---

## Exercise 13: Sort a List

Create a program that sorts numbers.

**Expected output:**
```
Before: [5, 2, 8, 1, 9, 3]
Sorted ascending: [1, 2, 3, 5, 8, 9]
Sorted descending: [9, 8, 5, 3, 2, 1]
```

**What to do:**
1. Create a file called `sort_list.py`
2. Create list of random numbers
3. Print before
4. Sort with `list.sort()`
5. Print sorted
6. Sort reverse with `list.sort(reverse=True)`
7. Print descending
8. Run it

**Hint:** `list.sort()` modifies list. `sorted(list)` creates new.

---

## Exercise 14: Build List from Input

Create a program that builds list from user input.

**Program interaction:**
```
How many numbers? 3
Enter number 1: 10
Enter number 2: 20
Enter number 3: 30
Your numbers: [10, 20, 30]
Sum: 60
Average: 20.0
```

**What to do:**
1. Create a file called `build_list.py`
2. Ask how many numbers
3. Loop that many times
4. Get number each time
5. Append to list
6. Print list
7. Print sum and average
8. Run it

**Hint:** Use `list.append()` in loop.

---

## Exercise 15: Real-World - Todo List

Create a simple todo list program.

**Program interaction:**
```
Todo List
1. Add item
2. Remove item
3. Show list
4. Exit
Choose: 1
Enter item: Buy milk
Item added!

1. Add item
2. Remove item
3. Show list
4. Exit
Choose: 3
Your todos: ['Buy milk']

1. Add item
2. Remove item
3. Show list
4. Exit
Choose: 4
Goodbye!
```

**What to do:**
1. Create a file called `todo_list.py`
2. Create empty list
3. Loop menu until exit
4. Option 1: get item and append
5. Option 2: remove item
6. Option 3: print list
7. Option 4: break
8. Run it

**Hint:** Menu loop with if/elif.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Can I create a list?
- ✓ Can I access items by index?
- ✓ Can I add and remove items?
- ✓ Can I loop over a list?
- ✓ Do I understand negative indexing?

---

## Important Observations

**About Lists:**
- Lists hold multiple items
- Zero-indexed (first is 0)
- Can access by positive or negative index
- Can add/remove items
- Can loop with `for`
- Can slice to extract portions
- Dynamic (grow/shrink as needed)

---

## Next Steps

Once you've mastered lists:

1. You can work with collections of data
2. You can process multiple items
3. You can store variable amounts of data
4. You're ready for dictionaries (key-value pairs)

You're ready for **Topic 13: Dictionaries**

Dictionaries let you organize data by names (keys) instead of numbers (indexes).

Excellent progress! 🎉
