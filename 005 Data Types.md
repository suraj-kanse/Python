Before diving deep into individual data types, you need a "bird's-eye view" of what tools Python offers. The core job of any program is to store data and compute it. If you don't know the exact "container" (data type) your data is sitting in, you won't know how to manipulate it. Note: In Python documentation, Data Types are often strictly referred to as "Object Types" because everything in Python is an object.

The 7 Core Python Data Types
The following are the mapped out the primary data types you will encounter daily.

1. Numbers
Python supports highly precise math out-of-the-box, unlike some other languages that require special libraries for large numbers.
- Integers (int): Standard whole numbers (1234).
- Floating Point (float): Decimal numbers (3.14).
- Complex Numbers (complex): Numbers with a real and imaginary part, represented by j instead of i (e.g., 3 + 4j).
- Exponents: To calculate powers, use double asterisks **. (e.g., 2 ** 4 means 2 to the power of 4). Python can effortlessly handle massive numbers like 2 ** 100 without crashing.
- Built-in Libraries: You can import math for things like math.pi, or import random to use random.random() and random.choice([1, 2, 3]) to pick a random item from a list.

2. Strings (str)
Strings handle text and can be defined using single quotes 'chai' or double quotes "chai".
- List-like Behavior: You can grab individual letters using brackets: username[0] returns the first letter. username[-1] returns the very last letter.
- Slicing: username[1:3] grabs letters starting at index 1 and stopping before index 3.
- Immutability Reminder: If you try to reassign a specific letter like username[0] = 'A', your program will crash with a TypeError. Strings are immutable; they do not support item assignment.

















