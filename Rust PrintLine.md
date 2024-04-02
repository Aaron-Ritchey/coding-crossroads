#languages/Rust #concepts/print

In Rust, you use the [[Rust Macro]] `println` to print text.

## Printing Strings
```rust
// Nothing exciting.
println!("Just a string.");
> Just a string.

// Ignore "{:?}" for the moment, it's convenient
//   but not what you want.
let location = "World";
println!("Hello {}", location);
> Hello World.
println!("Hello {0}", location);
> Hello World.
```
## Printing Other Things
A lot of answers point to "*use `{:?}` for All The Things!*" But since you're here, you want to know the minutiae of this.

`{0}` -- print the first argument, nothing exciting.

`{0:?}` -- print the `Debug` version of the first argument, which is usually a human-friendly representation of the object.

The `:` divides `0` and `?`.

`{}` -- print the "FAHP" (first argument we haven't printed) with `{}` (TODO: explain this better, while keeping the double entendre)

`{:?}` -- print the `Debug` version of "FAHP"

```rust
// Not quite what we want.
// `:` says "pick the next"
let location = "World";
// Explicitly print first argument.
println!("Hello {0:?}", location);
> Hello "World".

// Implicitly print first argument.
// But explicitly FAHPs.
println!("Hello {:?}", location);
> Hello "World".

// A lot of coders will FAHP instead
// of being explicit about what
// they're throwing onto the screen.
```
## Read More
- [Position Parameters for Formatted Strings - Rust Docs](https://doc.rust-lang.org/std/fmt/index.html#positional-parameters)