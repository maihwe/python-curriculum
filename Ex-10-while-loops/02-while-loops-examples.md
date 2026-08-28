# While Loops: Examples & Demos

## Example 1: Simple While Loop - Counting

**Code:**
```python
count = 0

while count < 5:
    print(count)
    count += 1
```

**Execution flow:**

Line 1: `count = 0`

Line 3: Check: is `0 < 5`? → Yes, enter loop

Line 4: Print `0`

Line 5: `count = 1`

Back to line 3: Check: is `1 < 5`? → Yes, continue

(Repeats until count = 5)

**Output:**
```
0
1
2
3
4
```

**Key insight:** Loop repeats, condition checks each time, exits when false.

---

## Example 2: While Loop - Reverse Counting

**Code:**
```python
count = 5

while count > 0:
    print(count)
    count -= 1

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

**Key insight:** You can count down. Last line only runs after loop exits.

---

## Example 3: Input Validation with While Loop

**Code:**
```python
age = -1

while age < 0:
    age = int(input("Enter your age: "))
    if age < 0:
        print("Age must be positive")

print("Your age:", age)
```

**Program interaction:**
```
Enter your age: -5
Age must be positive
Enter your age: -1
Age must be positive
Enter your age: 25
Your age: 25
```

**Key insight:** Loop repeats until valid input received.

---

## Example 4: Using `break` to Exit Loop

**Code:**
```python
while True:
    name = input("Enter your name (or 'quit'): ")
    if name == "quit":
        print("Goodbye!")
        break
    print("Hello, " + name)

print("Loop exited")
```

**Program interaction:**
```
Enter your name (or 'quit'): Alice
Hello, Alice
Enter your name (or 'quit'): Bob
Hello, Bob
Enter your name (or 'quit'): quit
Goodbye!
Loop exited
```

**Key insight:** `break` exits loop immediately.

---

## Example 5: Using `continue` to Skip Iteration

**Code:**
```python
count = 0

while count < 6:
    count += 1
    if count == 3:
        continue
    print(count)
```

**Output:**
```
1
2
4
5
6
```

**Explanation:**

When `count == 3`, `continue` skips print and goes back to check condition.

**Key insight:** `continue` skips rest of loop, then checks condition again.

---

## Example 6: Accumulating Sum

**Code:**
```python
total = 0
count = 0

while count < 3:
    num = int(input("Enter a number: "))
    total += num
    count += 1

print("Sum:", total)
```

**Program interaction:**
```
Enter a number: 10
Enter a number: 20
Enter a number: 15
Sum: 45
```

**Key insight:** Loop accumulates values over multiple iterations.

---

## Example 7: While Loop with User Control

**Code:**
```python
print("Guess the number (1-10)")
secret = 5

while True:
    guess = int(input("Guess: "))
    if guess == secret:
        print("Correct!")
        break
    elif guess < secret:
        print("Too low")
    else:
        print("Too high")

print("Game over")
```

**Program interaction:**
```
Guess the number (1-10)
Guess: 7
Too high
Guess: 3
Too low
Guess: 5
Correct!
Game over
```

**Key insight:** Loop continues until user gets answer.

---

## Example 8: Password Entry with Validation

**Code:**
```python
correct_password = "secret123"
attempts = 0

while attempts < 3:
    password = input("Enter password: ")
    if password == correct_password:
        print("Access granted!")
        break
    else:
        attempts += 1
        print("Wrong password. Attempts remaining:", 3 - attempts)

if attempts == 3:
    print("Account locked")
```

**Program interaction:**
```
Enter password: wrong
Wrong password. Attempts remaining: 2
Enter password: try
Wrong password. Attempts remaining: 1
Enter password: fail
Wrong password. Attempts remaining: 0
Account locked
```

**Key insight:** Combine loop counter with conditional logic.

---

## Example 9: Menu System with Loop

**Code:**
```python
while True:
    print("\n--- Menu ---")
    print("1. Say hello")
    print("2. Say goodbye")
    print("3. Exit")
    choice = input("Choose (1-3): ")
    
    if choice == "1":
        print("Hello!")
    elif choice == "2":
        print("Goodbye!")
    elif choice == "3":
        print("Exiting...")
        break
    else:
        print("Invalid choice")
```

**Program interaction:**
```
--- Menu ---
1. Say hello
2. Say goodbye
3. Exit
Choose (1-3): 1
Hello!

--- Menu ---
1. Say hello
2. Say goodbye
3. Exit
Choose (1-3): 3
Exiting...
```

**Key insight:** Menu systems loop until user chooses exit.

---

## Example 10: While Loop - Multiplication Table

**Code:**
```python
num = 5
multiplier = 1

while multiplier <= 10:
    result = num * multiplier
    print(str(num) + " x " + str(multiplier) + " = " + str(result))
    multiplier += 1
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

**Key insight:** Use loops for repetitive calculations.

---

## Example 11: Running Total with User Input

**Code:**
```python
total = 0

while True:
    num = int(input("Enter a number (or 0 to quit): "))
    if num == 0:
        break
    total += num
    print("Running total:", total)

print("Final total:", total)
```

**Program interaction:**
```
Enter a number (or 0 to quit): 10
Running total: 10
Enter a number (or 0 to quit): 20
Running total: 30
Enter a number (or 0 to quit): 15
Running total: 45
Enter a number (or 0 to quit): 0
Final total: 45
```

**Key insight:** Accumulate until user signals to stop.

---

## Example 12: Countdown Timer

**Code:**
```python
seconds = 5

print("Starting countdown...")
while seconds > 0:
    print(seconds)
    seconds -= 1

print("Time's up!")
```

**Output:**
```
Starting countdown...
5
4
3
2
1
Time's up!
```

**Key insight:** Decrement to reach exit condition.

---

## Example 13: Infinite Loop with Break

**Code:**
```python
response = input("Continue? (yes/no): ")

while response.lower() == "yes":
    print("Continuing...")
    response = input("Continue? (yes/no): ")

print("Stopped")
```

**Program interaction:**
```
Continue? (yes/no): yes
Continuing...
Continue? (yes/no): yes
Continuing...
Continue? (yes/no): no
Stopped
```

**Key insight:** Update condition variable to eventually exit.

---

## Example 14: Skipping Even Numbers

**Code:**
```python
num = 1

while num <= 10:
    if num % 2 == 0:
        num += 1
        continue
    print("Odd:", num)
    num += 1
```

**Output:**
```
Odd: 1
Odd: 3
Odd: 5
Odd: 7
Odd: 9
```

**Key insight:** Use `continue` to skip certain iterations.

---

## Example 15: Real-World - Bank ATM Loop

**Code:**
```python
balance = 1000

while True:
    print("\nATM Menu")
    print("1. Check balance")
    print("2. Withdraw")
    print("3. Deposit")
    print("4. Exit")
    
    choice = input("Choose: ")
    
    if choice == "1":
        print("Balance: $" + str(balance))
    elif choice == "2":
        amount = int(input("Withdraw amount: $"))
        if amount <= balance:
            balance -= amount
            print("Withdrawn $" + str(amount))
        else:
            print("Insufficient funds")
    elif choice == "3":
        amount = int(input("Deposit amount: $"))
        balance += amount
        print("Deposited $" + str(amount))
    elif choice == "4":
        print("Thank you!")
        break
    else:
        print("Invalid choice")
```

**Key insight:** Real programs use loops for continuous operation.

---

## Summary of Examples

- While loops repeat code
- Update condition variable to avoid infinite loops
- `break` exits loop early
- `continue` skips to next iteration
- Use loops for validation, accumulation, menus
- Loops run until condition is false

Next: practice with exercises.
