#languages/Swift #concepts/loops/for-in

This is different from [[Swift Foreach]].

Be careful how to create a for-each loop. Wrapping it in parenthesis will cause an error.

```swift
// The Right Way
for word in words {
	...
}

// The Wrong Way
for (word in words) {
	...
}
> "error: expected ',' separator"
```

## Read More
- [forEach(\_:) - Swift Docs](https://developer.apple.com/documentation/swift/sequence/foreach(_:))