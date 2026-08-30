# OOP Basics: Exercises & Practice

## Exercise 1: Simple Class

Create a simple Dog class.

**Expected output:**
```
Fluffy
Golden Retriever
```

**What to do:**
1. Create a file called `simple_class.py`
2. Define Dog class with __init__
3. Add name and breed attributes
4. Create object and print attributes
5. Run it

**Hint:** `self.name = name`

---

## Exercise 2: Class with Multiple Attributes

Create a Student class with attributes.

**Expected output:**
```
Alice: 20, A
```

**What to do:**
1. Create a file called `student_class.py`
2. Define Student class
3. Add name, age, grade attributes
4. Create object with 3 values
5. Print formatted output
6. Run it

**Hint:** __init__ takes multiple parameters.

---

## Exercise 3: Multiple Objects

Create multiple Student objects.

**Expected output:**
```
Alice: A
Bob: B
Charlie: A
```

**What to do:**
1. Create a file called `multiple_objects.py`
2. Define Student class
3. Create 3 different student objects
4. Print each one's name and grade
5. Run it

**Hint:** Each object has its own data.

---

## Exercise 4: Simple Method

Create a Dog class with a bark method.

**Expected output:**
```
Fluffy says Woof!
```

**What to do:**
1. Create a file called `method.py`
2. Define Dog class with name
3. Add bark() method
4. Create dog and call bark()
5. Run it

**Hint:** `def bark(self):`

---

## Exercise 5: Multiple Methods

Create a class with multiple methods.

**Expected output:**
```
Fluffy barks!
Fluffy sits!
```

**What to do:**
1. Create a file called `multiple_methods.py`
2. Define Dog class
3. Add bark() and sit() methods
4. Call both methods
5. Run it

**Hint:** Each method uses self.

---

## Exercise 6: Method That Modifies Attribute

Create a BankAccount with deposit method.

**Expected output:**
```
Balance: $1000
Deposited $500
Balance: $1500
```

**What to do:**
1. Create a file called `bank_account.py`
2. Define BankAccount class
3. Add balance attribute
4. Add show_balance() method
5. Add deposit() method
6. Test both
7. Run it

**Hint:** `self.balance += amount`

---

## Exercise 7: Method with Calculation

Create a Rectangle with area method.

**Expected output:**
```
Area: 15
```

**What to do:**
1. Create a file called `rectangle.py`
2. Define Rectangle class
3. Add width and height
4. Add area() method
5. Print area of 5x3 rectangle
6. Run it

**Hint:** `return self.width * self.height`

---

## Exercise 8: Simple Inheritance

Create Animal class and Dog subclass.

**Expected output:**
```
Fluffy
```

**What to do:**
1. Create a file called `inheritance.py`
2. Define Animal class with __init__
3. Define Dog class that inherits from Animal
4. Create Dog object
5. Print name
6. Run it

**Hint:** `class Dog(Animal):`

---

## Exercise 9: Override Method

Create parent and child with different methods.

**Expected output:**
```
Fluffy barks
```

**What to do:**
1. Create a file called `override.py`
2. Define Animal with make_sound()
3. Define Dog that overrides make_sound()
4. Create Dog and call make_sound()
5. Run it

**Hint:** Same method name in child overrides parent.

---

## Exercise 10: Inheritance with New Attributes

Create Dog that has more attributes than Animal.

**Expected output:**
```
Fluffy: 3 years old, Golden Retriever
```

**What to do:**
1. Create a file called `inheritance_extend.py`
2. Define Animal with name, age
3. Define Dog with breed attribute too
4. Override __init__ in Dog
5. Print all 3 attributes
6. Run it

**Hint:** Dog __init__ sets name, age, breed.

---

## Exercise 11: Objects in List

Create list of Student objects.

**Expected output:**
```
Alice: A
Bob: B
Charlie: C
```

**What to do:**
1. Create a file called `objects_in_list.py`
2. Define Student class
3. Create list of 3 students
4. Loop and print each
5. Run it

**Hint:** `for student in students:`

---

## Exercise 12: Objects in Dictionary

Create dictionary of Person objects.

**Expected output:**
```
Alice: 25
Bob: 30
```

**What to do:**
1. Create a file called `objects_in_dict.py`
2. Define Person class
3. Create dict with Person objects
4. Access and print 2 entries
5. Run it

**Hint:** `people["alice"].name`

---

## Exercise 13: Real-World - Todo Item

Create TodoItem with complete tracking.

**Expected output:**
```
○ Buy groceries
✓ Finished project
```

**What to do:**
1. Create a file called `todo_item.py`
2. Define TodoItem class
3. Add task and completed attributes
4. Add status() method that returns ✓ or ○
5. Create 2 items (one complete, one not)
6. Print status of each
7. Run it

**Hint:** Use if/else for symbol.

---

## Exercise 14: Real-World - Character Battle

Create Character class for game.

**Expected output:**
```
Hero - Health: 100
Hero took 30 damage
Hero - Health: 70
Hero healed 20
Hero - Health: 90
```

**What to do:**
1. Create a file called `character.py`
2. Define Character class
3. Add take_damage() method
4. Add heal() method
5. Add status() method
6. Create character and test all methods
7. Run it

**Hint:** Modify health in methods.

---

## Exercise 15: Real-World - Bank Account System

Create complete BankAccount class.

**Expected output:**
```
Alice's account - Balance: $1000
Deposit $500 - Balance: $1500
Withdraw $200 - Balance: $1300
Bob's account - Balance: $500
```

**What to do:**
1. Create a file called `bank_system.py`
2. Define BankAccount class
3. Add owner and balance attributes
4. Add deposit() method
5. Add withdraw() method
6. Add display_balance() method
7. Create 2 accounts and test
8. Run it

**Hint:** Check balance before withdraw.

---

## Checking Your Work

After exercises, ask yourself:

- ✓ Can I create classes?
- ✓ Can I add attributes?
- ✓ Can I write methods?
- ✓ Do I understand inheritance?
- ✓ Can I override methods?

---

## Key Concepts to Remember

**Class:**
- Blueprint for objects
- Defines attributes and methods

**Object:**
- Instance of a class
- Has own copy of attributes

**Attributes:**
- Data stored in object
- `self.name = value`

**Methods:**
- Functions inside class
- First parameter is `self`

**Inheritance:**
- Child class inherits from parent
- Can override methods
- Can add new attributes

---

## Next Steps

Once you've mastered OOP:

1. You understand object-oriented design
2. You can model real-world entities
3. You're ready for modules
4. You understand Python's design patterns

You're making excellent progress! 🎉

**17 core topics complete → 1 final topic!**

Next topic: **Topic 19: Modules** (organizing code)
