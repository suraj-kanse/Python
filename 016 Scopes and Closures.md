Scope determines where your variables live and who has access to them. Think of Scope like a house. If you create a variable out in the open (Global Scope), everyone can see it. If you create a variable inside a function (Local Scope), it is locked inside that "house."

Understanding this hierarchy, and what happens when a function "packs its bags" to leave the house (Closures), separates junior developers from senior engineers.

The Scope Hierarchy (The House Analogy)
In Python, whenever you indent code (like inside a ```def``` function or an ```if``` block), you are creating a new Scope.
- Global Scope (The World): Variables defined at the top level of your file without indentation.
- Local Scope (The House): Variables defined inside a specific function.

The Golden Rule of Scope Access:
- You can always look OUT of the house to see the world. (Functions can read Global variables).
- You can never look IN to the house from the world. (The Global scope cannot read variables trapped inside a function).
```
username = "Chai Aur Code" # GLOBAL SCOPE

def my_func():
    balance = 100 # LOCAL SCOPE
    print(username) # Works! The function can look out and see "Chai Aur Code"

print(balance) # CRASH! The global scope cannot look into the function's house.
```

The Climbing Algorithm (LEGB Rule)
What happens if you have variables with the exact same name? Python follows an strict order of operations to find a variable, often referred to academically as the LEGB Rule (Local, Enclosing, Global, Built-in).

The "Climbing" theory:
- Python first looks inside the current room (Local Function).
- If it doesn't find the variable, it steps out into the hallway (Enclosing/Parent Function).
- If it doesn't find it there, it steps out of the house into the world (Global Scope).
```
x = 99 # Global Scope

def func1():
    x = 88 # Enclosing Scope
    
    def func2():
        print(x) # Where does it get 'x' from?
        
    func2()

func1() 
# Outputs: 88. 
# It checked func2 (empty), climbed up to func1 and found 88. It stopped there and never needed to check Global.
```


