#languages/Ruby #concepts/array/frequency

Ruby arrays (which inherits `Enumerable`) have a built-in function that returns an associative array (or `Hash` in Ruby).

`array.tally` gives the frequency of elements.

```ruby
my_array = ["a","b","a","c","a"]

# `tally` is a method of *Enumerate*, not Array!
my_array.tally
> {"a"=>3, "b"=>1, "c"=>1}
```

`Enumerate.tally` is useful for finding [[Ruby str_to_chars|letter frequencies]].
## Read More
- [Enumerable.tally - Ruby Doc](https://www.rubydoc.info/stdlib/core/Enumerable:tally)
