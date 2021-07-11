name : floating-point (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Rust has two primitive types for floating-point numbers, which are numbers with decimal points. These are:
- `f32` for 32 bits
- `f64` for 64 bits

```rust
fn main() { 
	let x = 2.0; // f64
	let y: f32 = 3.0; // f32
}
```

###### Properties:
- Floating-point numbers are represented according to the IEE-754 standard
- `f32` type is a single-precision float while `f64` has double precision

###### Additional Thoughts:
