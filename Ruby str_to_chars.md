#languages/Ruby #concepts/string/char_array

Suggested to use `chars` over `split("")`.

```ruby
## faster and more robust
"abcdef".chars
> ["a","b","c","d","e","f"]

## regular expression split
"abcdef".split("")
> ["a","b","c","d","e","f"]
```

Useful for getting [[Ruby Array Frequency|letter frequencies]].

Read More
- https://stackoverflow.com/a/46442301