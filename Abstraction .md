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

import math

from abc import ABC, abstractmethod

class Shape(ABC):
    
    @abstractmethod
    
    def calculate_area(self):
    
        pass

class Rectangle(Shape):
    
    def __init__(self, length=10, breadth=5):
    
        self.length = length
        
        self.breadth = breadth
        
        print(f"Rectangle created with length: {self.length}, breadth: {self.breadth}")

    def calculate_area(self):
    
        return self.length * self.breadth

class Circle(Shape):
    
    def __init__(self, radius=7):
    
        self.radius = radius
        
        print(f"Circle created with radius: {self.radius}")

    def calculate_area(self):
    
        return math.pi * (self.radius ** 2)

if __name__ == "__main__":
  
    rect = Rectangle(10, 5)
    
    circ = Circle(7)
    
    rect_area = rect.calculate_area()
    
    print(f"Area of Rectangle: {rect_area}")
    
    circ_area = circ.calculate_area()
    
    print(f"Area of Circle: {circ_area:.2f}")



## Output

Rectangle created with length: 10, breadth: 5
  
Circle created with radius: 7

## Result

Area of Rectangle: 50

Area of Circle: 153.94
