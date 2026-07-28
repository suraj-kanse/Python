Scope determines where your variables live and who has access to them. Think of Scope like a house. If you create a variable out in the open (Global Scope), everyone can see it. If you create a variable inside a function (Local Scope), it is locked inside that "house."

Understanding this hierarchy, and what happens when a function "packs its bags" to leave the house (Closures), separates junior developers from senior engineers.

The Scope Hierarchy (The House Analogy)
In Python, whenever you indent code (like inside a ```def``` function or an ```if``` block), you are creating a new Scope.
- Global Scope (The World): Variables defined at the top level of your file without indentation.
- Local Scope (The House): Variables defined inside a specific function.

The Golden Rule of Scope Access:










