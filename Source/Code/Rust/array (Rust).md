name : array (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
An array is a general way of grouping together a number of values. Unlike a [[tuple (Rust)]], every element of an array must have the same type. Arrays have a fixed length and, once declared, cannot grow or shrink in size.

```rust
fn main() {
// When type is not defined, uses default settings
let a = [1, 2, 3, 4, 5];

let months = ["January", "February", "March", "April", "May", "June", "July","August", "September", "October", "November", "December"];
// declare the data types of the entries in the array
let a: [i32; 5] = [1, 2, 3, 4, 5];
// make an array with 3 repeated 5 times
let a = [3; 5];
}
```

You can access elements of an array using indexing, like this:
```rust
fn main() {
    let a = [1, 2, 3, 4, 5];

    let first = a[0];
    let second = a[1];
}
```

###### Properties:
- The first index in a tuple is the `0` position
- Stored in the [[stack (Rust)]]

###### Additional Thoughts:
