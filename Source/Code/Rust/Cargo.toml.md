name : Cargo.toml
tags : 
backlinks : 
source : [[The Rust Programming Language]]

###### Content:
A file which contains the configuration information [[cargo]] needs to compile a program: the name, the version, who wrote it, and the edition of Rust to use. This file is in TOML format.

```rust
[package]
name = "hello_cargo"
version = "0.1.0"
authors = ["Your Name <you@example.com>"]
edition = "2018"

[dependencies]
```
The first line, `[package]`, is a section heading that indicates that the following statements are configuring a package.

The last line, `[dependencies]`, is the start of a section for you to list any of your project’s dependencies. In Rust, packages of code are referred to as [[crate]]s. 

**Useful Commands/Functions**

###### Properties:
- [[cargo]] expects your source files to live inside the *src* directory.

###### Additional Thoughts:
