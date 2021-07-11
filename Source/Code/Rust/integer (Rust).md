name : integer (Rust)
tags : 
backlinks : 
source : #TRPL 

###### Content:
An *integer* is a number without a fractional component. The types of integer values are:

| Length  | Signed  | Unsigned |
| ------- | ------- | -------- |
| 8-bit   | `i8`    | `u8`     |
| 16-bit  | `i16`   | `u16`    |
| 32-bit  | `i32`   | `u32`    |
| 64-bit  | `i64`   | `u64`    |
| 128-bit | `i128`  | `u128`   |
| arch    | `isize` | `usize`  | 

Each variant can be either signed or unsigned and has an explicit size. Signed and unsigned refer to whether it's possible for the number to be negative.
Additionally, the `isize` and `usize` types depend on the kind of computer your program is running on: 64 bits for 64-bit architecture and 32 bits for 32-bit architecture.

You can write integer literals in any of the forms shown in Table 3-2. Note that all number literals except the byte literal allow a type suffix, such as `57u8`, and `_` as a visual separator, such as `1_000`.

| Number literals | Example       |
| --------------- | ------------- |
| Decimal         | `98_222`      |
| Hex             | `0xff`        |
| Octal           | `0o77`        |
| Binary          | `0b1111_0000` |
| Byte(`u8` only) | `b'A'`        |


###### Properties:
- Rust's integer types default to `i32`, which is generally the fastest
- The primary situation in which you'd use `isize` or `usize` is when indexing some sort of collection.

###### Additional Thoughts:
