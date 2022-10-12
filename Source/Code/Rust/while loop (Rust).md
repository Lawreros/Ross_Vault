name : while loop (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Similar to [[loop (Rust)]], the `while` loop is a built-in language construct which combines `loop`, `if`, `else`, and `break`.

```rust
fn main() {
	let mut number = 3;
	
	while number != 0 {
		println!("{}!", number);
		
		number -= 1;
	}
	
	println!("LIFTOFF!!!");
}
```

###### Properties:


###### Additional Thoughts:
