name : mutable, `mut`
tags : 
backlinks : 
source : #TRPL

###### Content:
A property of variables which states that, once a value is bound to a name/variable, it is able to be changed. Opposite of [[immutable]].

```rust
fn main() { 
	let mut x = 5; 
	println!("The value of x is: {}", x); 
	x = 6; 
	println!("The value of x is: {}", x); 
}
```

**Useful Commands/Functions**
- `mut` placed after `let` makes the declared variable mutable

###### Properties:
- You cannot change the type of a mutable variable. Meaning that if it was declared as a string, it cannot have it's value changed to an integer.
```rust
	let mut spaces = "   ";
	spaces = spaces.len();
```


###### Additional Thoughts:
