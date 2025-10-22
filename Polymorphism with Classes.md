# # 🐍 Python OOP: Polymorphism with Classes

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

class Beans:

    def type(self):
    
        print("Type: Vegetable")

    def color(self):
    
        print("Color: Green")

class Mango:

    def type(self):
    
        print("Type: Fruit")

    def color(self):
    
        print("Color: Yellow")

# 3. Define Generic Function func(obj)

def func(obj):
   
    print(f"\nCalling methods for {obj.__class__.__name__} object:")
    
    obj.type()  
    
    obj.color() 

if __name__ == "__main__":
   
    print("--- Creating Objects ---")
    
    obj_beans = Beans()
    
    obj_mango = Mango()

    func(obj_beans)
    
    print("The 'func' function worked with both objects,")
    
    print("even though they are different types.")
    
    print("This is polymorphism (duck typing).")



## Output

--- Creating Objects ---

Calling methods for Beans object:

Type: Vegetable

Color: Green

Calling methods for Mango object:

Type: Fruit

Color: Yellow

## Result

The 'func' function worked with both objects,

even though they are different types.

This is polymorphism (duck typing).
