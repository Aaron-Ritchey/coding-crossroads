#languages/TypeScript #concepts/foreach #concepts/loops/for-in

There are multiple ways to iterate over an array in TypeScript.
## for ... of
```typescript
for (let num of nums) {
	// do something with `num`
}
```
## for ... in
```typescript
for (let index in nums) {
	let num = nums[index];
	// do something with `num`
	//   while knowing its index in the array
}
```
## array.each()
If `lambda`'s are your thing...
```typescript
nums.forEach(
	num => {
		/* do something with `num` */
	}
)
```