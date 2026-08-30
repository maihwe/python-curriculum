# OOP Basics: Classes and Objects - Lecture

## Why This Matters

So far, you've organized code with functions:

```python
def create_student(name, age, grade):
    student = {"name": name, "age": age, "grade": grade}
    return student

def print_student(student):
    print(f"{student['name']}: {student['grade']}")

alice = create_student("Alice", 20, "A")
print_student(alice)
```

This works, but data and functions are separate. Real programs need **objects** that combine data and functions together.

**Object-Oriented Programming (OOP)** lets you create objects that hold both data AND behavior.

```python
class Student:
    def __init__(self, name, age, grade):
        self.name = name
        self.age = age
        self.grade = grade
    
    def print_info(self):
        print(f"{self.name}: {self.grade}")

alice = Student("Alice", 20, "A")
alice.print_info()
```

Data and behavior are now together. Much cleaner.

---

## The Mental Model: What Is a Class?

A **class** is a blueprint for creating objects.

```
Blueprint (Class):        Real Thing (Object):
House blueprint    →      Actual house
Car design         →      Actual car
Student template   →      Alice (specific student)
```

A class defines:
- What data it has (attributes)
- What it can do (methods)

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name      # Data (attribute)
        self.breed = breed
    
    def bark(self):           # Behavior (method)
        print(f"{self.name} says Woof!")
```

`Dog` is the class (blueprint).
`fluffy = Dog("Fluffy", "Golden")` creates an object (actual dog).

---

## The Mental Model: Attributes

**Attributes** are data stored in an object.

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name      # Attribute: name
        self.breed = breed    # Attribute: breed

fluffy = Dog("Fluffy", "Golden")
print(fluffy.name)   # "Fluffy"
print(fluffy.breed)  # "Golden"
```

Each object has its own copy of attributes.

```python
fluffy = Dog("Fluffy", "Golden")
buddy = Dog("Buddy", "Labrador")

print(fluffy.name)   # "Fluffy"
print(buddy.name)    # "Buddy" (different!)
```

---

## The Mental Model: Methods

**Methods** are functions inside a class. They describe what an object can do.

```python
class Dog:
    def __init__(self, name):
        self.name = name
    
    def bark(self):
        print(f"{self.name} says Woof!")
    
    def sit(self):
        print(f"{self.name} sits down")

fluffy = Dog("Fluffy")
fluffy.bark()   # "Fluffy says Woof!"
fluffy.sit()    # "Fluffy sits down"
```

Methods are called on objects using dot notation: `object.method()`

---

## The Mental Model: The Constructor (__init__)

`__init__` is a special method that runs when you create an object. It initializes attributes.

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

alice = Student("Alice", 20)  # __init__ runs here
```

Flow:
1. Create new object
2. Call `__init__` with arguments
3. Initialize attributes
4. Return object

---

## The Mental Model: self

`self` represents the object itself.

```python
class Dog:
    def __init__(self, name):
        self.name = name  # self = this specific dog
    
    def bark(self):
        print(f"{self.name} barks")  # self.name = this dog's name
```

When you call `fluffy.bark()`, Python automatically passes `fluffy` as `self`.

---

## The Mental Model: Inheritance

**Inheritance** means a class can inherit from another class.

```
Animal (parent/base class)
  ├── Dog (inherits from Animal)
  └── Cat (inherits from Animal)
```

Dog and Cat inherit attributes and methods from Animal:

```python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def make_sound(self):
        print("Some sound")

class Dog(Animal):  # Inherits from Animal
    def make_sound(self):
        print(f"{self.name} barks")

fluffy = Dog("Fluffy")
fluffy.make_sound()  # "Fluffy barks"
```

Dog gets `name` attribute from Animal but overrides `make_sound`.

---

## Key Concepts to Remember

1. **Class** = blueprint for objects
2. **Object** = instance of a class
3. **Attributes** = data stored in object
4. **Methods** = functions inside class
5. **self** = reference to object
6. **__init__** = constructor (initializer)
7. **Inheritance** = classes inherit from other classes
8. **Override** = child class replaces parent method
9. **Encapsulation** = bundle data and methods together
10. **OOP** = organize code around objects, not functions

---

## Common Misconceptions

**"Classes are complicated"**

They're just blueprints that combine data and functions. Simple.

**"I have to use OOP"**

No. Python supports multiple styles. Use OOP when it makes sense.

**"Objects are slower than functions"**

Negligible difference. Use what's clearest.

**"Inheritance is always good"**

No. Use it when there's genuine "is-a" relationship.

---

## Real-World OOP

**Bank Account:**
```python
class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner
        self.balance = balance
    
    def deposit(self, amount):
        self.balance += amount
    
    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
```

**Game Character:**
```python
class Character:
    def __init__(self, name, health):
        self.name = name
        self.health = health
    
    def take_damage(self, damage):
        self.health -= damage
    
    def heal(self, amount):
        self.health += amount
```

---

## Summary

**OOP** organizes code around objects that combine data and behavior.

**Classes** are blueprints. **Objects** are instances.

**Attributes** store data. **Methods** define behavior.

**Inheritance** lets classes inherit from other classes.

OOP makes complex programs organized and maintainable.

Next: see OOP in action.
