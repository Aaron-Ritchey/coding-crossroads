#languages/CPP #concepts/array #concepts/array/stack

A `Vector` is a re-sizable `array` which behaves like a **stack**.

(But look into [[CPP Vectors|C++ Vectors]] to understand the differences.)

```c++

// Empty vector.
vector<int> x = {};

// Push to end of vector.
x.push_back(1);

// Peek.
x.back();

// Pop. ***(does not `return` popped elements)***.
x.pop_back();

// Pop (saving the popped element).
// TODO: check if `y` is de-referenced.
int y = x.back();
x.pop_back()
```

## Read More
- [[Stacks in Different Languages]]