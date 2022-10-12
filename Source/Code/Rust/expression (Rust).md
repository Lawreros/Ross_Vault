name : expression (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Expressions are instructions that perform some action and evaluate to a resulting value. Expression evaluate to something and make up most of the code that you'll write.

```rust
fn main() {
	let x = 5;
	let y = {
		let x = 3;
		x + 1
	}; //block of code that evaluates to 4, the value which then gets bound to y
	
	println!("The value of y is:  {}", y);
}
```
Expressions can be part of statements, the `6` in the [[statement (Rust)]] `let y = 6;` is an expression that evaluates to the value `6`.
Expressions do not include ending semicolons. If you add a semicolon to the end of an expression, you turn it into a statement, which will then not return a value.


###### Properties:
- Calling a [[function (Rust)]] is an expression
- Calling a [[macro]] is an expression

###### Additional Thoughts:
