#languages/Rust 

Rust has various "macros" available. They can be recognized by the `!` symbol.

While a macro might look like a function, there are subtle differences. If you're new to Rust, learn to use the common ones first. If you're new to macros, there are plenty of articles about "functions vs macros", of which I have no particular suggestion at the moment.
## Examples

```rust
// Create an Vector of ten zeroes.
vec![0; 10]
```

Your standard [[Rust PrintLine|print message]].

```rust
// Print a message to standard out
println!("message")
```

Your standard [[Rust Panic|throw statement]]

```rust
// Throw an error.
panic!("no~~~~~~")
```