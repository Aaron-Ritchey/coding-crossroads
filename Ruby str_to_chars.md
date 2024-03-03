#languages/Ruby #concepts/string/char_array

Using `.chars` is the better way of splitting a string into an array.

```ruby
## faster and more robust
"abcdef".chars
> ["a","b","c","d","e","f"]

## using a regex-powered split
"abcdef".split("")
> ["a","b","c","d","e","f"]
```

From here, you can use [[Ruby Array Frequency|Enumerable.tally]] to get the frequency of array elements.
## Read More
- [Split vs. Chars - Stack Overflow](https://stackoverflow.com/a/46442301)