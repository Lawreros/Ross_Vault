name : for loop (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
As a more concise alternative to [[loop (Rust)]] and [[while loop (Rust)]], the `for` loop can be used to execute code for each item in a collection.

```rust
fn main() {
	let a = [10, 20, 30, 40, 50];
	
	for element in a.iter() {
		println!("the value is: {}", element);
	}
}
```

`rev` reverses the order:
```rust
fn main() {
	for number in (1..4).rev() {
		println!("{}!", number);
	}
	println!("LIFTOFF!!!")
}
```


###### Properties:
- Much more stable than trying to replicate these examples with `while` and `loop`.  It’s also slow to use `while` and `loop`, because the compiler adds runtime code to perform the conditional check on every element on every iteration through the loop.

###### Additional Thoughts:
