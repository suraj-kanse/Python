Lists (often called Arrays in other languages) are the most heavily used data structure in Python. They allow you to store multiple items in a single, mutable container. Mastering how to slice them, modify them in-place, and generate them dynamically (using List Comprehensions) is an absolute must for any Python developer.

Creating and Accessing Lists
Lists are defined using square brackets ```[ ]```. They are zero-indexed, meaning the first item is at index ```0```.
```
tea_varieties = ["Black", "Green", "Oolong", "White"]

# Accessing items
print(tea_varieties[0])  # Outputs: "Black"
print(tea_varieties[-1]) # Outputs: "White" (Negative indexing grabs from the end)
```

Slicing Lists ```[start:stop:hop]```
Just like strings, you can slice a list. The ```stop``` index is never included in the final output.
- ```tea_varieties[1:3]``` ➔ ```['Green', 'Oolong']``` (Starts at 1, stops before 3).
- ```tea_varieties[1:]``` ➔ Grabs everything from index 1 to the end.
- ```tea_varieties[:2]``` ➔ Grabs everything from the start, stopping before index 2.




















































