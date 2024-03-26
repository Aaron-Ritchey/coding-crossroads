#languages/Ruby #concepts/array/reduce

```ruby
## Get the word count for the bullet point with the most words.
bulllet_points.reduce(0) {
	| acc, ele |
	acc > ele.split.count ? acc : ele.split.count
}
```
## See also
- [[Useless Reduce Examples]]