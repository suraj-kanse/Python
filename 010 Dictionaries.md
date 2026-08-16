Lists are great when *order* matters (first, second, third). However, when order doesn't matter and you need to look up information by a specific name (like a user's age, first name, or email), you use a Dictionary. 
**Dictionaries** store data in **Key-Value pairs**, and they are incredibly fast for looking up data.

Creating and Accessing Dictionaries: 
Dictionaries are defined using curly braces ```{ }```. Every entry has a "Key" (the name) and a "Value" (the data), separated by a colon ```:```.
```
sports_types = {"cricket": "bat-ball-stump", "football": "team sport", "tennis": "racket-ball"}

# Accessing a value using Bracket Notation
print(sports_types["cricket"]) # Outputs: "bat-ball-stump"
```

Bracket Notation vs. The ```.get()``` Method:
What happens if you try to access a key that does not exist?
- Bracket Notation (```sports_types["carrom"]```): Python will crash and throw a ```KeyError```.
- The ```.get()``` Method (```sports_types.get("carrom")```): Python will safely return ```None``` without crashing your program.
- Industry Standard: Always use ```.get()``` when you aren't 100% sure the key exists (like when processing user input).

Modifying and Deleting Data:
Dictionaries are Mutable, meaning you can change them in-place.
- Update a value: ```sports_types["tennis"] = "tennis_rackets"``` (Changes the value of "tennis" from "racket-ball" to "tennis_rackets").
- Add a new Key-Value pair: ```sports_types["hockey"] = "hockey_stick-ball"``` (If the key doesn't exist, Python automatically adds it).
- ```.pop(key)```: Removes the specific key you ask for and returns its value. ```sports_types.pop("football")```.
- ```.popitem()```: Removes and returns the very last key-value pair added to the dictionary.
- ```del``` keyword: Physically deletes the item from memory. ```del sports_types["tennis"]```.
- ```.clear()```: Empties the entire dictionary, leaving it as ```{}```.

Looping Through Dictionaries (The 3 Ways):
Looping through a dictionary is slightly different than looping through a list because you have to decide if you want the Keys, the Values, or Both.

1. Looping for Keys (Default behavior)
```
for sport in sports_types:
    print(sport)
# Outputs: cricket, football, tennis (Only prints the Keys)
```

2. Looping for Values
```
for sport in sports_types:
    # Use the Key to access the Value
    print(sports_types[sport]) 
# Outputs: bat-ball-stump, team sport, racket-ball
```

3. Looping for Both (The ```.items()``` Method):
If you want both the Key and the Value at the same time, you must use the ```.items()``` method.
```
for key, value in sports_types.items():
    print(f"Key is {key} and Value is {value}")
```


Nested Dictionaries:

You can put dictionaries inside of dictionaries! This is heavily used when dealing with JSON data from APIs.
```
tea_shop = {
    "chai": {"masala": "spicy", "ginger": "zesty"},
    "tea": {"green": "mild", "black": "strong"}
}

# Accessing nested data (Chain the brackets!)
print(tea_shop["chai"]["ginger"]) # Outputs: "zesty"
```

Dictionary Comprehension:

Just like List Comprehension, you can generate dictionaries dynamically using a loop inside the curly braces.
```
# Create a dictionary where the Key is the number, and the Value is the number squared
squared_nums = {x: x**2 for x in range(6)}

print(squared_nums)
# Outputs: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

Dynamic Creation with ```fromkeys()```:

If you have a list of keys and want to create a dictionary where every key starts with the exact same default value, you use ```dict.fromkeys()```.
```
keys = ["masala", "ginger", "lemon"]
default_value = "delicious"

# Generates a new dictionary from the list
new_dict = dict.fromkeys(keys, default_value)

print(new_dict)
# Outputs: {'masala': 'delicious', 'ginger': 'delicious', 'lemon': 'delicious'}
```









