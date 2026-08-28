# For Loops: Controlled Repetition - Lecture

## Why This Matters

While loops repeat "as long as a condition is true."

But sometimes you know exactly how many times you want to repeat:

- Print numbers 1 to 10
- Process each item in a list
- Run something 5 times
- Do math 100 times

A **for loop** repeats a specific number of times. It's cleaner than while loops for these situations.

For loops are the most common loop in programming. You'll use them constantly.

---

## The Mental Model: For Loop vs. While Loop

**While loop:** "Repeat while something is true"

```python
count = 0
while count < 5:
    print(count)
    count += 1
```

**For loop:** "Repeat for each item" or "Repeat N times"

```python
for count in range(5):
    print(count)
```

Much cleaner. No need to manage count manually.

---

## The Mental Model: What Is `range()`?

`range()` creates a sequence of numbers.

```python
range(5)           # 0, 1, 2, 3, 4
range(1, 6)        # 1, 2, 3, 4, 5
range(0, 10, 2)    # 0, 2, 4, 6, 8
```

- `range(5)` = 0 to 4 (5 numbers)
- `range(1, 6)` = 1 to 5 (start=1, stop=6)
- `range(0, 10, 2)` = every 2nd number from 0 to 9

For loops use `range()` to repeat N times.

---

## The Mental Model: Basic For Loop

```python
for count in range(5):
    print(count)
```

Execution:

1. Loop variable `count` takes first value: 0
2. Run the loop body
3. `count` takes next value: 1
4. Run the loop body
5. ... (repeat for each value in range)
6. When range exhausted, exit loop

**Output:**
```
0
1
2
3
4
```

The variable `count` automatically changes each iteration.

---

## The Mental Model: For Loop with Custom Range

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

`range(1, 6)` starts at 1, goes up to (but not including) 6.

---

## The Mental Model: For Loop with Step

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

The third argument is the step (increment).

---

## The Mental Model: For Loop Over a List

For loops shine when iterating over lists (which we'll learn soon):

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

The loop variable automatically takes each item.

---

## The Mental Model: Nested For Loops

You can put loops inside loops:

```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

**Output:**
```
i=0, j=0
i=0, j=1
i=1, j=0
i=1, j=1
i=2, j=0
i=2, j=1
```

Outer loop runs 3 times. For each iteration, inner loop runs 2 times. Total: 3 × 2 = 6 iterations.

---

## The Mental Model: Break and Continue

Just like while loops, for loops support `break` and `continue`:

**`break`** exits loop early:

```python
for num in range(10):
    if num == 5:
        break
    print(num)
```

**`continue`** skips to next iteration:

```python
for num in range(5):
    if num == 2:
        continue
    print(num)
```

---

## Key Concepts to Remember

1. **For loop repeats** a known number of times
2. **`range(n)`** creates sequence 0 to n-1
3. **`range(a, b)`** creates a to b-1
4. **`range(a, b, c)`** creates a to b-1 stepping by c
5. **Loop variable** automatically updates
6. **`break`** exits early
7. **`continue`** skips to next
8. **No manual counter management** needed

---

## For Loop vs. While Loop - When to Use?

**Use while when:** You don't know how many times to repeat

```python
while password != "correct":
    password = input("Enter password: ")
```

**Use for when:** You know exactly how many times to repeat

```python
for i in range(10):
    print(i)
```

---

## Real-World Uses

- **Processing lists:** For each item, do something
- **Counting:** Repeat N times
- **Tables:** Print multiplication tables
- **Patterns:** Generate patterns
- **Summation:** Add up ranges of numbers
- **Grids:** Nested loops for 2D structures

---

## Common Misconceptions

**"For loops are faster than while"**

Not significantly. Speed depends on what you do inside.

**"I have to use `i` and `j`"**

No. Use descriptive names: `for student in students:` is better than `for s in students:`.

**"range(5) goes 0 to 5"**

No. It goes 0 to 4 (5 numbers).

**"I have to break at the end"**

No. Loop exits naturally when range exhausted.

---

## Summary

For loops repeat a fixed number of times, making them perfect for known-count repetitions. They're simpler than while loops when you know the count.

`range()` is your tool for creating sequences to loop over.

Next: see for loops in action.
