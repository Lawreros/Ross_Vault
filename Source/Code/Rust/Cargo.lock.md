name : Cargo.lock
tags : 
backlinks : 
source : [[The Rust Programming Language]]

###### Content:
This file is created when running either [[cargo build]] or [[cargo new]]. It keeps track of the exact versions of dependencies in the project being built. You will never have to change this file manually; Cargo manages its contents for you.

**Useful Commands/Functions**
- `cargo update` will ignore the Cargo.lock file and figure out all the latest versions that fit your specifications in [[Cargo.toml]]. If that works, Cargo will write those versions to the Cargo.lock file.
		- If `0.6.1`, will only update to `0.6.9`. To go to `0.7.x` you will have to manually change your Cargo.toml file

###### Properties:


###### Additional Thoughts:
