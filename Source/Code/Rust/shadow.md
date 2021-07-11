name : shadow
tags : 
backlinks : 
source : #TRPL 

###### Content:
When a new variable is declared using the same name as a previous variable. Rustaceans say that the first variable is *shadowed* by the second. In the example below, the program first binds `x` to a value of `5`. Then it shadows `x` by repeating `let x =`, taking the original value and adding `1` so the value of `x` is then `6`, etc.

```rust
fn main() { 
	let x = 5;
	let x = x + 1;
	let x = x * 2;
	println!("The value of x is: {}", x);
}
```

**Useful Commands/Functions**

###### Properties:


###### Additional Thoughts:
