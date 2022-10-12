name : loop ([[Rust]])
tags : 
backlinks : 
source : #TRPL 

###### Content:
The `loop` keyword tells Rust to execute a block of code over and over again forever or until you explicitly tell it to stop.

One of the uses of a `loop` is to retry an operation you know might fail, such as checking whether a thread has completed its job. However, you might need to pass the result of that operation to the rest of your code. To do this, you can add the value you want returned after the `break` expression you use to stop the loop; that value will be returned out of the loop so you can use it, as shown here:
```rust
fn main() {
	let mut counter = 0;
	
	let result = loop {
		counter += 1;
		
		if counter == 10 {
			break counter * 2; //multiplies counter by 2 before returning it
		}
	};
	
	println!("The result is {}", result); //will equal 20
}
```


###### Properties:
Unique relationships/properties

###### Additional Thoughts:
