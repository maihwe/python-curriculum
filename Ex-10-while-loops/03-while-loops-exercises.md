# While Loops: Exercises & Practice

## Exercise 1: Simple Countdown

Create a program that counts down from 5 to 1.

**Expected output:**
```
5
4
3
2
1
Blastoff!
```

**What to do:**
1. Create a file called `countdown.py`
2. Set count to 5
3. While count > 0, print and decrement
4. Print "Blastoff!" after loop
5. Run it

**Hint:** Use `count -= 1` to decrement.

---

## Exercise 2: Count to 10

Create a program that counts from 1 to 10.

**Expected output:**
```
1
2
3
4
5
6
7
8
9
10
```

**What to do:**
1. Create a file called `count_to_10.py`
2. Set count to 1
3. While count <= 10, print and increment
4. Run it

**Hint:** Use `count += 1` to increment.

---

## Exercise 3: Input Validation

Create a program that asks for age until valid (must be >= 0).

**Program interaction:**
```
Enter your age: -5
Age must be positive!
Enter your age: 25
Your age is 25
```

**What to do:**
1. Create a file called `age_validation.py`
2. Set age to -1 initially
3. While age < 0, ask for input
4. Print accepted age
5. Run it and test with negative and positive numbers

**Hint:** Loop exits when valid input received.

---

## Exercise 4: Using `break`

Create a program that repeats until user enters "quit".

**Program interaction:**
```
Say something (or 'quit' to exit): hello
You said: hello
Say something (or 'quit' to exit): goodbye
You said: goodbye
Say something (or 'quit' to exit): quit
Done!
```

**What to do:**
1. Create a file called `break_example.py`
2. Use `while True:`
3. Get input from user
4. If input is "quit", break
5. Otherwise, print the input

**Hint:** Use `if ... break` to exit.

---

## Exercise 5: Accumulating Sum

Create a program that sums numbers entered by user (stop when user enters 0).

**Program interaction:**
```
Enter a number (0 to stop): 10
Running total: 10
Enter a number (0 to stop): 20
Running total: 30
Enter a number (0 to stop): 15
Running total: 45
Enter a number (0 to stop): 0
Final sum: 45
```

**What to do:**
1. Create a file called `sum_accumulator.py`
2. Initialize total to 0
3. While user doesn't enter 0:
   - Get number
   - Add to total
   - Print running total
4. Print final sum
5. Run it

**Hint:** Add to total inside loop.

---

## Exercise 6: Password Retry

Create a program that allows 3 password attempts.

**Program interaction:**
```
Enter password: wrong
Wrong! Attempts remaining: 2
Enter password: try
Wrong! Attempts remaining: 1
Enter password: fail
Wrong! Attempts remaining: 0
Account locked
```

(Or if correct:)
```
Enter password: correct
Access granted!
```

**What to do:**
1. Create a file called `password_retry.py`
2. Set attempts to 3
3. While attempts > 0, ask for password
4. If correct, print access granted and break
5. If wrong, decrement attempts
6. If attempts reach 0, print locked

**Hint:** Track attempts counter.

---

## Exercise 7: Odd Numbers Loop

Create a program that prints odd numbers from 1 to 15.

**Expected output:**
```
1
3
5
7
9
11
13
15
```

**What to do:**
1. Create a file called `odd_numbers.py`
2. Set num to 1
3. While num <= 15:
   - Print num
   - Add 2 (to get next odd)
4. Run it

**Hint:** Increment by 2 to get every other number.

---

## Exercise 8: Even Numbers with `continue`

Create a program that prints 1-10 but skips even numbers.

**Expected output:**
```
1
3
5
7
9
```

**What to do:**
1. Create a file called `skip_even.py`
2. Set num to 0
3. While num < 10:
   - Increment num
   - If even, continue
   - Otherwise, print
4. Run it

**Hint:** Use `continue` to skip even numbers.

---

## Exercise 9: Multiplication Practice Quiz

Create a program that asks multiplication questions until user gets 3 right.

**Program interaction:**
```
What is 3 x 4? 12
Correct! Score: 1/3
What is 5 x 6? 20
Wrong! Score: 1/3
What is 7 x 2? 14
Correct! Score: 2/3
What is 8 x 9? 72
Correct! Score: 3/3
Quiz complete!
```

**What to do:**
1. Create a file called `multiplication_quiz.py`
2. Track score (start at 0)
3. While score < 3:
   - Ask multiplication question
   - Check if correct
   - Update score
4. Print done when 3 correct
5. Run it

**Hint:** Increment score only if correct.

---

## Exercise 10: Menu System

Create a program with a menu that loops until user exits.

**Program interaction:**
```
--- Menu ---
1. Greet
2. Calculate 2+2
3. Exit
Choose: 1
Hello!

--- Menu ---
1. Greet
2. Calculate 2+2
3. Exit
Choose: 2
2 + 2 = 4

--- Menu ---
1. Greet
2. Calculate 2+2
3. Exit
Choose: 3
Goodbye!
```

**What to do:**
1. Create a file called `menu_system.py`
2. Use `while True:`
3. Display menu
4. Get choice
5. Perform action
6. If exit, break
7. Loop back to menu

**Hint:** Each iteration shows menu again.

---

## Exercise 11: Running Until Condition Met

Create a program that asks for a number between 1-100.

**Program interaction:**
```
Enter a number between 1-100: 150
Out of range!
Enter a number between 1-100: 0
Out of range!
Enter a number between 1-100: 50
Valid! You entered: 50
```

**What to do:**
1. Create a file called `range_validator.py`
2. Set num to 0
3. While num is not in range:
   - Ask for input
   - Check if 1-100
4. Print valid number
5. Run it

**Hint:** Loop exits when valid.

---

## Exercise 12: Guess the Number Game

Create a guessing game that runs until correct (with hints).

**Program interaction:**
```
I'm thinking of a number (1-10)
Guess: 5
Too high
Guess: 3
Too low
Guess: 4
Correct! You got it in 3 tries!
```

**What to do:**
1. Create a file called `guess_game.py`
2. Set secret number
3. While guess != secret:
   - Get guess
   - Give hint (high/low)
   - Count attempts
4. Print success message with attempts
5. Run it

**Hint:** Track attempts counter.

---

## Exercise 13: Savings Goal

Create a program that calculates when savings goal is reached.

**Program interaction:**
```
Starting balance: $0
Monthly savings: $100
Goal: $1000
Month 1: $100
Month 2: $200
...
Month 10: $1000
Goal reached in 10 months!
```

**What to do:**
1. Create a file called `savings_goal.py`
2. Get starting balance, monthly savings, goal
3. While balance < goal:
   - Add monthly savings
   - Increment month
   - Print current balance
4. Print how many months to reach goal
5. Run it

**Hint:** Loop until goal reached.

---

## Exercise 14: Input Until Valid Type

Create a program that keeps asking until user enters valid integer.

**Program interaction:**
```
Enter an integer: hello
That's not an integer!
Enter an integer: 3.14
That's not an integer!
Enter an integer: 42
You entered: 42
```

**What to do:**
1. Create a file called `int_validator.py`
2. Use `while True:`
3. Try to convert to int
4. If successful, break
5. If error, ask again
6. Print the integer

**Hint:** This is more advanced—handle conversion errors.

---

## Exercise 15: Real-World - Simple ATM

Create a program that simulates ATM with balance.

**Program interaction:**
```
ATM Menu
1. Check balance
2. Withdraw
3. Deposit
4. Exit
Choose: 1
Balance: $1000

ATM Menu
1. Check balance
2. Withdraw
3. Deposit
4. Exit
Choose: 2
Withdraw amount: 200
New balance: $800

ATM Menu
1. Check balance
2. Withdraw
3. Deposit
4. Exit
Choose: 4
Thank you!
```

**What to do:**
1. Create a file called `simple_atm.py`
2. Set starting balance
3. Use `while True:` for menu loop
4. Implement each option
5. Break when user chooses exit
6. Run it

**Hint:** Menu should repeat until exit.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Does loop repeat correctly?
- ✓ Does condition eventually become false?
- ✓ Are updates happening inside loop?
- ✓ Can user exit the loop?

---

## Important Observations

**About While Loops:**
- Condition checked before each iteration
- Must update condition variable
- `break` exits immediately
- `continue` skips to next check
- Useful for validation, menus, counting

---

## Next Steps

Once you've completed these exercises:

1. You understand loop repetition
2. You can validate input with loops
3. You can create menus
4. You can accumulate values
5. You understand `break` and `continue`

You're ready for Topic 11: **For Loops**

For loops are for when you know how many times to repeat. While loops are for when you don't.

Next lesson: controlled repetition!
