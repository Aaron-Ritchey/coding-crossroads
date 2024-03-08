#languages/Rust #concepts/primitives #unique 

Rust has a unique primitive, `usize`. It behaves pretty much an `i32` except is used for array indices and sizes of data structure.

IMHO it's pretty clever, although it'll regularly bite you with the following error:

> `expected "i32", found "usize"`

To address this, you can cast values to `usize` to get an element from an array.

> `array[x as usize]`

In Rust, it feels like 10% of my code is writing the word `as`.
