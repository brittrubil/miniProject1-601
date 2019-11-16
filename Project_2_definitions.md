**1.	How python uses the Indentation to control Flow**
<br>

Python uses indentation to the control the flow of code. Each block contains a group of code to be run together. Once a 
separate indentation is made, python will read it as a separate group of code. 
Note that the block must all contain the same amount of indentations to be read together.
<br>

Example layout:

![Blocks](/images/blocks.png)

**2.	Don’t repeat yourself**
The Don’t repeat yourself (DRY) principle in python is necessary in avoiding unnecessary repetition with the code. 
It allows for the code to have a better flow and be easier to read. Another benefit is that if the code needs to be update, 
it will help in reducing additional work needed. 

Example: 
Rather than listing the following separately it could be combined into one listing. 
Original
print(test1)
print(test2)
print(test3)
	DRY Applied
	print(test1,test2,test3)
	

**3.	Design patterns from Gang of Four**
<br>
The Gang of Four design patterns are a group of 23 patterns that are the foundation for software design. 
They breakdown into three categories: Creational, Structural, and Behavior.


A singleton pattern which is a creational pattern is a class of which only a single instance can exist. 

Example of Singleton pattern: 

class Singleton(type):
 
 def __init__(cls, name, bases, attrs, kwargs):
        super().__init__(name, bases, attrs)
        cls._instance = None

    def __call__(cls, args, kwargs):
        if cls._instance is None:
            cls._instance = super().__call__(args, kwargs)
        return cls._instance

class MyClass(metaclass=Singleton):
    """
    Example class.
    """
    pass

def main():
    m1 = MyClass()
    m2 = MyClass()
    assert m1 is m2

if __name__ == "__main__":
    main()
    
 **4.Class**
<br>

A class allows for a way to create objects. It is consider to be the template for creating objects.

Example:
class MyClass:
  x = 5
  
  **5.	Object**
<br>

Python is an object oriented programming language. An object is a collection of data (variables) and methods (functions) 
that act on those data. 
Example: 
p1 = MyClass()
print(p1.x)

**6.	Static**
<br>
Static method is also a method which is bound to the class and not the object of the class and cannot access or modify class state.
Static variable or class are shared by all objects.
<br>
