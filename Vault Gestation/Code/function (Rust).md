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


###### [[ownership (Rust)]] and Functions
The semantics for passing a value to a function are similar to those for assigning a value to a variable. Passing a variable to a function will move or copy, just as assignment does. Listing 4-3 has an example with some annotations showing where variables go into and out of scope.

Filename: src/main.rs

```rust
fn main() {
    let s = String::from("hello");  // s comes into scope

    takes_ownership(s);             // s's value moves into the function...
                                    // ... and so is no longer valid here

    let x = 5;                      // x comes into scope

    makes_copy(x);                  // x would move into the function,
                                    // but i32 is Copy, so it's okay to still
                                    // use x afterward

} // Here, x goes out of scope, then s. But because s's value was moved, nothing
  // special happens.

fn takes_ownership(some_string: String) { // some_string comes into scope
    println!("{}", some_string);
} // Here, some_string goes out of scope and `drop` is called. The backing
  // memory is freed.

fn makes_copy(some_integer: i32) { // some_integer comes into scope
    println!("{}", some_integer);
} // Here, some_integer goes out of scope. Nothing special happens.`` 
```
Listing 4-3: Functions with ownership and scope annotated

If we tried to use `s` after the call to `takes_ownership`, Rust would throw a compile-time error. These static checks protect us from mistakes. Try adding code to `main` that uses `s` and `x` to see where you can use them and where the ownership rules prevent you from doing so.

###### Return Values and Scope

Returning values can also transfer ownership. Listing 4-4 is an example with similar annotations to those in Listing 4-3.

```rust fn main() {
    let s1 = gives_ownership();         // gives_ownership moves its return
                                        // value into s1

    let s2 = String::from("hello");     // s2 comes into scope

    let s3 = takes_and_gives_back(s2);  // s2 is moved into
                                        // takes_and_gives_back, which also
                                        // moves its return value into s3
} // Here, s3 goes out of scope and is dropped. s2 goes out of scope but was
  // moved, so nothing happens. s1 goes out of scope and is dropped.

fn gives_ownership() -> String {             // gives_ownership will move its
                                             // return value into the function
                                             // that calls it

    let some_string = String::from("hello"); // some_string comes into scope

    some_string                              // some_string is returned and
                                             // moves out to the calling
                                             // function
}

// takes_and_gives_back will take a String and return one
fn takes_and_gives_back(a_string: String) -> String { // a_string comes into
                                                      // scope

    a_string  // a_string is returned and moves out to the calling function
}` 
```
Listing 4-4: Transferring ownership of return values

The ownership of a variable follows the same pattern every time: assigning a value to another variable moves it. When a variable that includes data on the heap goes out of scope, the value will be cleaned up by `drop` unless the data has been moved to be owned by another variable.


###### Properties:
- Rust does not care where you define functions, only that they are defined somewhere

###### Additional Thoughts:
