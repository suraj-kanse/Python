Loops (Iteration) allow you to repeat a block of code continuously. 
While Python's loop syntax is simple, the internal mechanics of how Python handles iterables (behind the scenes) are actually quite different from languages like C++ or Java. 
To master Python, you must first get comfortable writing basic ```for``` and ```while``` loops before diving into the internal memory mechanics.

The ```for``` Loop
The ```for``` loop is primarily used to iterate over a sequence (like a List, String, or Range).

Problem 1: Counting Positive Numbers
Goal: Given a list of numbers, count how many are positive.
```
numbers = [1, -2, 3, -4, 5, 6, -7, -8, 9, 10]
positive_number_count = 0

for num in numbers:
    if num > 0:
        positive_number_count += 1 

print("Final Count:", positive_number_count)
```

Problem 2: Sum of Even Numbers up to ```n```
Goal: Calculate the sum of all even numbers up to a given number ```n```.
```
n = 10
sum_even = 0

# The range must be n + 1 because the stop value is exclusive.
for i in range(1, n + 1):
    if i % 2 == 0:
        sum_even += i

print("Sum of even numbers:", sum_even)
```

Loop Control Keywords (```continue``` and ```break```)
Sometimes you need to skip a specific loop iteration or stop the loop entirely.

Problem 3: Skip an Iteration (```continue```)
Goal: Print the multiplication table for ```3```, but skip the 5th iteration.
- ```continue```: Immediately stops the current loop iteration and jumps to the next one.
```
number = 3

for i in range(1, 11):
    if i == 5:
        continue # Skips the rest of the code below and goes to i = 6
    print(number, 'x', i, '=', number * i)
```

Problem 4: Reverse a String using a Loop
Goal: Reverse a string without using built-in string methods or slicing.
```
input_string = "Python"
reversed_string = ""

for char in input_string:
    # Adding the new character IN FRONT of the existing string reverses it
    reversed_string = char + reversed_string 

print(reversed_string) # Outputs: nohtyP
```

Problem 5: Find the First Non-Repeated Character (```break```)
Goal: Given a string, find the very first character that does not repeat.
- ```break```: Immediately destroys the loop completely. No further iterations will occur.
```
input_string = "teeter"

for char in input_string:
    if input_string.count(char) == 1:
        print("First non-repeated char is:", char)
        break # We found it! Stop searching immediately.
```

The ```while``` Loop
A ```while``` loop runs continuously as long as a specific condition remains ```True```.

Problem 6: Calculate Factorial
Goal: Calculate the factorial of a number using a ```while``` loop (e.g., 5! = 5 * 4 * 3 * 2 * 1).
- Interview Tip: Don't get trapped thinking you have to use Recursion (a function calling itself) just because an interviewer asks for a factorial. Stick to the requirements—if they ask for a ```while``` loop, write a ```while``` loop.
```
number = 5
factorial = 1

while number > 0:
    factorial *= number
    number -= 1 # Decrement the number so the loop eventually stops

print("Factorial is:", factorial)
```

Problem 7: Validate User Input (The Infinite Loop)
Goal: Keep asking the user for input until they provide a number between 1 and 10.
- ```while True```: creates an intentional infinite loop. The only way out is to trigger a ```break```.
```
while True:
    user_input = int(input("Enter value between 1 and 10: "))
    # Python allows chained comparisons!
    if 1 <= user_input <= 10:
        print("Thanks!")
        break
    else:
        print("Invalid number, try again.")
```
