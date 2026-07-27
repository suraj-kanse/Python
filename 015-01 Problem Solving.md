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







































