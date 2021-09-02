name : tuple (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
A tuple is a general way of grouping together a number of values with a variety of types into one compound type. Tuples have a fixed length and, once declared, they cannot grow or shrink in size.

```rust
fn main() {
	let tupy: (i32, f64, u8) = (500, 6.4, 1);
	let (x, y, z) = tupy;
	println!("The value of y is: {}", y);
}
```

Each position in the tuple has a type, and the types of the different values in the tuple don't have to be the same.

Tuple elements can be accessed directly by using a period (`.`) followed by the index of the value we want to access.
```rust
fn main() { 
	let x: (i32, f64, u8) = (500, 6.4, 1); 
	let five_hundred = x.0; 
	let six_point_four = x.1; 
	let one = x.2; 
}
```

###### Properties:
- The first index in a tuple is the `0` position
- Stored in the [[heap (Rust)]] instead of the [[stack (Rust)]]

###### Additional Thoughts:
