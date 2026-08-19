# Hello World: Your First Program - Lecture

## Why This Matters

Before you learn anything about Python, you need to answer one question: **What actually happens when you run code?**

Most people think of programming like writing an email—you write something, you send it, and... something happens somewhere. But that's vague. We need to be precise.

This lesson answers that question by building the simplest possible program. By the end, you'll understand:
- What a program actually is
- What Python does with your code
- What it means to "run" something
- How to see the result

---

## The Mental Model: What Is a Program?

Imagine you're giving instructions to a very literal robot.

You say: "Make me a sandwich."

The robot has no idea what that means. It doesn't know what bread is, what peanut butter is, or how to assemble them.

So you need to give it **step-by-step instructions**:

```
1. Open the cupboard
2. Take out the bread
3. Open the jar of peanut butter
4. Get a knife
5. Spread peanut butter on the bread
6. Close the jar
7. Hand me the sandwich
```

The robot reads your instructions from top to bottom, one at a time, and does exactly what you say. No more, no less.

A **program** is exactly like this: a list of instructions written in a language the computer understands. The computer reads them from top to bottom and does exactly what you tell it to.

Python is the *language* we use to write those instructions so the computer understands them.

---

## The Mental Model: What Does Python Do?

Here's the key insight: **Python is a translator.**

You write code in English-like Python syntax. Python reads your code and translates it into instructions the computer's processor actually understands.

Here's the flow:

```
You write:  print("Hello, World!")
                    ↓
Python reads it and understands: "The user wants to display text on screen"
                    ↓
Python translates it into machine instructions
                    ↓
Your computer's processor executes those instructions
                    ↓
Text appears on your screen: Hello, World!
```

This happens in milliseconds. But it's important to understand that there are *three actors* here:
1. **You** (the programmer, writing code)
2. **Python** (the translator)
3. **The computer** (the executor)

Without Python, the computer wouldn't understand your English-like instructions. Without you, there would be no instructions. Without the computer, nothing would actually happen.

---

## The Mental Model: What Does `print()` Actually Do?

Before we write any code, let's understand what the word "print" really means in programming.

In everyday life, "print" means to put ink on paper. But in programming, `print()` means something different: **"send this text to the screen so I can see it."**

Think of it like shouting. You want to communicate something to the world, so you make noise: `print()` makes your program "shout" its message onto the screen.

When you write `print("Hello, World!")`, you're saying:
- "Python, I want to display something"
- "What I want to display is: Hello, World!"
- "Please send it to the screen"

Python does exactly that.

---

## The Mental Model: What Are Quotation Marks?

Here's something that confuses beginners: Why do we need the quotation marks?

```python
print("Hello, World!")  ← correct
print(Hello, World!)    ← wrong
```

The quotation marks tell Python: **"Everything inside these quotes is text. Treat it as a message, not as Python code."**

Without quotes, Python would think `Hello` and `World` are names of things you defined earlier. It would say "I don't know what `Hello` means" and crash.

With quotes, Python knows: "Oh, this is just text the user wants to display."

Think of it like a name tag:
- If you say: `"Alice"` — the computer understands this is the text "Alice"
- If you say: `Alice` — the computer looks for something called Alice in your program

The quotes tell the computer: "This is literally the text I want, not a reference to something else."

---

## The Syntax: Breaking It Down

Here is the entire program:

```python
print("Hello, World!")
```

That's it. One line.

Breaking it down piece by piece:

```
print          ← the action (a built-in Python tool)
(              ← open parentheses (giving the tool what it needs)
"Hello, World!" ← what you want printed (the text in quotes)
)              ← close parentheses (end of the instruction)
```

Here's what's happening:
1. You call the `print()` function (a built-in tool Python provides)
2. You give it one **argument**: the text `"Hello, World!"`
3. Python executes it
4. The text appears on your screen

---

## How Execution Works: Step By Step

When you run a Python program, here's what happens:

**Step 1: You save a file called `hello.py`**
- The `.py` extension tells your computer: "This is a Python file"

**Step 2: You run the file using Python**
- You open a terminal and type: `python3 hello.py`
- This tells your computer: "Python, please read the file called hello.py and execute it"

**Step 3: Python reads your code**
- Python opens the file
- It reads the first line: `print("Hello, World!")`

**Step 4: Python translates and executes**
- Python understands: "The user wants text displayed"
- Python sends a message to your screen: "Display this text"

**Step 5: You see the result**
- Your screen shows: `Hello, World!`

That entire process takes milliseconds. But each step happens in order, one after another.

---

## Key Concepts to Remember

1. **A program is step-by-step instructions** that run from top to bottom
2. **Python is a translator** between human-readable code and machine instructions
3. **`print()`** is a tool that displays text on your screen
4. **Quotation marks** tell Python "this is literal text, not a reference"
5. **Parentheses** tell Python "execute this action"

---

## Common Questions

**Q: Why is it called "Hello, World!"?**

A: Tradition. Every programmer writes this as their first program. It's a ritual. It proves your setup works and you understand the basics. Think of it as "Hello, I've entered the world of programming."

**Q: What if I write `print("Goodbye, World!")`?**

A: It works exactly the same way. Python doesn't care about the specific text. It just displays whatever you put in the quotes.

**Q: What if I forget the quotes?**

A: Python will crash with an error. The error will tell you that the first word is undefined. This happens because Python thinks you're referring to something called that name, not the literal text.

**Q: What if I forget the parentheses?**

A: Python will crash. `print` without parentheses is just referring to the function itself, not calling it. We'll talk more about functions later, but for now: parentheses mean "do this action."

**Q: Can I run multiple print statements?**

A: Yes. Each one will display on its own line. We'll see this in the examples.

---

## Summary: What You Now Understand

- A **program** is a list of step-by-step instructions
- **Python** is a translator between human-readable code and machine instructions
- **`print()`** is a tool that displays text on your screen
- **Quotation marks** tell Python "this is text, not code"
- **Running** a program means executing it line by line from top to bottom

You now have everything you need to understand the Hello World program.

Next: see it in action with real examples.
