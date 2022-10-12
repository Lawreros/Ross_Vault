name : heap (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
A part of memory that is available for code to use at runtime. Data with an unknown size at compile time or a size that might change must be stored on the [[heap (Rust)]] instead of the [[stack (Rust)]].
The heap is less organized: when you put data on the heap, you request a certain amount of space. The memory allocator finds an empty spot in the heap that is big enough, marks it as being in use, and returns a [[pointer (Rust)]]. This process is called *allocating on the heap* and is sometimes abbreviated as just *allocating*. Because the pointer is a known, fixed size, you can store the pointer on the [[stack (Rust)]].

###### Properties:
- Allocating space on the heap requires more work, because the allocator must first find a big enough space to hold the data and then perform bookkeeping to prepare for the next allocation.
- Accessing data in the heap is slower than accessing data on the stack because you have to follow a pointer to get there. Contemporary processors are faster if they jump around less in memory.

###### Additional Thoughts:
