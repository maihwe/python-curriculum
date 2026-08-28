# Functions: Reusable Code Blocks - Lecture

## Why This Matters

So far, when you need to repeat code, you copy/paste:

```python
# Check password multiple times
password1 = input("Enter password: ")
if password1 == "secret":
    print("Correct!")
else:
    print("Wrong!")

# Check password again (copy/paste)
password2 = input("Enter password: ")
if password2 == "secret":
    print("Correct!")
else:
    print("Wrong!")

# Check password again (copy/paste AGAIN)
password3 = input("Enter password: ")
if password3 == "secret":
    print("Correct!")
else:
    print("Wrong!")
```

This is terrible. Code duplication is a nightmare to maintain.

A **function** is a reusable block of code you write once, then use many times.

Functions are how real programs are built.

---

## The Mental Model: What Is a Function?

A function is like a **recipe**.

```
Recipe: "How to make cookies"
- You write it once
- Anyone can use it many times
- Same instructions each time
- Different ingredients each time
```

Code functions work the same way:

```python
def check_password(password):  # Write once
    if password == "secret":
        print("Correct!")
    else:
        print("Wrong!")

check_password("secret")      # Use many times
check_password("wrong")
check_password("another")
```

Write the function once. Use it as many times as you want.

---

## The Mental Model: Defining Functions

**Basic structure:**

```python
def function_name(parameter1, parameter2):
    # Code here
    return result
```

**Breaking it down:**

```
def           ← "I'm defining a function"
function_name ← Name you choose
(parameters)  ← Inputs the function accepts
:             ← Start of function body
[code]        ← What the function does
return        ← What the function outputs
```

---

## The Mental Model: Parameters and Arguments

**Parameters** = variables in function definition

```python
def greet(name):  # 'name' is a parameter
    print("Hello, " + name)
```

**Arguments** = values you pass when calling the function

```python
greet("Alice")  # "Alice" is an argument
greet("Bob")    # "Bob" is an argument
```

---

## The Mental Model: Return Values

Functions can **return** values back to the caller:

```python
def add(a, b):
    result = a + b
    return result

total = add(5, 3)
print(total)  # 8
```

Flow:
1. Call `add(5, 3)`
2. Function calculates `result = 8`
3. Function `return`s 8
4. Value 8 goes into `total`
5. Print 8

---

## The Mental Model: Scope

**Scope** = where variables exist

```python
x = 10  # Global scope (exists everywhere)

def my_function():
    y = 20  # Local scope (only inside function)
    print(y)  # Works: 20

my_function()
print(x)  # Works: 10 (global)
print(y)  # ERROR! y doesn't exist outside function
```

Variables inside functions are **local** - they only exist inside that function.

Variables outside are **global** - they exist everywhere.

---

## The Mental Model: Function Execution

When you call a function:

```python
def add(a, b):
    result = a + b
    return result

total = add(5, 3)
```

Execution flow:

```
1. Call add(5, 3)
2. a = 5, b = 3 (parameters set)
3. result = 5 + 3 = 8
4. return 8
5. Function stops
6. total = 8
7. Continue main program
```

The function runs, returns a value, then stops.

---

## Key Concepts to Remember

1. **Functions are reusable code blocks**
2. **Define once, call many times**
3. **Parameters = inputs**
4. **Arguments = values you pass**
5. **Return = output value**
6. **Local scope = inside function**
7. **Global scope = outside function**
8. **Functions make code DRY** (Don't Repeat Yourself)
9. **Functions make code readable**
10. **Functions make code maintainable**

---

## Real-World Uses

**Validation functions:**
```python
def validate_email(email):
    if "@" in email:
        return True
    return False
```

**Calculation functions:**
```python
def calculate_discount(price, percentage):
    discount = price * (percentage / 100)
    return discount
```

**Processing functions:**
```python
def clean_text(text):
    return text.strip().lower()
```

**Conversion functions:**
```python
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32
```

---

## Common Misconceptions

**"Functions are complicated"**

They're just code blocks that accept inputs and return outputs. Simple.

**"I should write everything in one function"**

No. Break code into small, single-purpose functions.

**"Local variables are confusing"**

Variables in functions stay in functions. Global variables work everywhere. Simple rule.

**"I must use return"**

Functions can work without return, but return is how you get data back out.

---

## Best Practices

**1. Give functions clear names**
```python
✅ calculate_total
❌ calc_tot
```

**2. One purpose per function**
```python
✅ validate_email, calculate_tax, send_email
❌ do_everything_for_user
```

**3. Keep functions small**
```python
✅ 5-20 lines per function
❌ 100+ lines per function
```

**4. Use meaningful parameter names**
```python
✅ def add(first_number, second_number):
❌ def add(a, b):
```

---

## Summary

Functions are **reusable code blocks** that make programs:
- **Cleaner** (no copy/paste)
- **Readable** (clear intent)
- **Maintainable** (change once, fixes everywhere)
- **Testable** (test each function)

Write the function once. Use it as many times as needed.

Next: see functions in action.
