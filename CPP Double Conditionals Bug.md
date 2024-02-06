#languages/CPP 

This will result in a nasty hidden bug.

```c++

// WRONG
if ('A' <= letter <= 'Z') {
	...
}

// CORRECT
if ('A' <= letter && letter <= 'Z') {
	...
}
```