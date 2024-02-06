#languages/Java #concepts/array #concepts/array/initialize

Java arrays are "fixed length".

## Initialization

```java

// Array will ONLY ever have eight elements
//   duringt this code run.
int[] array = new int[8];

function void x(int size) {
	// Dynamic size allocation is okay.
	// (In some languages, like C++, it's not allowed.)
	int[] array = new int[size];
}

```
