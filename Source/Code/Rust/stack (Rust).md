name : stack (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
A part of memory that is available for code to use at runtime. All data stored on the stack must have a known, fixed size. Data with an unknown size at compile time or a size that might change must be stored on the [[heap (Rust)]] instead.
The stack stores values in the order it gets them and removes the values in the opposite order (*last in, first out*). Think of a stack of plates: when you add more plates, you put them on top of the pile, and when you need a plate, you take off the top. Adding data is called *pushing onto the stack*, and removing data is called *popping off the stack*.

###### Properties:
- Pushing to the stack is faster than allocating on the heap because the allocator never has to search fro a place to store new data; that location is always at the top of the stack.
- Ideally you want most things in the stack instead of the heap.
- When your code calls a [[function (Rust)]], the values passed into the function (including, potentially, pointers to data on the [[heap (Rust)]]) and the function's local variables get pushed onto the stack. When the function is over, those values get popped off the stack.

###### Additional Thoughts:
