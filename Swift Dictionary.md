#languages/Swift #structures/dictionary 

## Initialize
```swift
// How to create a basic Counter object.
var counter = [String : Int]();

// A dictionary which gathers words.
var word_groups = [String : [String]]();
```

## Autovivification
```swift
if counter[letter] == nil { counter[letter] = 0 };

if word_groups[key] == nil { word_groups[key] = [] };
```

## Get
```swift
// Returns an Optional(Int)
// This needs to be "unwrapped" I think.
var x = counter['word'];

// Returns an Int. (Or might die trying.)
var x = counter['word']?;

// Return _with_ your Int, or _on_ it.
// (I'm not sure if this right, I just wanted the reference.)
var x = counter['word']!;
```
## Append to Value
```swift
result[key].append(word);
> error: value of optional type '[String]?' must be unwrapped to refer to member 'append' of wrapped base type '[String]'

result[key]?.append(word);
> OK
```

## Returning Values as an Array
In Swift, `Dictioanry.values` does not return an array, it returns a `Collection`. (Looks like it's good for lazily iterating over the values.) So we have to coerce it into an array.

```swift
// This won't work.
return counter.values;
> "error: cannot convert return expression of type 'Dictionary<String, Int>.Values' to return type '[Int]'"

// Do this instead.
return Array(counter.values);
> "OK"
```

## Read More
- [Dictionary.Values - Swift Docs](https://developer.apple.com/documentation/swift/dictionary/values-swift.struct)
	- This is not an `Array`, it's a `Collection`.
- [Swift Dictionary Quick Reference - Coding Explorer Blog](https://www.codingexplorer.com/swift-dictionary-quick-reference/)
- [A Good Response on Stack Overflow](https://stackoverflow.com/a/27769314)