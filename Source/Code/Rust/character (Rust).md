name : character (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
Rust’s `char` type is four bytes in size and represents a Unicode Scalar Value, which means it can represent a lot more than just ASCII. The `char` type is the language's most primitive alphabetic type. Accented letters; Chinese, Japanese, and Korean characters; emoji; and zero-width spaces are all valid `char` values in Rust.

```rust
fn main() { 
	let c = 'z'; 
	let z = 'ℤ'; 
	let heart_eyed_cat = '😻'; 
}
```

###### Properties:
- `char` literals are specified with single quotes, as opposed to string literals, which use double quotes.

###### Additional Thoughts:
