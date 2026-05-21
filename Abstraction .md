# 🐍 Python OOP: Abstract Class & Method Example

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
~~~
from abc import ABC, abstractmethod


class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass


class Rectangle(Shape):

    def __init__(self):
        self.length = 10
        self.breadth = 5

    def calculate_area(self):
        area = self.length * self.breadth
        print("Area of Rectangle =", area)


class Circle(Shape):

    def __init__(self):
        self.radius = 7

    def calculate_area(self):
        area = 3.14 * self.radius * self.radius
        print("Area of Circle =", area)


r = Rectangle()
r.calculate_area()

c = Circle()
c.calculate_area()
~~~

## Output
~~~
Area of Rectangle = 50
Area of Circle = 153.86
~~~


## Result
Thus, the Python program demonstrating abstract classes and abstract methods was executed successfully.
