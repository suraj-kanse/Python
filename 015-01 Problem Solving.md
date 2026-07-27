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

































