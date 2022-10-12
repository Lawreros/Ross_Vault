name : else if ([[Rust]])
tags : 
backlinks : 
source : #TRPL 

###### Content:
All `if` expressions start with the keyword `if`, which is followed by a condition. The block of code you want to execute if the condition is true is placed immediately after the condition inside of the curly brackets. 
Optionally, we can also include an `else` expression, which we choose to do here, to give the program an alternative block of code to execute should the condition evaluate to false. If you don't provide an `else` expression and the condition is false, the program will just skip the `if` block and move on to the next bit of code.

```rust
fn main() {
	let number = 6;
	
	if number % 4 == 0 {
		println!("number is divisible by 4");
	} else if number % 3 == 0 {
		println!("number is divisible by 3");
	} else if number % 2 == 0 {
		println!("number is divisible by 2");
	} else {
		println!("number is not divisible by 4, 3, or 2");
	}
}
```

It is worth noting that the condition must be a `bool` in order to do an `if` statement like this:
```rust
if var_1 {
	println!("var_1 is true")
}
```
as rust will not automatically try to convert non-Boolean types to a Boolean.

**Using if in a let Statement**
Because `if` is an [[expression (Rust)]], you can use it on the right side of a `let` statement:
```rust
fn main() {
	let condition = true;
	let number = if condition { 5 } else { 6 };
	
	println!("The value of number is: {}", number);
}
```
the values that have the potential to be results from each arm of the `if` must be the same type. If the types are mismatched we’ll get an error.

###### Properties:
- Blocks of code associated with the conditions in `if` expressions are sometimes called *arms*.
- Rust only executes the block for the first true condition, and once it finds one, it doesn't even check the rest.

###### Additional Thoughts:
