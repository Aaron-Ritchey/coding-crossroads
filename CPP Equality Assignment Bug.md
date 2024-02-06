#languages/CPP 

Some languages will catch errors where you accidentally do an equality check instead of an assignment.

```
// PSEUDOCODE
x = 5
if (true) {
	x == 15
}
> "error message goes here"
```

C++ is not one of those languages.

```c++
int x = 5;
if (true) {
	x == 15;
	// This equality check will do nothing.

	x = 15;
	// This assignment is what we wanted.
}
```