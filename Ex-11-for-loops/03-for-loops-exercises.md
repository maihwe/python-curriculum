# For Loops: Exercises & Practice

## Exercise 1: Count 1 to 10

Create a program that counts from 1 to 10 using a for loop.

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
1. Create a file called `count_1_to_10.py`
2. Use `for num in range(1, 11):`
3. Print each number
4. Run it

**Hint:** `range(1, 11)` gives 1-10.

---

## Exercise 2: Even Numbers 0 to 20

Create a program that prints only even numbers from 0 to 20.

**Expected output:**
```
0
2
4
6
8
10
12
14
16
18
20
```

**What to do:**
1. Create a file called `even_numbers.py`
2. Use `for num in range(0, 21, 2):`
3. Print each number
4. Run it

**Hint:** Step by 2 to get every other number.

---

## Exercise 3: Countdown 10 to 1

Create a program that counts down from 10 to 1.

**Expected output:**
```
10
9
8
7
6
5
4
3
2
1
```

**What to do:**
1. Create a file called `countdown_10.py`
2. Use `for num in range(10, 0, -1):`
3. Print each number
4. Run it

**Hint:** Negative step counts down.

---

## Exercise 4: Multiplication Table

Create a program that prints the multiplication table for 7.

**Expected output:**
```
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
...
7 x 10 = 70
```

**What to do:**
1. Create a file called `mult_table_7.py`
2. Set num to 7
3. Use `for i in range(1, 11):`
4. Calculate and print 7 * i
5. Run it

**Hint:** Loop prints 10 lines.

---

## Exercise 5: Sum 1 to 100

Create a program that calculates the sum of numbers 1 to 100.

**Expected output:**
```
Sum: 5050
```

**What to do:**
1. Create a file called `sum_1_to_100.py`
2. Initialize total to 0
3. Use `for num in range(1, 101):`
4. Add each number to total
5. Print the sum
6. Run it

**Hint:** 1+2+3+...+100 = 5050.

---

## Exercise 6: Count Odd Numbers 1-50

Create a program that counts how many odd numbers are between 1 and 50.

**Expected output:**
```
Odd numbers: 25
```

**What to do:**
1. Create a file called `count_odds.py`
2. Initialize count to 0
3. Use `for num in range(1, 51):`
4. If odd (num % 2 != 0), increment count
5. Print the count
6. Run it

**Hint:** Odd numbers: remainder is 1 when divided by 2.

---

## Exercise 7: Break Early

Create a program that prints numbers 1-10 but stops at 5.

**Expected output:**
```
1
2
3
4
5
```

**What to do:**
1. Create a file called `break_early.py`
2. Use `for num in range(1, 11):`
3. Print the number
4. If num == 5, break
5. Run it

**Hint:** `break` stops the loop.

---

## Exercise 8: Skip Even Numbers

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
1. Create a file called `skip_evens.py`
2. Use `for num in range(1, 11):`
3. If even, continue
4. Otherwise, print
5. Run it

**Hint:** Use `continue` to skip.

---

## Exercise 9: Print a Square Pattern

Create a program that prints a 5x5 square of asterisks.

**Expected output:**
```
*****
*****
*****
*****
*****
```

**What to do:**
1. Create a file called `square_pattern.py`
2. Outer loop: `for i in range(5):`
3. Inner loop: `for j in range(5):`
4. Print "*" without newline (use `end=""`)
5. After inner loop, print newline
6. Run it

**Hint:** Nested loops create 2D patterns.

---

## Exercise 10: Print a Triangle Pattern

Create a program that prints a triangle.

**Expected output:**
```
*
**
***
****
*****
```

**What to do:**
1. Create a file called `triangle_pattern.py`
2. Outer loop: `for i in range(1, 6):`
3. Inner loop: `for j in range(i):`
4. Print "*" without newline
5. After inner loop, print newline
6. Run it

**Hint:** Inner loop runs i times.

---

## Exercise 11: Factorial Calculation

Create a program that calculates 5! (5 factorial = 5×4×3×2×1).

**Expected output:**
```
5! = 120
```

**What to do:**
1. Create a file called `factorial.py`
2. Set n to 5, result to 1
3. Use `for i in range(1, n+1):`
4. Multiply result by i
5. Print the result
6. Run it

**Hint:** 5×4×3×2×1 = 120.

---

## Exercise 12: Average of Numbers

Create a program that calculates average of numbers 1-10.

**Expected output:**
```
Average: 5.5
```

**What to do:**
1. Create a file called `average.py`
2. Initialize total to 0
3. Use `for num in range(1, 11):`
4. Add to total
5. Calculate average = total / 10
6. Print average
7. Run it

**Hint:** Average = sum / count.

---

## Exercise 13: Powers of 2

Create a program that prints first 10 powers of 2.

**Expected output:**
```
2^1 = 2
2^2 = 4
2^3 = 8
2^4 = 16
2^5 = 32
2^6 = 64
2^7 = 128
2^8 = 256
2^9 = 512
2^10 = 1024
```

**What to do:**
1. Create a file called `powers_of_2.py`
2. Use `for i in range(1, 11):`
3. Calculate 2^i (use ** for power)
4. Print in format shown
5. Run it

**Hint:** Use `2**i` for 2 to the power i.

---

## Exercise 14: Character Count

Create a program that counts characters in a string using a loop.

**Program interaction:**
```
Enter a word: hello
Character count: 5
```

**What to do:**
1. Create a file called `char_count.py`
2. Get word from user
3. Initialize count to 0
4. Use `for char in word:`
5. Increment count for each character
6. Print count
7. Run it

**Hint:** Loop over each character in string.

---

## Exercise 15: Nested Loop - Multiplication Grid

Create a program that prints a multiplication grid (1-5 by 1-5).

**Expected output:**
```
1 2 3 4 5
2 4 6 8 10
3 6 9 12 15
4 8 12 16 20
5 10 15 20 25
```

**What to do:**
1. Create a file called `mult_grid.py`
2. Outer loop: `for i in range(1, 6):`
3. Inner loop: `for j in range(1, 6):`
4. Print i*j without newline (use `end=" "`)
5. After inner loop, print newline
6. Run it

**Hint:** Each cell is i × j.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Does loop run correct number of times?
- ✓ Does range() give expected values?
- ✓ Does output match expected?
- ✓ Do I understand `range()`?

---

## Important Observations

**About For Loops:**
- Repeat known number of times
- `range()` creates number sequences
- Loop variable updates automatically
- `break` exits early
- `continue` skips to next
- Nested loops create patterns

---

## Completed!

You've now learned:
1. Hello World
2. Variables
3. Input
4. Strings
5. Type Conversion
6. Arithmetic
7. Comparisons
8. If/Else
9. Logical Operators
10. While Loops
11. For Loops

**You now have the foundational building blocks of programming!**

With these 11 topics, you can write:
- Input/output programs
- Decision-making programs
- Repeating programs
- Mathematical programs
- Games and simulations
- Data validation
- Menu systems

Next topic (when ready):

**Topic 12: Lists** — Store and process collections of data

Lists are essential for any real program. They let you work with groups of items.

Great progress! 🎉
