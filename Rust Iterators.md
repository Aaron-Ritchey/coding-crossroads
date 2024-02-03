#languages/Rust #concepts/iterator 

## Consult, Consume, Modify

A great response from "prog-fh" on Stack Overflow.
https://stackoverflow.com/a/70609138

>Use `array.iter().enumerate()` to [consult](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter) 
>Use `array.iter_mut().enumerate()` to [modify](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter_mut) (to modify)
>Use `array.into_iter().enumerate()` to [consume](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.into_iter)


Also, the docs:
https://doc.rust-lang.org/std/iter/index.html