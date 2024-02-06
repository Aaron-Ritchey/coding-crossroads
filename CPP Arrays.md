#languages/CPP #concepts/array 

**TLDR:** you're probably looking for [[CPP Vectors|C++ Vectors]].

C++ arrays are "fixed length".

Arrays also cannot be initialized to a specific size based on a dynamic value.
## Initialization

```c++
// PSEUDO-CODE
function foo(int bar) {
	int[bar] baz;
	// (error message)
}
```

