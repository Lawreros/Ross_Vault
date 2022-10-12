name : scope (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
A scope is the range within a program for which an item is valid. Let's say we have a variable that looks like this:
```rust
{
	let s = "hello";
}
```

The variable `s` refers to a string literal, where the vale of the string is hardcoded into the text of our program. The variable is valid from the point at which it's declared until the end of the current scope.

```rust
{
	let s = String::from("hello"); // s is valid from this point forward
	// do stuff with s
}		// this scope is now over, and s is no longer valid
```

In other words, there are two important points in time here:
- When `s` comes into scope, it is valid
- it remains valid until it goes out of scope.

###### Properties:

###### Additional Thoughts:
