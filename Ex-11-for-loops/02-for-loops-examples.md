# For Loops: Examples & Demos

## Example 1: Simple For Loop - Count 0 to 4

**Code:**
```python
for count in range(5):
    print(count)
```

**Output:**
```
0
1
2
3
4
```

**Execution flow:**

`range(5)` creates: 0, 1, 2, 3, 4

Loop runs 5 times, `count` takes each value

**Key insight:** Loop variable updates automatically.

---

## Example 2: For Loop with range(1, 6)

**Code:**
```python
for num in range(1, 6):
    print(num)
```

**Output:**
```
1
2
3
4
5
```

**Explanation:**

`range(1, 6)` starts at 1, goes up to (but not including) 6

**Key insight:** Start and stop: `range(start, stop)`.

---

## Example 3: For Loop with Step

**Code:**
```python
for num in range(0, 10, 2):
    print(num)
```

**Output:**
```
0
2
4
6
8
```

**Explanation:**

`range(0, 10, 2)` starts at 0, goes to 10 (not included), stepping by 2

**Key insight:** Third argument is the step size.

---

## Example 4: Countdown with For Loop

**Code:**
```python
for num in range(5, 0, -1):
    print(num)

print("Blastoff!")
```

**Output:**
```
5
4
3
2
1
Blastoff!
```

**Explanation:**

`range(5, 0, -1)` starts at 5, goes down to 1, stepping by -1

**Key insight:** Negative step counts down.

---

## Example 5: Multiplication Table

**Code:**
```python
num = 5

for multiplier in range(1, 11):
    result = num * multiplier
    print(str(num) + " x " + str(multiplier) + " = " + str(result))
```

**Output:**
```
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

**Key insight:** Use loop for repetitive calculations.

---

## Example 6: Sum Numbers 1 to 10

**Code:**
```python
total = 0

for num in range(1, 11):
    total += num

print("Sum:", total)
```

**Output:**
```
Sum: 55
```

**Explanation:**

1+2+3+4+5+6+7+8+9+10 = 55

**Key insight:** Accumulate values in a for loop.

---

## Example 7: Nested For Loop - Multiplication Grid

**Code:**
```python
for i in range(1, 4):
    for j in range(1, 4):
        print(str(i) + "," + str(j), end=" ")
    print()  # New line after each outer iteration
```

**Output:**
```
1,1 1,2 1,3 
2,1 2,2 2,3 
3,1 3,2 3,3 
```

**Explanation:**

Outer loop runs 3 times. For each, inner loop runs 3 times.

**Key insight:** Nested loops for 2D patterns.

---

## Example 8: Using `break` in For Loop

**Code:**
```python
for num in range(1, 11):
    if num == 5:
        break
    print(num)

print("Done")
```

**Output:**
```
1
2
3
4
Done
```

**Key insight:** `break` exits loop early.

---

## Example 9: Using `continue` in For Loop

**Code:**
```python
for num in range(1, 6):
    if num == 3:
        continue
    print(num)
```

**Output:**
```
1
2
4
5
```

**Key insight:** `continue` skips current iteration.

---

## Example 10: For Loop Over List

**Code:**
```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print("I like " + fruit)
```

**Output:**
```
I like apple
I like banana
I like cherry
```

**Key insight:** Iterate over each item in a list.

---

## Example 11: Counting Even Numbers

**Code:**
```python
count = 0

for num in range(1, 21):
    if num % 2 == 0:
        count += 1

print("Even numbers from 1-20:", count)
```

**Output:**
```
Even numbers from 1-20: 10
```

**Key insight:** Count items matching a condition.

---

## Example 12: Finding Maximum

**Code:**
```python
max_num = 0

for num in range(1, 11):
    if num > max_num:
        max_num = num

print("Maximum:", max_num)
```

**Output:**
```
Maximum: 10
```

**Key insight:** Track max value while looping.

---

## Example 13: Building a String with Loop

**Code:**
```python
result = ""

for letter in "hello":
    result += letter.upper()

print(result)
```

**Output:**
```
HELLO
```

**Key insight:** You can loop over strings character by character.

---

## Example 14: Nested Loop - Pyramid Pattern

**Code:**
```python
for i in range(1, 6):
    for j in range(i):
        print("*", end="")
    print()
```

**Output:**
```
*
**
***
****
*****
```

**Key insight:** Nested loops create 2D patterns.

---

## Example 15: Real-World - Checking Grades

**Code:**
```python
scores = [85, 92, 78, 95, 88]
total = 0

for score in scores:
    total += score

average = total / len(scores)

print("Average score:", average)
```

**Output:**
```
Average score: 87.6
```

**Key insight:** Process items in a list with for loop.

---

## Summary of Examples

- For loops repeat N times
- `range()` creates number sequences
- Loop variable updates automatically
- Can break or continue
- Can iterate over lists
- Nested loops create 2D structures
- Great for calculations and patterns

Next: practice with exercises.
