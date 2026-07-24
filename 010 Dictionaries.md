Lists are great when *order* matters (first, second, third). However, when order doesn't matter and you need to look up information by a specific name (like a user's age, first name, or email), you use a Dictionary. 
**Dictionaries** store data in **Key-Value pairs**, and they are incredibly fast for looking up data.

Creating and Accessing Dictionaries
Dictionaries are defined using curly braces ```{ }```. Every entry has a "Key" (the name) and a "Value" (the data), separated by a colon ```:```.
```
chai_types = {"masala": "spicy", "ginger": "zesty", "green": "mild"}

# Accessing a value using Bracket Notation
print(chai_types["masala"]) # Outputs: "spicy"
```

⚠️ Bracket Notation vs. The ```.get()``` Method
What happens if you try to access a key that does not exist?
- Bracket Notation (```chai_types["lemon"]```): Python will crash and throw a ```KeyError```.
- The ```.get()``` Method (```chai_types.get("lemon")```): Python will safely return ```None``` without crashing your program.
- Industry Standard: Always use ```.get()``` when you aren't 100% sure the key exists (like when processing user input).

































