#languages/TypeScript #unique

In JavaScript/TypeScript, you can declare a function anywhere in scope, and the language will helpfully move the function to the top of the code block.

Some languages (PHP, Python) will throw a fit if you do that.

```typescript
function example() {

	return hoisted_function();

	// JavaScript will move this above
	//   the `return` statement.
	function hoisted_function() {
		return "lol";
	}
}

example();
> "lol"
```