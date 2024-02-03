#languages/Rust 

Rust has a unique primitive, `usize`. It behaves pretty much an `i32` but is used by for array indices and sizes of data structure.

IMHO it's pretty clever, although it'll regularly bite you with:

> expected `i32`, found `usize`

In Rust, it feels like 10% of my code is writing the word `as`.

> `array[x as usize]`
