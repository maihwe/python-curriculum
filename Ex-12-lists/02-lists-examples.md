# Lists: Examples & Demos

## Example 1: Creating and Accessing a List

**Code:**
```python
fruits = ["apple", "banana", "cherry"]

print("List:", fruits)
print("First item (index 0):", fruits[0])
print("Second item (index 1):", fruits[1])
print("Third item (index 2):", fruits[2])
```

**Output:**
```
List: ['apple', 'banana', 'cherry']
First item (index 0): apple
Second item (index 1): banana
Third item (index 2): cherry
```

**Key insight:** Access items by index. First is 0, not 1.

---

## Example 2: Negative Indexing

**Code:**
```python
fruits = ["apple", "banana", "cherry", "date"]

print("Last item:", fruits[-1])
print("Second to last:", fruits[-2])
print("Third to last:", fruits[-3])
print("Fourth to last:", fruits[-4])
```

**Output:**
```
Last item: date
Second to last: cherry
Third to last: banana
Fourth to last: apple
```

**Key insight:** Negative index counts from end. -1 is last item.

---

## Example 3: List Length

**Code:**
```python
fruits = ["apple", "banana", "cherry"]
numbers = [10, 20, 30, 40, 50]
empty = []

print("Length of fruits:", len(fruits))
print("Length of numbers:", len(numbers))
print("Length of empty list:", len(empty))
```

**Output:**
```
Length of fruits: 3
Length of numbers: 5
Length of empty list: 0
```

**Key insight:** `len()` tells you how many items.

---

## Example 4: Appending Items

**Code:**
```python
fruits = ["apple", "banana"]
print("Before:", fruits)

fruits.append("cherry")
print("After append:", fruits)

fruits.append("date")
print("After another append:", fruits)
```

**Output:**
```
Before: ['apple', 'banana']
After append: ['apple', 'banana', 'cherry']
After another append: ['apple', 'banana', 'cherry', 'date']
```

**Key insight:** `append()` adds to end. Modifies original list.

---

## Example 5: Inserting at Position

**Code:**
```python
fruits = ["apple", "banana", "cherry"]
print("Before:", fruits)

fruits.insert(1, "grape")
print("After insert at index 1:", fruits)

fruits.insert(0, "avocado")
print("After insert at index 0:", fruits)
```

**Output:**
```
Before: ['apple', 'banana', 'cherry']
After insert at index 1: ['apple', 'grape', 'banana', 'cherry']
After insert at index 0: ['avocado', 'apple', 'grape', 'banana', 'cherry']
```

**Key insight:** `insert()` adds at specific position. Shifts others.

---

## Example 6: Removing by Value

**Code:**
```python
fruits = ["apple", "banana", "cherry", "banana"]
print("Before:", fruits)

fruits.remove("banana")
print("After remove:", fruits)
```

**Output:**
```
Before: ['apple', 'banana', 'cherry', 'banana']
After remove: ['apple', 'cherry', 'banana']
```

**Key insight:** `remove()` removes first occurrence.

---

## Example 7: Removing by Index with pop()

**Code:**
```python
fruits = ["apple", "banana", "cherry"]
print("Before:", fruits)

removed = fruits.pop(1)
print("Removed item:", removed)
print("After pop:", fruits)
```

**Output:**
```
Before: ['apple', 'banana', 'cherry']
Removed item: banana
After pop: ['apple', 'cherry']
```

**Key insight:** `pop()` removes by index and returns item.

---

## Example 8: Looping Over List

**Code:**
```python
fruits = ["apple", "banana", "cherry"]

print("Items in list:")
for fruit in fruits:
    print("-", fruit)
```

**Output:**
```
Items in list:
- apple
- banana
- cherry
```

**Key insight:** Loop with `for` to process each item.

---

## Example 9: Looping with Index

**Code:**
```python
fruits = ["apple", "banana", "cherry"]

print("Items with indexes:")
for i in range(len(fruits)):
    print(i, ":", fruits[i])
```

**Output:**
```
Items with indexes:
0 : apple
1 : banana
2 : cherry
```

**Key insight:** Use `range(len())` to loop with indexes.

---

## Example 10: Checking Membership with `in`

**Code:**
```python
fruits = ["apple", "banana", "cherry"]

if "apple" in fruits:
    print("Found apple!")
else:
    print("No apple")

if "grape" in fruits:
    print("Found grape!")
else:
    print("No grape")
```

**Output:**
```
Found apple!
No grape
```

**Key insight:** Use `in` to check if item exists.

---

## Example 11: Slicing Lists

**Code:**
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print("Original:", numbers)
print("numbers[2:5]:", numbers[2:5])
print("numbers[:3]:", numbers[:3])
print("numbers[7:]:", numbers[7:])
print("numbers[::2]:", numbers[::2])
```

**Output:**
```
Original: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[2:5]: [2, 3, 4]
numbers[:3]: [0, 1, 2]
numbers[7:]: [7, 8, 9]
numbers[::2]: [0, 2, 4, 6, 8]
```

**Key insight:** Slicing creates new list. Original unchanged.

---

## Example 12: Summing List

**Code:**
```python
numbers = [10, 20, 30, 40]
total = sum(numbers)

print("Numbers:", numbers)
print("Sum:", total)
print("Average:", total / len(numbers))
```

**Output:**
```
Numbers: [10, 20, 30, 40]
Sum: 100
Average: 25.0
```

**Key insight:** `sum()` adds all items.

---

## Example 13: Finding Max and Min

**Code:**
```python
scores = [85, 92, 78, 95, 88]

print("Scores:", scores)
print("Highest:", max(scores))
print("Lowest:", min(scores))
```

**Output:**
```
Scores: [85, 92, 78, 95, 88]
Highest: 95
Lowest: 78
```

**Key insight:** `max()` and `min()` find extremes.

---

## Example 14: Sorting a List

**Code:**
```python
numbers = [5, 2, 8, 1, 9, 3]
print("Before:", numbers)

numbers.sort()
print("After sort:", numbers)

numbers.sort(reverse=True)
print("Reverse sort:", numbers)
```

**Output:**
```
Before: [5, 2, 8, 1, 9, 3]
After sort: [1, 2, 3, 5, 8, 9]
Reverse sort: [9, 8, 5, 3, 2, 1]
```

**Key insight:** `sort()` arranges items. `reverse=True` for descending.

---

## Example 15: Building List from User Input

**Code:**
```python
numbers = []

for i in range(3):
    num = int(input("Enter a number: "))
    numbers.append(num)

print("Numbers:", numbers)
print("Sum:", sum(numbers))
print("Average:", sum(numbers) / len(numbers))
```

**Program interaction:**
```
Enter a number: 10
Enter a number: 20
Enter a number: 30
Numbers: [10, 20, 30]
Sum: 60
Average: 20.0
```

**Key insight:** Dynamically build lists. Grow as you go.

---

## Summary of Examples

- Create and access lists by index
- Negative indexing from end
- `append()` and `insert()` to add
- `remove()` and `pop()` to delete
- Loop with `for` to process
- Slice to extract portions
- `in` to check membership
- `sum()`, `max()`, `min()` for calculations
- `sort()` to arrange
- Build dynamically from input

Next: practice with exercises.
