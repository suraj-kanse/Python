Problem 1: Basic Function Syntax
Goal: Write a function to calculate and return the square of a number.
Concept Taught: How to define a function, pass a parameter, and use the ```return``` keyword. Using ```return``` instead of ```print()``` inside functions, as returning data allows you to store it in variables and use it later in your program.
```
# 'number' is the parameter (placeholder) the function accepts.
def square(number):
    return number ** 2

result = square(4)
print("The square is:", result) # Outputs: 16
```

Problem 2: Function with Multiple Parameters
Goal: Create a function that takes two numbers as parameters and returns their sum.
Concept: Passing multiple parameters into a function using a comma-separated list.
```
def add(num1, num2):
    return num1 + num2

# Using the function:
sum_result = add(5, 5)
print("The sum is:", sum_result) # Outputs: 10
```

Problem 3: Polymorphism in Functions
Goal: Write a function ```multiply``` that multiplies two numbers, but can also accept and multiply a string and a number.

Concept: Python operators naturally support polymorphism (one operator doing multiple things depending on the data type). The ```*``` operator mathematically multiplies two numbers, but if you pass a string and a number, it repeats the string. You don't have to write any special logic for this; Python handles it dynamically.
```
def multiply(p1, p2):
    return p1 * p2

# Scenario A: Passing two numbers
print(multiply(8, 5)) # Outputs: 40

# Scenario B: Passing a string and a number (Polymorphism)
print(multiply("a", 5)) # Outputs: aaaaa
```

Problem 4: Returning Multiple Values
Goal: Create a function that returns both the area and circumference of a circle given its radius.

Concept: Unlike many other programming languages, Python functions can return multiple distinct values at the exact same time. When a function returns multiple values, it technically returns them as a Tuple, which you can easily unpack into separate variables.
```
import math

def circle_stats(radius):
    # Area = π * r^2
    area = math.pi * (radius ** 2)
    
    # Circumference = 2 * π * r
    circumference = 2 * math.pi * radius
    
    # Return both values separated by a comma
    return area, circumference

# Unpacking the returned Tuple into two separate variables
a, c = circle_stats(3)
print("Area:", a, "Circumference:", c)
```

Problem 5: Default Parameter Value
Goal: Write a function that greets a user. If no name is provided, it should greet with a default name.
Concept: You can assign default values to parameters directly in the function definition. If the user calls the function but forgets to pass an argument, Python will automatically use the default value instead of crashing with a "missing argument" error.
```
# 'name' defaults to "User" if nothing is passed
def greet(name="User"):
    return "Hello " + name + "!"

# Scenario A: Passing a specific name
print(greet("Suraj")) # Outputs: Hello Suraj!

# Scenario B: Passing nothing
print(greet()) # Outputs: Hello User!
```

Problem 6: Lambda Functions (Anonymous Functions)
Goal: Create a lambda function to compute the cube of a number.
Concept: A ```lambda``` function is a shortcut for creating small, one-line functions without giving them a formal name (using ```def```). They are heavily used in frameworks (like Django) for quick, on-the-fly calculations where writing a full function definition would be overkill.
```
# The syntax: lambda arguments : expression
# We store the lambda function in a variable named 'cube'
cube = lambda x: x ** 3

# Using the lambda function:
print(cube(3)) # Outputs: 27
```

Problem 7: Handling Multiple Arguments (*args)
Goal: Write a function that takes a variable number of arguments and returns their sum.
Concept: What if you don't know how many numbers a user will pass? Using ```*args``` (the asterisk is the magic part, ```args``` is just the naming convention) tells Python to grab every single argument passed in and bundle them together into a Tuple. You can then loop through that Tuple.
```
# The '*' tells Python to gather all positional arguments into a Tuple
def sum_all(*args):
    # 'sum()' is a built-in Python function that adds up an iterable
    return sum(args) 
    
    # (Alternatively, you could manually write a 'for' loop to add them)

print(sum_all(1, 2))       # Outputs: 3
print(sum_all(1, 2, 3, 4)) # Outputs: 10
```

Problem 8: Keyword Arguments (```**kwargs```)
Goal: Create a function that accepts any number of keyword arguments and prints them in the format ```key: value```.

Concept: If ```*args``` gathers unnamed arguments into a Tuple, ```**kwargs``` (double asterisk) gathers named (keyword) arguments and bundles them into a Dictionary. This is incredibly useful when passing dynamic configurations or database entries.
```
# The '**' gathers all named arguments into a Dictionary
def print_kwargs(**kwargs):
    # Looping through a dictionary requires the .items() method
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# Using the function with arbitrary named arguments:
print_kwargs(name="Shaktiman", power="Lazer", enemy="Kilvish") 
# Outputs:
# name: Shaktiman
# power: Lazer
# enemy: Kilvish
```






