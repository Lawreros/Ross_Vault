name : constant (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Like [[immutable]], constants are values that are bound to a name and are not allowed to change.

```rust
const MAX_Points: u32 = 100
```

**Useful Commands/Functions**
- `const` keyword

###### Properties:
- The type of value *must* be annotated during the creation of the constant
- Constants can be declared in any [[scope (Rust)]], including the [[global scope]]
- Constants *must* be set only to a constant expression, not the result of a function call or any other value that could only be computed at runtime.

###### Additional Thoughts:
