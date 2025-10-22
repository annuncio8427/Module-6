# 🐍 Python OOP: Operator Overloading (Less Than `<`)

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

class A:

    def __init__(self, a):
      
        self.a = a
        
        print(f"Object created with value a = {self.a}")

    def __lt__(self, other_obj):
    
        print(f"\nComparing {self.a} < {other_obj.a}")
        
        if self.a < other_obj.a:
        
            return "ob1 is less than ob2"
            
        else:
        
            return "ob2 is less than or equal to ob1" 

if __name__ == "__main__":

    ob1 = A(20)
    
    ob2 = A(30)

    print("\n--- Using the < Operator ---")
    
    result = ob1 < ob2
    
    print(f"Result of (ob1 < ob2): {result}")
    
    print("\n--- Using the < Operator (Reversed) ---")
    
    ob3 = A(50)
    
    ob4 = A(40)
    
    result_2 = ob3 < ob4
    
    print(f"Result of (ob3 < ob4): {result_2}")
    
    print("The '<' operator was successfully overloaded,")
    
    print("calling the custom __lt__ method.")


## Output
--- Creating Objects ---

Object created with value a = 20

Object created with value a = 30

--- Using the < Operator ---

Comparing 20 < 30

Result of (ob1 < ob2): ob1 is less than ob2

--- Using the < Operator (Reversed) ---

Object created with value a = 50

Object created with value a = 40

Comparing 50 < 40

Result of (ob3 < ob4): ob2 is less than or equal to ob1

## Result

The '<' operator was successfully overloaded, calling the custom __lt__ method.
