# Functions: Examples & Demos

## Example 1: Simple Function

**Code:**
```python
def greet():
    print("Hello, World!")

greet()
greet()
greet()
```

**Output:**
```
Hello, World!
Hello, World!
Hello, World!
```

**Key insight:** Define once, call multiple times.

---

## Example 2: Function with Parameter

**Code:**
```python
def greet(name):
    print("Hello, " + name + "!")

greet("Alice")
greet("Bob")
greet("Charlie")
```

**Output:**
```
Hello, Alice!
Hello, Bob!
Hello, Charlie!
```

**Key insight:** Parameters let you pass different values.

---

## Example 3: Function with Multiple Parameters

**Code:**
```python
def add(a, b):
    result = a + b
    print(str(a) + " + " + str(b) + " = " + str(result))

add(5, 3)
add(10, 20)
add(100, 1)
```

**Output:**
```
5 + 3 = 8
10 + 20 = 30
100 + 1 = 101
```

**Key insight:** Multiple parameters work the same as one.

---

## Example 4: Function with Return

**Code:**
```python
def add(a, b):
    return a + b

result1 = add(5, 3)
result2 = add(10, 20)

print("Result 1:", result1)
print("Result 2:", result2)
print("Sum:", result1 + result2)
```

**Output:**
```
Result 1: 8
Result 2: 30
Sum: 38
```

**Key insight:** Return sends value back to caller.

---

## Example 5: Function vs No Return

**Code:**
```python
def add_no_return(a, b):
    print(a + b)

def add_with_return(a, b):
    return a + b

# No return
add_no_return(5, 3)

# With return
result = add_with_return(5, 3)
print("Result:", result)
```

**Output:**
```
8
Result: 8
```

**Key insight:** Return lets you store and use the value.

---

## Example 6: Execution Flow

**Code:**
```python
print("Before function definition")

def multiply(a, b):
    print("Inside function: multiplying")
    return a * b

print("After function definition, before call")

result = multiply(4, 5)

print("After function call")
print("Result:", result)
```

**Output:**
```
Before function definition
After function definition, before call
Inside function: multiplying
After function call
Result: 20
```

**Key insight:** Function body only runs when called, not when defined.

---

## Example 7: Local Variables

**Code:**
```python
x = 100  # Global

def my_function():
    x = 5  # Local
    print("Inside function, x =", x)

print("Before function, x =", x)
my_function()
print("After function, x =", x)
```

**Output:**
```
Before function, x = 100
Inside function, x = 5
After function, x = 100
```

**Key insight:** Local variables only exist inside function.

---

## Example 8: Validation Function

**Code:**
```python
def is_adult(age):
    if age >= 18:
        return True
    else:
        return False

print("Is 25 an adult?", is_adult(25))
print("Is 15 an adult?", is_adult(15))
print("Is 18 an adult?", is_adult(18))
```

**Output:**
```
Is 25 an adult? True
Is 15 an adult? False
Is 18 an adult? True
```

**Key insight:** Functions can return True/False.

---

## Example 9: Conversion Function

**Code:**
```python
def celsius_to_fahrenheit(celsius):
    fahrenheit = (celsius * 9/5) + 32
    return fahrenheit

c1 = celsius_to_fahrenheit(0)
c2 = celsius_to_fahrenheit(100)
c3 = celsius_to_fahrenheit(-40)

print("0°C =", c1, "°F")
print("100°C =", c2, "°F")
print("-40°C =", c3, "°F")
```

**Output:**
```
0°C = 32.0 °F
100°C = 212.0 °F
-40°C = -40.0 °F
```

**Key insight:** Functions can do calculations and return results.

---

## Example 10: String Processing Function

**Code:**
```python
def clean_text(text):
    return text.strip().lower()

messy1 = "  HELLO  "
messy2 = "  WoRlD  "

clean1 = clean_text(messy1)
clean2 = clean_text(messy2)

print("Original 1:", messy1)
print("Clean 1:", clean1)
print("Original 2:", messy2)
print("Clean 2:", clean2)
```

**Output:**
```
Original 1:   HELLO  
Clean 1: hello
Original 2:   WoRlD  
Clean 2: world
```

**Key insight:** Functions can process and transform data.

---

## Example 11: Function Calling Function

**Code:**
```python
def add(a, b):
    return a + b

def multiply_and_add(x, y, z):
    sum_xy = add(x, y)
    result = sum_xy * z
    return result

result = multiply_and_add(2, 3, 4)
print("(2 + 3) * 4 =", result)
```

**Output:**
```
(2 + 3) * 4 = 20
```

**Key insight:** Functions can call other functions.

---

## Example 12: List Processing Function

**Code:**
```python
def sum_list(numbers):
    total = 0
    for num in numbers:
        total += num
    return total

list1 = [1, 2, 3, 4, 5]
list2 = [10, 20, 30]

sum1 = sum_list(list1)
sum2 = sum_list(list2)

print("Sum of", list1, "=", sum1)
print("Sum of", list2, "=", sum2)
```

**Output:**
```
Sum of [1, 2, 3, 4, 5] = 15
Sum of [10, 20, 30] = 60
```

**Key insight:** Functions work with collections.

---

## Example 13: Dictionary Processing Function

**Code:**
```python
def get_grade_letter(percentage):
    if percentage >= 90:
        return "A"
    elif percentage >= 80:
        return "B"
    elif percentage >= 70:
        return "C"
    else:
        return "F"

scores = {"Alice": 95, "Bob": 82, "Charlie": 78}

for name, score in scores.items():
    grade = get_grade_letter(score)
    print(name + ": " + str(score) + "% = " + grade)
```

**Output:**
```
Alice: 95% = A
Bob: 82% = B
Charlie: 78% = C
```

**Key insight:** Functions work great with dictionaries.

---

## Example 14: Decision Function

**Code:**
```python
def classify_age(age):
    if age < 13:
        return "Child"
    elif age < 18:
        return "Teen"
    elif age < 65:
        return "Adult"
    else:
        return "Senior"

ages = [5, 15, 25, 70]

for age in ages:
    category = classify_age(age)
    print("Age", age, "=", category)
```

**Output:**
```
Age 5 = Child
Age 15 = Teen
Age 25 = Adult
Age 70 = Senior
```

**Key insight:** Functions with complex logic.

---

## Example 15: Real-World - Calculator Functions

**Code:**
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error: Division by zero"
    return a / b

print("5 + 3 =", add(5, 3))
print("5 - 3 =", subtract(5, 3))
print("5 * 3 =", multiply(5, 3))
print("5 / 3 =", divide(5, 3))
print("5 / 0 =", divide(5, 0))
```

**Output:**
```
5 + 3 = 8
5 - 3 = 2
5 * 3 = 15
5 / 3 = 1.6666666666666667
5 / 0 = Error: Division by zero
```

**Key insight:** Build a library of useful functions.

---

## Summary of Examples

- Simple functions
- Functions with parameters
- Functions with returns
- Local variables
- Validation functions
- Conversion functions
- Processing functions
- Functions calling functions
- Working with collections
- Working with dictionaries
- Complex logic in functions
- Real-world calculators

Next: practice with exercises.
