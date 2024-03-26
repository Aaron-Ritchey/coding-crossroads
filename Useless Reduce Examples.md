#concepts/array/reduce 

A lot of website offer the following example for their language's `reduce` function.

```pseudocode
// This is equivalent to a "sum" function.
// This will return 15.
[1,2,3,4,5].reduce(
	function (x, y) {
		return x + y;
	},
	0
)
```

The problem with this code is they don't say what `x` and `y` are.

```pseudocode
// Will this return 30 or 129?
[1,2,3,4,5].reduce(
	function (x, y) {
		return 2*x + y;
	},
	0
)
```

## My Proposal
> This is my soapbox. There are many like it, but...

### 1. Useful variable names
It doesn't matter what. I once saw the phrases `accumulator` and `element` which stuck with me, which I abbreviate to `acc` and `ele` out of convenience.
```pseudocode
[1,2,3,4,5].reduce(
	function (acc, ele) {
		return acc + ele;
	},
	0
)
```

### 2. Emulate "max" instead of "sum"
TODO: okay, maybe max isn't any better. I want to suggest 2.1 instead, but that might be a lot more complicated.
```pseudocode
// This is equivalent to a "max" function instead of a "sum".
[2,4,6,0,1].reduce(
	function (x, y) {
		// 
		return (x > y) ? x : y;
	},
	0
)
```

### 2.1. Emulate "length of longest string in array"
This is a better example.
```pseudocode
["ich bin ein Berliner"].reduce(
	// While we still aren't being told what x and y are,
	//   we can read this lambda function and guess that
	//   "x" is an integer, and we return "y.length()"
	//   when it's bigger than "x". 
	function (x, y) {
		return (y.length() > x) ? y.length() : x;
	},
	0
)

```
