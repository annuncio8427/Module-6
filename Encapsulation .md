# 🐍 Python OOP: Encapsulation with Private Members

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

class Rectangle:
    
    def __init__(self, length=10, breadth=5):
        
        self.__length = length
        
        self.__breadth = breadth
        
        print("--- Inside the __init__ method ---")
        
        print(f"Accessing private __length: {self.__length}")
        
        print(f"Accessing private __breadth: {self.__breadth}")

if __name__ == "__main__":
    
    rect = Rectangle(20, 10)
    
    try:
    
        print(f"Accessing rect.__length: {rect.__length}")
        
    except AttributeError as e:
    
        print(f"Caught expected error: {e}")



## Output

Accessing private __length: 20

Accessing private __breadth: 10

## Result

Accessing private __length: 20

Accessing private __breadth: 10

Caught expected error: 'Rectangle' object has no attribute '__length'
