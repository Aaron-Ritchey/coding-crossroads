#languages/CPP #concepts/array

**TLDR:** you're probably looking for [[CPP Vectors|C++ Vectors]].

C++ arrays are "[[Array Resizing|fixed width]]".

Arrays also cannot be initialized to a specific size based on a dynamic value.
## Initialization

```c++
// PSEUDO-CODE
function foo(int bar) {
	int[bar] baz = { 0 };
	// (error message)
}
```

## Default-initialized vs Zero-initialized

This could bite you if you're coming from other languages.

```c++
function foo(int bar) {

    // Allocate space for an array.
    // I don't care what's in it.
    int[10] array_default_init;

    cout << array_default_init[3];
    > 0? 1? -- indeterminate

    // Allocate space for an array,
    //   and fill it with zeroes.
    int[10] array_zero_init = { 0 };

    cout << array_zero_init[3];
    > 0 -- determinate

}
```
