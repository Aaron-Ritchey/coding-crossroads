#languages/CPP #concepts/loops/foreach

 ```
for (auto&& num : nums) {
    ...
}
```

The `auto&& num` has something to do with pointers and "deduction". The documentation says: "*It is \[safe and preferable] to use deduction.*" See the docs below.

Using `auto&&` (or `auto&`) will let you modify the value of that element. Using just `auto` creates a copy of that element. And supposedly in simple cases, it doesn't matter if you use `auto` or `auto&` because compilers can optimize in simple cases.

In all cases of `auto` or `auto&` or `auto&&`, the `auto` says "set `num` as whatever type `nums` is.

https://en.cppreference.com/w/cpp/language/range-for