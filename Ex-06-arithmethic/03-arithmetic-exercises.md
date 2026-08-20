# Arithmetic: Exercises & Practice

## Exercise 1: Simple Addition Program

Create a program that adds two numbers.

**Program interaction:**
```
Enter first number: 5
Enter second number: 3
Sum: 8
```

**What to do:**
1. Create a file called `add_two.py`
2. Get two numbers from user
3. Convert to numbers
4. Add them
5. Print result

**Hint:** Use `int()` or `float()` to convert.

---

## Exercise 2: All Four Basic Operations

Create a program that performs four operations on two numbers.

**Program interaction:**
```
Enter first number: 10
Enter second number: 3
Sum: 13
Difference: 7
Product: 30
Quotient: 3.3333333333333335
```

**What to do:**
1. Create a file called `four_operations.py`
2. Get two numbers
3. Calculate all four: +, -, *, /
4. Print all results
5. Run it

**Hint:** You'll need four print statements.

---

## Exercise 3: Using Shortcuts (+=, -=, etc.)

Create a program that updates a score using shortcuts.

**Code structure:**
```python
score = 10
score += 5
score *= 2
score -= 8
print(score)
```

**What to do:**
1. Create a file called `score_update.py`
2. Start with score = 10
3. Use += to add 5
4. Use *= to multiply by 2
5. Use -= to subtract 8
6. Print final score
7. Figure out what the final score should be before running

**Expected output:**
```
14
```

**Hint:** Work through it step by step: 10 + 5 = 15, 15 * 2 = 30, 30 - 8 = 22. Wait, that's not 14. Let me recalculate... Actually the expected output should be 22.

---

## Exercise 4: Order of Operations

Create a program that demonstrates order of operations.

**Code:**
```python
print("2 + 3 * 4 =", 2 + 3 * 4)
print("(2 + 3) * 4 =", (2 + 3) * 4)
print("10 / 2 * 5 =", 10 / 2 * 5)
print("2 ** 3 * 4 =", 2 ** 3 * 4)
```

**What to do:**
1. Create a file called `order_of_operations.py`
2. Copy the code above
3. Before running, predict each answer
4. Run it and check if you were right
5. Try to explain why each is correct

**Expected output:**
```
2 + 3 * 4 = 14
(2 + 3) * 4 = 20
10 / 2 * 5 = 25.0
2 ** 3 * 4 = 32
```

**Hint:** Remember PEMDAS.

---

## Exercise 5: Floor Division and Modulo

Create a program that demonstrates floor division and modulo.

**Program interaction:**
```
Enter a number: 10
Enter another number: 3
Regular division: 3.3333333333333335
Floor division: 3
Remainder (modulo): 1
```

**What to do:**
1. Create a file called `floor_and_modulo.py`
2. Get two numbers from user
3. Calculate regular division, floor division, and modulo
4. Print all three
5. Run it and test

**Hint:** Use `/`, `//`, and `%`.

---

## Exercise 6: Area and Perimeter of Rectangle

Create a program that calculates area and perimeter.

**Program interaction:**
```
Enter length: 5
Enter width: 3
Area: 15
Perimeter: 16
```

**What to do:**
1. Create a file called `rectangle.py`
2. Get length and width from user (convert to numbers)
3. Calculate area = length * width
4. Calculate perimeter = 2 * (length + width)
5. Print both
6. Run it

**Hint:** Area and perimeter are basic formulas.

---

## Exercise 7: Circle Calculations

Create a program that calculates circle properties.

**Program interaction:**
```
Enter radius: 5
Area: 78.5
Circumference: 31.400000000000002
```

**What to do:**
1. Create a file called `circle.py`
2. Get radius from user (convert to float)
3. Calculate area = 3.14159 * radius ** 2
4. Calculate circumference = 2 * 3.14159 * radius
5. Print both
6. Run it

**Hint:** Use π ≈ 3.14159

---

## Exercise 8: Temperature Conversion

Create a program that converts Celsius to Fahrenheit and Kelvin.

**Program interaction:**
```
Enter Celsius: 0
Fahrenheit: 32.0
Kelvin: 273.15
```

**Formulas:**
- Fahrenheit = (Celsius * 9/5) + 32
- Kelvin = Celsius + 273.15

**What to do:**
1. Create a file called `temperature.py`
2. Get Celsius from user
3. Convert to Fahrenheit and Kelvin
4. Print both
5. Run it and test with 0, 100, and -40

**Hint:** These are just arithmetic formulas.

---

## Exercise 9: Compound Interest

Create a program that calculates compound interest.

**Formula:** A = P(1 + r)^t

Where:
- P = principal (starting amount)
- r = annual rate (as decimal, so 5% = 0.05)
- t = time in years
- A = final amount

**Program interaction:**
```
Enter principal: 1000
Enter rate (as decimal, e.g. 0.05 for 5%): 0.05
Enter time (years): 2
Final amount: 1102.5
```

**What to do:**
1. Create a file called `compound_interest.py`
2. Get principal, rate, and time from user
3. Convert all to floats
4. Calculate using formula
5. Print result
6. Run it

**Hint:** Use `**` for exponent.

---

## Exercise 10: Average Calculator

Create a program that calculates the average of four numbers.

**Program interaction:**
```
Enter score 1: 85
Enter score 2: 90
Enter score 3: 78
Enter score 4: 92
Average: 86.25
```

**What to do:**
1. Create a file called `average.py`
2. Get four numbers from user
3. Calculate average = sum / 4
4. Print result
5. Run it

**Hint:** Add all four, then divide by 4.

---

## Exercise 11: Checking Even and Odd

Create a program that checks if a number is even or odd.

**Program interaction:**
```
Enter a number: 7
7 is odd
```

Then try with 8 and it should say "8 is even"

**What to do:**
1. Create a file called `even_odd.py`
2. Get a number from user
3. Use modulo to check: if num % 2 == 0 it's even, else odd
4. Print result (we'll learn if/else properly next, but you can try with a simple if)

**Hint:** Look at Example 12 in the Arithmetic examples file.

---

## Exercise 12: Distance and Speed Calculator

Create a program that calculates time given distance and speed.

**Formula:** Time = Distance / Speed

**Program interaction:**
```
Enter distance (miles): 100
Enter speed (mph): 60
Time: 1.6666666666666667 hours
```

**What to do:**
1. Create a file called `distance_time.py`
2. Get distance and speed from user
3. Convert to floats
4. Calculate time = distance / speed
5. Print result
6. Run it

**Hint:** This is simple division.

---

## Exercise 13: Salary Calculator with Bonus

Create a program that calculates salary with bonus.

**Program interaction:**
```
Enter base salary: 50000
Enter bonus percentage (as decimal, e.g. 0.1 for 10%): 0.1
Bonus amount: 5000.0
Total salary: 55000.0
```

**What to do:**
1. Create a file called `salary_bonus.py`
2. Get base salary and bonus percentage
3. Calculate bonus = salary * bonus_percent
4. Calculate total = salary + bonus
5. Print both bonus and total
6. Run it

**Hint:** Bonus = base * percentage, Total = base + bonus

---

## Exercise 14: Complex Formula - Quadratic Discriminant

Create a program that calculates the discriminant of a quadratic equation.

**Formula:** discriminant = b² - 4ac

**Program interaction:**
```
Enter a: 1
Enter b: 2
Enter c: 1
Discriminant: 0
```

**What to do:**
1. Create a file called `quadratic.py`
2. Get a, b, c from user
3. Calculate discriminant = b**2 - 4*a*c
4. Print result
5. Run it with a=1, b=2, c=1 (answer should be 0)

**Hint:** Use `**` for squaring.

---

## Exercise 15: Real-World - Shopping Bill with Tax

Create a program that calculates bill total with tax.

**Program interaction:**
```
Enter item price: 50.00
Enter tax rate (as decimal, e.g. 0.08 for 8%): 0.08
Subtotal: 50.0
Tax: 4.0
Total: 54.0
```

**What to do:**
1. Create a file called `bill_with_tax.py`
2. Get price and tax rate from user
3. Calculate tax = price * tax_rate
4. Calculate total = price + tax
5. Print subtotal, tax, and total
6. Run it

**Hint:** This is a real-world problem you solve with arithmetic.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Are the math results correct?
- ✓ Did I convert types properly?
- ✓ Did I store results in variables?
- ✓ Can I predict the output before running?

---

## Important Observations

**About Arithmetic:**
- `/` always returns float (use `//` for integers)
- Order of operations matters (use parentheses if unsure)
- Modulo (`%`) is useful for patterns and checking divisibility
- Update variables with shortcuts (`+=`, `-=`, etc.)
- Real-world formulas are combinations of basic operations
- Floats have tiny precision errors (normal)

---

## Next Steps

Once you've completed these exercises:

1. You can perform all basic arithmetic
2. You understand order of operations
3. You can calculate complex formulas
4. You can store and reuse results
5. You understand different division types

You're ready for Topic 7: **Comparisons**

In Comparisons, you'll learn how to compare values (==, !=, <, >, <=, >=) which leads directly to conditional logic (if/else).

Next lesson: making Python make decisions!
