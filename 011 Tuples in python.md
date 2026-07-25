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

The Immutability Check (The Fatal Error)
Because Tuples are immutable, they do not support item assignment.
```
# THIS WILL CRASH YOUR PROGRAM
tea_types[0] = "Lemon" 
# TypeError: 'tuple' object does not support item assignment
```
- Note: Because you cannot alter them, Tuples DO NOT have methods like ```.append()```, ```.remove()```, ```.pop()```, or ```.insert()```. Those belong strictly to Lists.


What CAN you do with a Tuple?
Even though you can't mutate an existing Tuple, you can perform analytical operations on it or create brand new Tuples out of it.
- Check Length: ```len(tea_types)``` returns ```3```.
- Concatenation (Merging): You can add two Tuples together to create a brand new third Tuple.
```
more_tea = ("Herbal", "Earl Grey")
all_tea = tea_types + more_tea
# all_tea is now ('Black', 'Green', 'Oolong', 'Herbal', 'Earl Grey')
```
- Count Items: ```tea_types.count("Green")``` will scan the Tuple and return how many times "Green" appears (returns ```1```). If the item doesn't exist, it returns ```0```.
- Conditional Checks: You can ask if an item exists inside the Tuple.
```
if "Green" in tea_types:
    print("I have Green tea")
```

Tuple Unwrapping (The Interview Essential)
This is an incredibly common operation in Python, especially when dealing with data coming back from a database (databases frequently return data as Tuples to ensure it hasn't been altered).
Tuple Unpacking allows you to extract all the items in a Tuple and assign them to individual variables in a single, clean line of code.
```
# Our Tuple has 3 items
tea_types = ("Black", "Green", "Oolong")

# We create 3 separate variables on the left side, matching the number of items
black, green, oolong = tea_types

# The variables are now populated with the strings!
print(green) # Outputs: "Green"
```

The Unpacking Rule: The number of variables on the left side of the equals sign must exactly match the number of items inside the Tuple on the right side. If they don't match, Python will throw a ```ValueError``` ("too many values to unpack" or "not enough values to unpack").

Nested Tuples
Just like Lists, you can put Tuples inside of other Tuples.
```
nested_tuple = ("Black", (1, 2, 3), "Oolong")
```

🔍 Checking the Data Type
If you are ever unsure whether a variable is holding a List or a Tuple, you can check it dynamically using the type() function.
```
print(type(tea_types)) 
# Outputs: <class 'tuple'>
```

Summary & Takeaways
- Tuples = ```( )```. They are exactly like Lists, but they are Immutable (locked in memory).
- Performance: Because they are immutable, Tuples are more memory-efficient and faster than Lists.
- No Mutation: You cannot use ```.append()```, ```.pop()```, or reassign indexes (```tup[0] = "new"```).
- Concatenation: You can merge two Tuples (```tup1 + tup2```), but this creates a brand new Tuple in memory.
- Tuple Unpacking: You can quickly assign Tuple data to individual variables: ```var1, var2 = ("item1", "item2")```. The number of variables must perfectly match the length of the Tuple.









































