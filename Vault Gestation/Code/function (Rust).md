name : function (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Function definitions in Rust start with `fn` and have a set of parenthesis after the function name. The curly brackets tell the compiler where the function body begins and ends.

**Function Parameters**
Functions can be defined to have parameters, which are special variables that are part of the function's signature.
```rust
fn main() {
	another_function(5,6);
}

fn another_function(x: i32, y:i32) {
	println!("The value of x is: {}", x);
	println!("The value of y is: {}", y);
}
```
In function signatures, you **must** declare the type of each parameter. When you want a function to have multiple parameters, separate the parameter declarations with commas. The example function above takes two parameters, both of which are `i32` types.


**Return Values**
Functions can return values to the code that calls them. We don't name the return values, but we do declare their type after an `->`. In Rust, the return values of the function is synonymous with the value of the final expression in the block of the body of a function.
```rust
fn main() {
	let x = plus_one(5);
	println!("The value of x is: {}", x);
}

fn plus_one(x: i32) -> i32 {
	x+1 //notice the absence of a semicolon
}

```
You can return early from a function by using the `return` keyword and specifying a value, but most functions return the last expression implicitly. In the example above, since `x+1` is the last [[expression (Rust)]] in the function, it will be returned.

###### Properties:
- Rust does not care where you define functions, only that they are defined somewhere

###### Additional Thoughts:
