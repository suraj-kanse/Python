To pass interviews at top-tier companies, you cannot simply know Python's syntax; you must understand its foundation. Python handles memory dynamically through Object References and Garbage Collection. Misunderstanding how Python assigns memory (especially when dealing with Lists and Slicing) is the #1 cause of bugs in Data Science and high-end software development.

The Reference Count (How Python Tracks Memory)

When you assign a variable (e.g., ```score = 10```), Python creates a memory object for ```10``` and points ```score``` to it. But what happens if you point three variables to that same 10?
- Python keeps a hidden tally called the Reference Count for every object in memory.
- If ```a = 10```, ```b = 10```, and ```c = 10```, the reference count for the ```10``` memory object is ```3```.
- Garbage Collection: If you delete all those variables (or reassign them), the reference count drops to ```0```. Python's internal Garbage Collector immediately sweeps in, deletes the object, and frees up your RAM.
- The "Number & String" Exception: Python knows you will use small numbers and common strings frequently. To optimize performance, Python delays the garbage collection for small numbers and strings, keeping them cached in memory just in case you need them again soon.









































