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

````
number = 3

for i in range(1, 11):
    if i == 5:
        continue # Skips the rest of the code below and goes to i = 6
    print(number, 'x', i, '=', number * i)
````






















