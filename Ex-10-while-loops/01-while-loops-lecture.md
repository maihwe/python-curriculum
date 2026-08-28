# While Loops: Repeating Actions - Lecture

## Why This Matters

So far, your programs run once from top to bottom.

```python
name = input("What is your name? ")
print("Hello, " + name)
```

Each line runs exactly once. If you want to do something multiple times, you copy/paste code—which is bad.

Real programs repeat actions:

- A game loop that runs until the game ends
- Asking for input repeatedly until valid
- Processing items in a list
- Counting from 1 to 100
- Running until a condition changes

A **while loop** repeats a block of code as long as a condition is true.

This is how programs become dynamic and powerful.

---

## The Mental Model: What Is a Loop?

A loop is a **fork in the road that curves back**.

```
Print "Hello"
    ↓
Is count < 5?
    ↓ Yes
count += 1
    ↓
Go back to "Is count < 5?"
    ↓ No
Continue to next code
```

The code repeats, checking a condition each time. When the condition is false, the loop exits.

---

## The Mental Model: Basic While Loop

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

Execution:

1. `count = 0`
2. Check: is `0 < 5`? → Yes, enter loop
3. Print `0`
4. `count = 1`
5. Check: is `1 < 5`? → Yes, continue loop
6. Print `1`
7. `count = 2`
... (repeats) ...
5. Check: is `5 < 5`? → No, exit loop

**Output:**
```
0
1
2
3
4
```

---

## The Mental Model: Loop Structure

Every while loop has three parts:

```python
count = 0                # 1. Initialize variable
while count < 5:         # 2. Check condition
    print(count)         # 3. Do something
    count += 1           # 4. Update variable (or loop repeats forever!)
```

**Critical:** You MUST update the variable, or the condition never changes, and the loop runs forever (infinite loop).

---

## The Mental Model: Infinite Loops

If you don't update the condition variable, you get an infinite loop:

```python
count = 0

while count < 5:
    print(count)
    # MISSING: count += 1
    # count never changes, so count < 5 is always true
    # Loop runs forever!
```

This is a **bug**. The program never exits.

---

## The Mental Model: Loop Control - break

Sometimes you want to exit a loop early:

```python
while True:
    name = input("Enter your name (or 'quit' to exit): ")
    if name == "quit":
        break
    print("Hello, " + name)
```

`break` exits the loop immediately, even if the condition is still true.

---

## The Mental Model: Loop Control - continue

Sometimes you want to skip the rest of the loop and go to the next iteration:

```python
count = 0

while count < 5:
    count += 1
    if count == 3:
        continue
    print(count)
```

When `count == 3`, `continue` skips the print and goes back to check the condition.

**Output:**
```
1
2
4
5
```

Notice 3 is skipped.

---

## The Mental Model: Using Loops with Input

A common pattern: keep asking until valid input:

```python
age = -1

while age < 0:
    age = int(input("Enter your age: "))
    if age < 0:
        print("Age must be positive")
```

Loop repeats until user enters valid input.

---

## The Mental Model: Accumulating Values

Loops are great for accumulating totals:

```python
total = 0
count = 0

while count < 5:
    num = int(input("Enter a number: "))
    total += num
    count += 1

print("Sum:", total)
```

Each iteration adds to the total.

---

## Key Concepts to Remember

1. **While loop repeats** as long as condition is true
2. **Must update condition variable** or get infinite loop
3. **`break`** exits loop early
4. **`continue`** skips to next iteration
5. **Indentation matters** (just like if/else)
6. Common pattern: validate input
7. Common pattern: accumulate values
8. Loops run top to bottom, then back to check condition

---

## Common Mistakes

**"My loop runs forever"**

You're probably not updating the condition variable.

**"break and continue confuse me"**

`break` = exit entire loop. `continue` = skip to next check.

**"Why do I need loops? I can copy/paste code"**

You could, but:
1. Code gets huge
2. Hard to maintain
3. Can't repeat unknown times (until user quits)

Loops are essential.

---

## Real-World Uses

- **Game loops**: Run game until player quits
- **Input validation**: Keep asking until valid
- **Processing**: Handle each item in order
- **Counting**: Repeat for range of numbers
- **Summation**: Add up values
- **Search**: Find item matching criteria

---

## Summary

While loops let you repeat actions as long as a condition is true. This is how programs become powerful and dynamic.

Every loop needs:
1. Initialization (set up the variable)
2. Condition (check if should continue)
3. Update (change the variable)

Without proper updates, loops run forever.

Next: see while loops in action.
