# Python Curriculum Hierarchy: Reverse-Engineered

## What We're Building Toward
A complete Python programmer who can:
- Write programs that solve real problems
- Work with data and automate tasks
- Read and understand code
- Debug and fix problems
- Think like a programmer

---

## Concept Dependency Graph (Low to High)

### TIER 1: Program Execution Fundamentals
*Foundation: How computers execute instructions*

1. **Program Execution** (Hello World)
   - What a program is
   - Sequential execution (top to bottom)
   - Output with `print()`
   - Dependencies: None

2. **Data Storage** (Variables)
   - Storing values
   - Named references
   - Reusing values
   - Dependencies: Program Execution

3. **User Interaction** (Input)
   - Reading user input
   - Storing input
   - Interactive programs
   - Dependencies: Program Execution, Data Storage

---

### TIER 2: Data & Operations
*Foundation: Working with different types of data and doing things with them*

4. **Text Manipulation** (Strings)
   - Text as data
   - Combining text (concatenation)
   - String methods (uppercase, lowercase, etc.)
   - String indexing (getting characters)
   - Text length
   - Dependencies: Data Storage, User Interaction

5. **Type Conversion**
   - Converting text to numbers
   - Converting numbers to text
   - Why types matter
   - `int()`, `float()`, `str()`
   - Dependencies: Data Storage, Text Manipulation

6. **Arithmetic Operations**
   - Math with numbers (+, -, *, /, //, %)
   - Order of operations
   - Storing math results
   - Dependencies: Data Storage, Type Conversion

7. **Comparison Operations**
   - Comparing values (==, !=, <, >, <=, >=)
   - Boolean results (True/False)
   - Comparisons in variables
   - Dependencies: Data Storage, Arithmetic Operations

8. **Logical Operations**
   - AND, OR, NOT
   - Combining conditions
   - Boolean logic
   - Dependencies: Comparison Operations

---

### TIER 3: Control Flow
*Foundation: Making decisions and repeating actions*

9. **Conditional Statements** (if/else)
   - Making decisions based on conditions
   - if, elif, else
   - Running different code paths
   - Dependencies: Comparison Operations, Logical Operations

10. **Loops - while**
    - Repeating code
    - Loop conditions
    - Loop control (break, continue)
    - Dependencies: Conditional Statements

11. **Loops - for**
    - Iterating over sequences
    - Loop variables
    - Range function
    - Dependencies: Loops - while

---

### TIER 4: Data Structures
*Foundation: Organizing and managing multiple pieces of data*

12. **Lists**
    - Storing multiple values
    - Indexing (accessing elements)
    - List methods (append, remove, etc.)
    - List iteration with loops
    - Dependencies: Loops (for and while)

13. **Dictionaries**
    - Key-value pairs
    - Accessing by key
    - Dictionary methods
    - Dictionary iteration
    - Dependencies: Lists

14. **Tuples**
    - Immutable sequences
    - When to use tuples vs lists
    - Tuple unpacking
    - Dependencies: Lists

15. **Sets**
    - Unique values
    - Set operations
    - Set methods
    - Dependencies: Lists

---

### TIER 5: Functions & Abstraction
*Foundation: Writing reusable code*

16. **Functions - Definition**
    - Defining functions
    - Parameters and arguments
    - Return values
    - Function scope
    - Dependencies: All previous tiers (functions use all concepts)

17. **Functions - Advanced**
    - Default parameters
    - *args and **kwargs
    - Recursion
    - Lambda functions
    - Dependencies: Functions - Definition

---

### TIER 6: File Operations
*Foundation: Persistent data*

18. **File I/O**
    - Reading files
    - Writing files
    - File modes
    - Closing files (with context managers)
    - Dependencies: Strings, Lists, Functions

---

### TIER 7: Advanced Concepts
*Foundation: Building complex programs*

19. **Error Handling**
    - Try/except/finally
    - Raising exceptions
    - Custom exceptions
    - Dependencies: Functions, File I/O

20. **Object-Oriented Programming**
    - Classes and objects
    - Attributes and methods
    - Inheritance
    - Encapsulation
    - Dependencies: Functions, Data Structures

21. **List Comprehensions**
    - Creating lists with loops
    - Conditional list comprehensions
    - Nested comprehensions
    - Dependencies: Lists, For loops, Conditional Statements

22. **Generators & Iterators**
    - yield keyword
    - Generator functions
    - When to use generators
    - Dependencies: Functions, For loops

---

### TIER 8: External Libraries & Integration
*Foundation: Leveraging existing code*

23. **Importing Modules**
    - import statements
    - Module structure
    - Using standard library
    - Dependencies: Functions, File I/O

24. **Working with JSON**
    - JSON format
    - Parsing JSON
    - Creating JSON
    - Dependencies: Dictionaries, File I/O, Importing Modules

25. **APIs and Requests** (Optional)
    - Making HTTP requests
    - JSON responses
    - Error handling with APIs
    - Dependencies: Importing Modules, Dictionaries, Error Handling

---

### TIER 9: Advanced Topics (Optional)
*Foundation: Specialized use cases*

26. **Decorators** (Optional)
    - Function decorators
    - Class decorators
    - Dependencies: Functions - Advanced

27. **Context Managers** (Optional)
    - with statement
    - Creating context managers
    - Dependencies: Functions - Advanced

28. **Testing** (Optional)
    - Unit testing
    - pytest
    - Test-driven development
    - Dependencies: Functions, Modules

---

## Summary: Order of Instruction

**PHASE 1: Basics** (Topics 1-3)
- How code runs
- Storing data
- Getting user input

**PHASE 2: Data & Math** (Topics 4-8)
- Working with text
- Converting types
- Math operations
- Making comparisons

**PHASE 3: Decision Making** (Topic 9)
- If/else statements
- Conditional logic

**PHASE 4: Repetition** (Topics 10-11)
- While loops
- For loops

**PHASE 5: Data Organization** (Topics 12-15)
- Lists
- Dictionaries
- Tuples
- Sets

**PHASE 6: Code Reuse** (Topics 16-17)
- Writing functions
- Advanced function techniques

**PHASE 7: Persistence** (Topic 18)
- Reading/writing files

**PHASE 8: Robustness** (Topic 19)
- Error handling

**PHASE 9: Object-Oriented** (Topic 20)
- Classes and OOP (optional but recommended)

**PHASE 10: Convenience** (Topics 21-22)
- List comprehensions
- Generators

**PHASE 11: Integration** (Topics 23-25)
- Modules and libraries
- JSON
- APIs (optional)

**PHASE 12: Advanced** (Topics 26-28)
- Decorators (optional)
- Context managers (optional)
- Testing (optional)

---

## Which Topics Are Required vs. Optional?

### Essential (Must Learn)
Topics 1-19: Everything through Error Handling
- These form the foundation for any Python program

### Recommended (Should Learn)
Topic 20: Object-Oriented Programming
- Not technically required for simple scripts
- Essential for larger programs
- Industry standard

### Nice-to-Have (Learn When Needed)
Topics 21-28: Advanced topics
- Learn based on your specific use case
- Not needed for basic Python proficiency

---

## Next Steps

Based on this hierarchy, we should build in this order:

**Already Created:**
1. ✅ Hello World (Program Execution)
2. ✅ Variables (Data Storage)
3. ✅ Input (User Interaction)

**Should Build Next:**
4. Strings (Text Manipulation)
5. Type Conversion (Converting Types)
6. Arithmetic (Math Operations)
7. Comparisons (Comparing Values)
8. Logical Operators (Boolean Logic)
9. If/Else (Conditionals)
10. While Loops (Repetition)
11. For Loops (Iteration)
... and so on

---

This is the complete hierarchy. Should we start building Topic 4 (Strings)?
