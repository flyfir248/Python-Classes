# Python-Classes
Classes in Python

````
class Animal:
    def __init__(self):
        print("Animal can move.")
        
class Mammal(Animal):
    def __init__(self):
        super().__init__()
        print("Mammals are warm-blooded.")
        
class Cat(Mammal):
    def __init__(self):
        super().__init__()
        print("Cats have fur.")

kitty = Cat()
````

In the above code, we have three classes: Animal, Mammal, and Cat. 

The Mammal and Cat classes inherit from the Animal class, and each class has its own __init__ method that prints a statement. 

When we create an object of the Cat class, the __init__ method of all three classes gets called in the order of inheritance (Animal -> Mammal -> Cat).

In the Mammal class, we use super().__init__() to call the __init__ method of the parent class (Animals). 

Similarly, in the Cat class, we use super().__init__() to call the __init__ method of the parent class (Mammal). 

This allows us to execute the code in the parent class before executing the code in the child class, and build a chain of method calls that follows the order of inheritance.

When we run the code and create an instance of the Cat class, the following output is displayed:

````
Animals can move.
Mammals are warm-blooded.
Cats have fur.
````

This example shows how the super() function can be used in a multi-level class hierarchy to call the method of the parent class and maintain the order of inheritance.
