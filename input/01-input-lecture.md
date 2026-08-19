# Input: Getting Information from Users - Lecture

## Why This Matters

So far, all your programs have hardcoded information—values you typed directly into the code.

```python
name = "Alice"
print(name)
```

But real programs need to *ask users* for information. Think about it:

- A login screen asks for your username and password
- A calculator asks for the numbers you want to add
- A to-do app asks you to type the task
- A game asks for your name before starting

The **`input()` function** is how programs ask users to provide information.

This is where programs become interactive. Instead of hardcoding everything, you ask users to give you the data, store it in variables, and use it.

---

## The Mental Model: What Is Input?

Think of your program like a form.

When you fill out a form online:
1. The form displays a question: "What is your name?"
2. You type your answer
3. The form stores your answer
4. The form uses your answer somehow (sends it, displays it, etc.)

A program with `input()` works the same way:

```
Program displays: "What is your name?"
                           ↓
You type: Alice
                           ↓
Program stores: Alice
                           ↓
Program uses it: Hello, Alice!
```

The `input()` function is step 1 and 2: **displaying a question and reading what the user types**.

---

## The Mental Model: How `input()` Works

Here's the basic syntax:

```python
answer = input("What is your name? ")
```

Breaking it down:

- `input()` — the function that asks the user for information
- `"What is your name? "` — the question displayed on screen
- `answer =` — stores what the user types in a variable

When this line runs, Python:
1. Displays the question: `What is your name? `
2. Waits for the user to type something
3. Waits for the user to press Enter
4. Takes what the user typed and stores it in the variable `answer`

The program pauses and waits. The user is in control.

---

## The Mental Model: Input Always Returns Text

This is critical: **`input()` always gives you text, even if the user types a number.**

```python
age = input("How old are you? ")
```

If the user types `25`, Python stores it as the text `"25"`, not the number `25`.

Why does this matter? Because text and numbers behave differently:

- Text `"25"` + text `"5"` = `"255"` (joined together)
- Number `25` + number `5` = `30` (added)

We'll learn how to convert text to numbers later. For now, just remember: `input()` always gives you text.

---

## The Mental Model: Program Flow with Input

Here's how a program with input flows:

```python
print("Hello!")
name = input("What is your name? ")
print("Nice to meet you, " + name)
```

**Execution:**

1. Print: `Hello!`
2. Display question: `What is your name? ` (and wait)
3. User types: `Alice` and presses Enter
4. Store `"Alice"` in variable `name`
5. Print: `Nice to meet you, ` combined with the value in `name`
6. Program ends

Notice: The program pauses at `input()` and waits for the user. The user controls when the program continues.

---

## The Mental Model: Prompts Are User-Friendly

The text inside `input()` is called a **prompt**. It's a message asking the user for something.

Good prompts:
- Tell the user what to enter
- Are clear and specific
- Often end with a space or colon for formatting

✓ Good prompts:
```python
input("What is your name? ")
input("Enter your age: ")
input("What is the capital of France? ")
```

✗ Unclear prompts:
```python
input("?")
input("Data: ")
input("gimme something")
```

A good prompt tells the user exactly what information you want.

---

## Key Concepts to Remember

1. **`input()` displays a question** and waits for the user to answer
2. **The user types** and presses Enter
3. **Python stores** what the user typed in a variable
4. **`input()` always returns text**, even if the user types numbers
5. **Your program pauses** and waits for the user
6. **Write clear prompts** so users know what to enter

---

## How Input and Variables Work Together

This is the real power: combining input with variables.

Before (hardcoded):
```python
name = "Alice"
print("Hello, " + name)
```

Now (interactive):
```python
name = input("What is your name? ")
print("Hello, " + name)
```

The only difference: instead of hardcoding the value, you *ask the user* for it. Everything else works exactly the same.

---

## What Happens Behind the Scenes

When the user types something into `input()`:

1. Python displays the prompt
2. Python waits (your program is paused)
3. The user's keyboard input appears on screen as they type
4. The user presses Enter
5. Python takes everything the user typed (the text)
6. Python stores it in the variable
7. Your program continues to the next line

This happens seamlessly, but it's important to understand: *your program waits*. If there's no user input, the program doesn't continue.

---

## Common Misconception: Input Doesn't Do Anything Special

Beginners sometimes think `input()` is magic. It's not.

`input()` is just:
- A display mechanism (shows a question)
- A pause mechanism (waits for the user)
- A retrieval mechanism (captures what was typed)
- A storage mechanism (puts it in a variable)

Once you have the text in a variable, `input()` is done. Everything else is just working with the variable normally.

---

## Summary: What You'll Learn Next

- How to use `input()` to ask users for information
- How to store user input in variables
- How to use the input data in your programs
- How input and variables work together to create interactive programs

This is the transition from static programs (same output every time) to dynamic programs (different output based on user input).

Next: see `input()` in action.
