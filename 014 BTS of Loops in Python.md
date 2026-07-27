To most developers, a loop is just a ```for``` or ```while``` statement. 
But in Python, iteration is a deeply reimagined system driven by three distinct components: Iterable Objects, Iterator Objects, and Iteration Tools. 
Understanding how Python traverses memory under the hood—specifically using ```iter()```, ```next()```, and handling the ```StopIteration``` exception—is essential for mastering file handling, generator design, and advanced data processing.

The Three Pillars of Python Iteration
Python breaks down iteration into three distinct actors:
```
[ Iteration Tool ] ──(1. Query / Request)──► [ Iterable Object ]
      ▲                                            │
      │                                     (2. Returns Iterator)
      │                                            ▼
      └─────────(3. Call next() until)─────── [ Iterator Object ]
                      StopIteration
```

- Iteration Tools: The mechanism that initiates and manages the loop.
  - Examples: ```for``` loops, List Comprehensions, ```map()```, generator expressions.
- Iterable Objects: Any object in memory that contains data that can be stepped through sequentially.
  - Examples: for loops, List Comprehensions, map(), generator expressions.
- Iterator Objects & Responses: The underlying memory pointers that track where you currently are in the loop and yield the next item when requested via ```__next__()``` or ```next()```.






























































