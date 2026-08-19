# Input: Exercises & Practice

## Exercise 1: Simple Input and Output

Create a program that asks for your favorite food and prints it back to you.

**Program interaction example:**
```
What is your favorite food? Pizza
Pizza
```

**What to do:**
1. Create a file called `favorite_food.py`
2. Use `input()` to ask for favorite food
3. Store it in a variable
4. Print it
5. Run it and test with different foods

**Hint:** Use a clear prompt in `input()`.

---

## Exercise 2: Multiple Inputs

Create a program that asks for:
- Your name
- Your age
- Your hobby

Print each one on its own line.

**Program interaction example:**
```
What is your name? Alice
How old are you? 28
What is your hobby? Reading
Alice
28
Reading
```

**What to do:**
1. Create a file called `three_inputs.py`
2. Create three `input()` statements
3. Store each in a different variable
4. Print each variable on its own line

**Hint:** Each `input()` will pause and wait for the user.

---

## Exercise 3: Input with Greeting

Create a program that asks for your name and then greets you personally.

**Program interaction example:**
```
What is your name? Bob
Hello, Bob!
```

**What to do:**
1. Create a file called `greet.py`
2. Ask for the user's name
3. Print a greeting that includes their name
4. Use string concatenation (`+`) to combine text

**Hint:** You'll need to combine the text `"Hello, "` with the name variable.

---

## Exercise 4: Debug This

This code has an error. Run it, read the error, and fix it.

```python
name = input(What is your name?)
print(name)
```

**Expected program interaction:**
```
What is your name? Alice
Alice
```

**What to do:**
1. Create a file called `debug_input.py`
2. Copy the broken code
3. Run it and read the error
4. Fix it
5. Run it again to verify

**Hint:** The error message will tell you exactly what's wrong. Look for missing quotation marks.

---

## Exercise 5: Creating a Profile

Create a program that collects information about a person and displays it in a nice format.

**Program interaction example:**
```
Welcome!

Name: Alice
Age: 28
Email: alice@example.com

Your information:
Name: Alice
Age: 28
Email: alice@example.com
```

**What to do:**
1. Create a file called `profile.py`
2. Display a welcome message
3. Ask for name, age, and email
4. Display a nice profile with all the information
5. Use blank lines (`print()`) to make it readable

**Hint:** Use multiple `input()` statements and then multiple `print()` statements to display nicely.

---

## Exercise 6: Conversation

Create a program that has a simple conversation with the user.

**Program interaction example:**
```
What is your name? Alice
Hello, Alice! Nice to meet you.
What is your favorite color? Blue
Blue is a great color, Alice!
```

**What to do:**
1. Create a file called `conversation.py`
2. Ask for the user's name
3. Print a response using their name
4. Ask for their favorite color
5. Print another response using both their name and color

**Hint:** Collect input, then use those variables in print statements.

---

## Exercise 7: Two People

Create a program that asks for two people's names and creates a message about them.

**Program interaction example:**
```
First person's name: Alice
Second person's name: Bob
Alice and Bob are best friends!
```

**What to do:**
1. Create a file called `two_people.py`
2. Ask for two different names
3. Store them in different variables
4. Print a sentence that includes both names

**Hint:** Use `+` to combine text and variables.

---

## Exercise 8: The Text Problem (Important!)

Run this code and observe what happens:

```python
number1 = input("Enter first number: ")
number2 = input("Enter second number: ")

print(number1 + number2)
```

**Program interaction example:**
```
Enter first number: 5
Enter second number: 3
53
```

**What to do:**
1. Create a file called `text_problem.py`
2. Copy the code above
3. Run it
4. Notice the output
5. Answer these questions (write them down):
   - You entered 5 and 3. Why did you get 53?
   - What would you need to do to get 8 instead?

**Key insight:** This demonstrates that `input()` returns text, not numbers. Text `"5"` + text `"3"` = text `"53"` (joining), not math.

---

## Exercise 9: Building a Sentence

Create a program that asks for words and combines them into a sentence.

**Program interaction example:**
```
Enter a noun: cat
Enter a verb: jumped
Enter an adjective: happy

The happy cat jumped!
```

**What to do:**
1. Create a file called `sentence.py`
2. Ask for three different words (noun, verb, adjective)
3. Store each in a variable
4. Print them combined into a sentence
5. Use `+` to combine text

**Hint:** You'll need to add spaces between words when combining them.

---

## Exercise 10: City Information

Create a program that gathers information about a city and displays it.

**Program interaction example:**
```
City name: Paris
Country: France
Population: 2.2 million

City: Paris
Country: France
Population: 2.2 million
```

**What to do:**
1. Create a file called `city_info.py`
2. Ask for city name, country, and population
3. Display all the information in a formatted way
4. Use clear prompts so the user knows what to enter

**Hint:** Remember to use quotes in `input()` prompts.

---

## Exercise 11: Debug Multiple Inputs

This code has TWO errors. Find and fix both.

```python
first_name = input("First name")
last_name = input(Last name: )

print(first_name + last_name)
```

**Expected program interaction:**
```
First name: Alice
Last name: Johnson
AliceJohnson
```

**What to do:**
1. Create a file called `debug_multiple.py`
2. Copy the broken code
3. Identify both errors
4. Fix them
5. Run it and verify it works

**Hint:** Look at each `input()` statement. Check for missing or mismatched quotes.

---

## Exercise 12: Interactive Story

Create a program that tells a short story using information provided by the user.

**Program interaction example:**
```
What is your name? Alice
What is your favorite animal? Dragon
What is your favorite place? Mountain

Once upon a time, Alice went to the Mountain.
She found a Dragon!
The Dragon and Alice became best friends.
The End.
```

**What to do:**
1. Create a file called `story.py`
2. Ask for a name, favorite animal, and favorite place
3. Display a story that includes all three pieces of information
4. Make it creative and fun

**Hint:** Use multiple `print()` statements to tell the story line by line.

---

## Checking Your Work

After each exercise, ask yourself:

- ✓ Did my program run without error?
- ✓ Did the program ask for input?
- ✓ Did it store the input in variables?
- ✓ Did it display the expected output?
- ✓ Did I use clear prompts?
- ✓ Can I explain what each line does?

---

## Important Observations

**About `input()`:**
- It always returns text
- The user controls when the program continues
- Good prompts are clear and specific
- You can use input values multiple times

**About combining input with variables:**
- Input is just another way to assign values to variables
- Once you have a value in a variable, it works like any other variable
- You can combine multiple input values in output

---

## Next Steps

Once you've completed these exercises:

1. You can use `input()` to ask users for information
2. You can store user input in variables
3. You can use input multiple times in your program
4. You understand that `input()` returns text
5. You can combine input with other operations

You're ready for the next concept: **String Operations** — doing things with text like combining it, finding pieces of it, and changing it.

Next lesson: making text do things!
