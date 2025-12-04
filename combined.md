
# 🐍6A Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return 3.14 * self.radius * self.radius

rect = Rectangle(10, 5)
circle = Circle(7)
print("Area of Rectangle:", rect.calculate_area())
print("Area of Circle:", circle.calculate_area())
```


## Output
<img width="1141" height="250" alt="Screenshot 2025-11-23 184837" src="https://github.com/user-attachments/assets/2816090a-3747-40f9-9dcd-34bc16168fd6" />


## Result
The program successfully demonstrates the concept of abstract classes and methods in Python by implementing calculate_area() in both Rectangle and Circle subclasses.



# 🐍6B Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
class Rectangle:
    def __init__(self, length, breadth):
        self.__length = length      # private member
        self.__breadth = breadth    # private member
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)
rect = Rectangle(10, 5)
```


## Output
<img width="1144" height="265" alt="Screenshot 2025-11-23 185046" src="https://github.com/user-attachments/assets/b884400b-9080-40b9-9778-b7d9be6c47a4" />


## Result
The program successfully demonstrates Encapsulation in Python by using private members __length and __breadth in the Rectangle class.



# 🐟6C Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class A:
    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

ob1 = A(5)
ob2 = A(10)

print(ob1 < ob2)
```

## OUTPUT
<img width="1143" height="259" alt="Screenshot 2025-11-23 185304" src="https://github.com/user-attachments/assets/0683534b-e270-47b7-962e-76ea744c1a07" />


## RESULT
The program successfully demonstrates operator overloading in Python by overriding the less than (<) operator using the lt() method.



# 🐍6D Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A:
    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

ob1 = A(5)
ob2 = A(10)
print(ob1 < ob2)
```

## Output
<img width="1138" height="250" alt="Screenshot 2025-11-23 185500" src="https://github.com/user-attachments/assets/60481a6e-719d-429d-a651-d5978fd615a9" />


## Result
The program successfully demonstrates operator overloading in Python by overriding the less than (<) operator using the lt() method.


# # 🐍6E Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
class Beans:
    def type(self):
        print("Vegetable")
    def color(self):
        print("Green")

class Mango:
    def type(self):
        print("Fruit")
    def color(self):
        print("Yellow")

def func(obj):
    obj.type()
    obj.color()

obj1 = Beans()
obj2 = Mango()

func(obj1)
func(obj2)
```

## Output
<img width="1144" height="328" alt="Screenshot 2025-11-23 185613" src="https://github.com/user-attachments/assets/3859eb15-b7bd-44cb-8ab7-109bf71bf7af" />


## Result
The program successfully demonstrates polymorphism in Python OOP by using a generic function that works with different classes (Beans and Mango) and calls their respective methods.
