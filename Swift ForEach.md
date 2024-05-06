#languages/Swift #concepts/loops/foreach #concepts/loops/for-in 

There are multiple ways to iterate over the array.
## Example: "How many numbers are odd?"
All of the examples will illustrate this as a simple example.
```swift
let nums = [1,2,3,4,5,6,7];
var found = 0;

//--------------------------//
// <code snippet goes here> //
//--------------------------//

// Do something with the number.
print(found)
> 4 (1,3,5,7)
```
## array.forEach
The lambda/closure way.
- Cannot `continue` or `break`.
	- *"There is no escape."*
```swift
// The standard way.
nums.forEach { num in
	if (num % 2 == 1) {
		found += 1;
	}
}

// Using "shorthand argument names".
nums.forEach {
	if ($0 % 2 == 1) {
		found += 1;
	}
}
```
## for ... in
The traditional way.

**Gotcha:** wrapping it in parenthesis will cause an error. While you're allowed to use explicit parenthesis in most places, it's not allowed here.

```swift
// The Right Way
for num in nums {
	if (num % 2 == 1) {
		found += 1;
	}
}

// The Wrong Way
for (num in nums) {
	if (num % 2 == 1) {
		found += 1;
	}
}

/*
> error: expected ',' separator in solution.swift
> for (num in nums)
>          ^
*/
```
## for i in range
For completeness, here's how to iterate using a [[Swift Range]].

**Gotcha:** there are two gotchas; to avoid them, remember to start with `0..<`
```swift
// CORRECT:
for i in 0..<nums.count {
    var num = nums[i];
	if (num % 2 == 1) {
		found += 1;
	}
}

// WRONG:
// "error: cannot find operator '..' in scope"
for i in 0..nums.count {
    var num = nums[i];
	if (num % 2 == 1) {
		found += 1;
	}
}

// WRONG:
// "Program crashed: Illegal instruction"
for i in 0...nums.count {
    var num = nums[i];
	if (num % 2 == 1) {
		found += 1;
	}
}

```
## Read More
- [forEach(\_:) - Swift Docs](https://developer.apple.com/documentation/swift/sequence/foreach(_:))
	- [Closures - Swift Docs](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/closures/)
- [For-in loops - Swift Docs](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/controlflow/)
	- [Explicit Parenthesis - Swift Docs](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/basicoperators/#Explicit-Parentheses)