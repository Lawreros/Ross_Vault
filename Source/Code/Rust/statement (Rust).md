name : statement (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Statements are instructions that perform some action and do not return a value. Statements do not return values. Therefore, you can't assign a `let` statement to another variable as the following code tries to do; you'll get an error:
```rust
fn main() {
	let x = (let y = 6);
}
```
The `let` statement does not return a value, so there isn't anything for `x` to bind to.

###### Properties:
- [[function (Rust)]] definitions are also statements.

###### Additional Thoughts:
