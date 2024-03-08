#languages/Rust #concepts/iterator 

Rust has three forms of iterators.

The rust documentation (see Read More) explains what the three iterators are.
## Consult, Consume, Modify
User "*prog-fh*" on Stack Overflow gives a great explanation of [the three types of Rust iterators](https://stackoverflow.com/a/70609138).

>Use `array.iter().enumerate()` to [consult](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter) 
>Use `array.iter_mut().enumerate()` to [modify](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter_mut)
>Use `array.into_iter().enumerate()` to [consume](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.into_iter)

Using this idea to think of what you're doing with an array of data is pretty interesting.
## Read More
- [Iterator Module - Rust Docs](https://doc.rust-lang.org/std/iter/index.html)