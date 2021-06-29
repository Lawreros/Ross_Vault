name : cargo build
tags : 
backlinks : 
source : [[The Rust Programming Language]]

###### Content:
Builds the project you are currently in by entering the following command:
`cargo build`

This command creates and executable file in *target/debug/projectname* rather than in your current directory.

Running `cargo build` for the first time also causes [[cargo]] to create a new file at the top level: [[Cargo.lock]].

**Useful Commands/Functions**
- When your project is ready for release, use `cargo build --release` to compile it with optimizations. This will create an executable in *target/release*.

###### Properties:

###### Additional Thoughts:
