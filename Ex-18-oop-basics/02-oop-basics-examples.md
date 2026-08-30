# OOP Basics: Examples & Demos

## Example 1: Simple Class

**Code:**
```python
class Dog:
    def __init__(self, name):
        self.name = name

fluffy = Dog("Fluffy")
print("Dog name:", fluffy.name)
```

**Output:**
```
Dog name: Fluffy
```

**Key insight:** Class is a blueprint. Object is a specific instance.

---

## Example 2: Class with Attributes

**Code:**
```python
class Student:
    def __init__(self, name, age, grade):
        self.name = name
        self.age = age
        self.grade = grade

alice = Student("Alice", 20, "A")
print(f"{alice.name}: age {alice.age}, grade {alice.grade}")
```

**Output:**
```
Alice: age 20, grade A
```

**Key insight:** Objects store multiple attributes.

---

## Example 3: Multiple Objects

**Code:**
```python
class Student:
    def __init__(self, name, grade):
        self.name = name
        self.grade = grade

alice = Student("Alice", "A")
bob = Student("Bob", "B")
charlie = Student("Charlie", "A")

print(alice.name, alice.grade)
print(bob.name, bob.grade)
print(charlie.name, charlie.grade)
```

**Output:**
```
Alice A
Bob B
Charlie A
```

**Key insight:** Each object is independent with own data.

---

## Example 4: Methods

**Code:**
```python
class Dog:
    def __init__(self, name):
        self.name = name
    
    def bark(self):
        print(f"{self.name} says Woof!")
    
    def sit(self):
        print(f"{self.name} sits down")

fluffy = Dog("Fluffy")
fluffy.bark()
fluffy.sit()
```

**Output:**
```
Fluffy says Woof!
Fluffy sits down
```

**Key insight:** Methods are functions that belong to objects.

---

## Example 5: Methods That Modify Attributes

**Code:**
```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.balance = balance
    
    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited ${amount}")
    
    def withdraw(self, amount):
        self.balance -= amount
        print(f"Withdrew ${amount}")
    
    def show_balance(self):
        print(f"Balance: ${self.balance}")

alice_account = BankAccount("Alice", 1000)
alice_account.show_balance()
alice_account.deposit(500)
alice_account.withdraw(200)
alice_account.show_balance()
```

**Output:**
```
Balance: $1000
Deposited $500
Withdrew $200
Balance: $1300
```

**Key insight:** Methods can read and modify object attributes.

---

## Example 6: Inheritance Basic

**Code:**
```python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def make_sound(self):
        print("Some generic sound")

class Dog(Animal):
    pass

fluffy = Dog("Fluffy")
print(fluffy.name)
fluffy.make_sound()
```

**Output:**
```
Fluffy
Some generic sound
```

**Key insight:** Dog inherits from Animal automatically.

---

## Example 7: Override Methods

**Code:**
```python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def make_sound(self):
        print("Generic sound")

class Dog(Animal):
    def make_sound(self):
        print(f"{self.name} barks!")

class Cat(Animal):
    def make_sound(self):
        print(f"{self.name} meows!")

dog = Dog("Fluffy")
cat = Cat("Whiskers")

dog.make_sound()
cat.make_sound()
```

**Output:**
```
Fluffy barks!
Whiskers meows!
```

**Key insight:** Child classes can override parent methods.

---

## Example 8: Inheritance with Extended Features

**Code:**
```python
class Animal:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def info(self):
        print(f"{self.name} is {self.age} years old")

class Dog(Animal):
    def __init__(self, name, age, breed):
        self.name = name
        self.age = age
        self.breed = breed
    
    def info(self):
        print(f"{self.name} is {self.age} years old, breed: {self.breed}")

fluffy = Dog("Fluffy", 3, "Golden Retriever")
fluffy.info()
```

**Output:**
```
Fluffy is 3 years old, breed: Golden Retriever
```

**Key insight:** Child can have more attributes than parent.

---

## Example 9: Game Character

**Code:**
```python
class Character:
    def __init__(self, name, health):
        self.name = name
        self.health = health
    
    def take_damage(self, damage):
        self.health -= damage
        print(f"{self.name} took {damage} damage")
    
    def heal(self, amount):
        self.health += amount
        print(f"{self.name} healed {amount}")
    
    def status(self):
        print(f"{self.name} - Health: {self.health}")

hero = Character("Hero", 100)
hero.status()
hero.take_damage(20)
hero.status()
hero.heal(10)
hero.status()
```

**Output:**
```
Hero - Health: 100
Hero took 20 damage
Hero - Health: 80
Hero healed 10
Hero - Health: 90
```

**Key insight:** OOP models real-world entities well.

---

## Example 10: Store Objects in List

**Code:**
```python
class Student:
    def __init__(self, name, grade):
        self.name = name
        self.grade = grade

students = [
    Student("Alice", "A"),
    Student("Bob", "B"),
    Student("Charlie", "A")
]

for student in students:
    print(f"{student.name}: {student.grade}")
```

**Output:**
```
Alice: A
Bob: B
Charlie: A
```

**Key insight:** Can store objects in collections.

---

## Example 11: Store Objects in Dictionary

**Code:**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

people = {
    "alice": Person("Alice", 25),
    "bob": Person("Bob", 30),
    "charlie": Person("Charlie", 28)
}

print(people["alice"].name, people["alice"].age)
print(people["bob"].name, people["bob"].age)
```

**Output:**
```
Alice 25
Bob 30
```

**Key insight:** Objects can be dictionary values.

---

## Example 12: Checking Object Type

**Code:**
```python
class Dog:
    def __init__(self, name):
        self.name = name

class Cat:
    def __init__(self, name):
        self.name = name

fluffy = Dog("Fluffy")
whiskers = Cat("Whiskers")

print(isinstance(fluffy, Dog))
print(isinstance(fluffy, Cat))
print(isinstance(whiskers, Cat))
```

**Output:**
```
True
False
True
```

**Key insight:** Use isinstance() to check object type.

---

## Example 13: String Representation

**Code:**
```python
class Student:
    def __init__(self, name, grade):
        self.name = name
        self.grade = grade
    
    def __str__(self):
        return f"Student({self.name}, {self.grade})"

alice = Student("Alice", "A")
print(alice)
print(str(alice))
```

**Output:**
```
Student(Alice, A)
Student(Alice, A)
```

**Key insight:** __str__ defines how object prints.

---

## Example 14: Real-World - Todo Item

**Code:**
```python
class TodoItem:
    def __init__(self, task, completed=False):
        self.task = task
        self.completed = completed
    
    def mark_complete(self):
        self.completed = True
    
    def status(self):
        status = "✓" if self.completed else "○"
        return f"{status} {self.task}"

todo1 = TodoItem("Buy groceries")
todo2 = TodoItem("Write code")
todo3 = TodoItem("Exercise", True)

print(todo1.status())
print(todo2.status())
print(todo3.status())

todo1.mark_complete()
print(todo1.status())
```

**Output:**
```
○ Buy groceries
○ Write code
✓ Exercise
✓ Buy groceries
```

**Key insight:** OOP models real workflow well.

---

## Example 15: Real-World - Rectangle

**Code:**
```python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)
    
    def info(self):
        print(f"Rectangle {self.width}x{self.height}")
        print(f"Area: {self.area()}")
        print(f"Perimeter: {self.perimeter()}")

rect = Rectangle(5, 3)
rect.info()
```

**Output:**
```
Rectangle 5x3
Area: 15
Perimeter: 16
```

**Key insight:** Methods can compute values from attributes.

---

## Summary of Examples

- Simple classes and objects
- Attributes and multiple objects
- Methods that use self
- Methods that modify attributes
- Inheritance and method override
- Extending inherited classes
- Game character modeling
- Objects in collections
- isinstance() checking
- Custom __str__
- Real-world Todo items
- Real-world Rectangle calculations

Next: practice with exercises.
