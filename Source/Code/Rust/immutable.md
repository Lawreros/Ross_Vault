name : immutable
tags : 
backlinks : 
source : #TRPL

###### Content:
A property of variables which states that, once a value is bound to a name/variable, you can't change the value. Opposite of [[mutable]]. This is done in order to minimize the memory requirements of your code by putting more things in the [[stack (Rust)]].

```rust
fn main() { 
	let x = 5;
	println!("The value of x is: {}", x);
	x = 6;
	println!("The value of x is: {}", x); 
}
```
^will not run compile due to the attempt to change the immutable x variable

**Useful Commands/Functions**

###### Properties:
- In rust, variables are immutable by default (best practice)
- If the variable in one part of the code is immutable, it's value will never change and other parts of the code will not be able to change it.

###### Additional Thoughts:
