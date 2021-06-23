name : cargo new
tags : 
backlinks : 
source : [[The Rust Programming Language]]

###### Content:
`cargo new <project name>` from a given directory will create a new directory called `<project name>`. This will generate two files and one directory: a [[Cargo.toml]] file and a *src* directory with a *main.rs* file inside.

This will also initialize a new Github repository along with a *.gitignore* file. Git files won't be generated if you run `cargo new` within an existing Git repository; you can override this behavior by using `cargo new --vcs=git`

**Useful Commands/Functions**

###### Properties:

###### Additional Thoughts:
