#languages/Swift #concepts/map-function 

Using `.forEach` won't return an array.

```swift
var best_in_column = matrix.reduce(
	Array(repeating: -1, count: matrix.count), { acc, ele in
		zip(acc, ele).map {
			accX, eleX in
			max(accX, eleX);
		}
	}
);

// Using ...anonymous variables?
var best_in_column = matrix.reduce(
	Array(repeating: -1, count: matrix.count), {
		zip($0, $1).map {
			max($0, $1);
		}
	}
);
```