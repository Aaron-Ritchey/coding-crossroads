#languages/Rust #concepts/exception

> *"Sometimes, bad things happen in your code, and there’s nothing you can do about it."* [Rust Docs](https://doc.rust-lang.org/book/ch09-01-unrecoverable-errors-with-panic.html)

Rust does not throw exceptions. It **panics**.

```rust
panic!("You dun goof'd.")
```

Note: this isn't a function, it's a [[Rust Macro|macro]]. While that's nothing you need to worry about when you're using it, keep in mind that `!` means its a macro.