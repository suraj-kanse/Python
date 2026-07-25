Lists and Tuples are incredibly similar data structures—they both hold a sequence of items, they both support zero-based indexing, and they both support slicing.

So why do Tuples exist? Because they are Immutable.
Once you create a Tuple in memory, it is locked. You cannot add to it, remove from it, or change an item inside it. This provides a massive performance and memory optimization boost, making Tuples much faster than Lists. If you have data that should never change (like days of the week, or settings configurations), you should always store it in a Tuple, not a List.

Creating and Accessing Tuples
Tuples are defined using parentheses ```( )```, whereas Lists use square brackets ```[ ]```.
```
tea_types = ("Black", "Green", "Oolong")

# Accessing items (Exactly the same as a List)
print(tea_types[0])  # Outputs: "Black"
print(tea_types[-1]) # Outputs: "Oolong"

# Slicing (Exactly the same as a List)
print(tea_types[1:]) # Outputs: ('Green', 'Oolong')
```







































































