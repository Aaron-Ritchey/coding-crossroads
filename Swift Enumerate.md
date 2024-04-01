#languages/Swift #concepts/enumerate 

```swift
for (i, row) in grid.enumerated() {
	for (j, cell) in row.enumerated() {
		// i = row
		// j = column
		// cell = value of cell
	}
}
```