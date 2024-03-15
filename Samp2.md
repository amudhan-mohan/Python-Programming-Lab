Inheritance:

Inheritance could be a feature of object-oriented programming that permits one class to acquire characteristics from another class. In other words, inheritance permits a class to be characterized in terms of another class, which makes it simpler to make and keep up an application.

Types of Inheritance in Python
Single inheritance: A derived class inherits from one base class.
Multiple inheritance: A derived class inherits from multiple base classes.
Multilevel inheritance: A derived class inherits from a base class that inherits from another base class.
Hierarchical inheritance: Multiple derived classes inherit from the same base class.
Hybrid inheritance: A combination of two or more of the above inheritance types.

Inheritance Syntax:

Inheritance allows a class (subclass/derived class) to inherit attributes and methods from another class (superclass/base class).
Syntax for inheritance:
python

class DerivedClassName(BaseClassName):
    # class body

Example: 
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

# Example usage
dog = Dog()
dog.speak()  # Output: Animal speaks
dog.bark()   # Output: Dog barks

Polymorphism:

Polymorphism in Python refers to the ability of different objects to respond to the same method or attribute call in different ways. It allows objects of different classes to be treated as objects of a common superclass. This concept is fundamental to object-oriented programming and enables flexibility and extensibility in code.

Compile-Time Polymorphism:

Achieved through method overloading and operator overloading.
Resolves at compile time based on the number and types of arguments.
Run-Time Polymorphism:

Achieved through method overriding.
Resolves at runtime based on the actual type of the object.

Polymorphism Syntax:

Polymorphism allows objects of different classes to be treated as objects of a common superclass.
It allows methods to be overridden in a subclass with the same name but different implementation.

Syntax for polymorphism:

class BaseClassName:
    def method_name(self):
        # base class method implementation

class DerivedClassName(BaseClassName):
    def method_name(self):
        # derived class method implementation


Example: 

class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Dog barks")

# Example usage
animal = Animal()
dog = Dog()

animal.speak()  # Output: Animal speaks
dog.speak()     # Output: Dog barks

