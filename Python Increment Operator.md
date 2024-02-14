#languages/Python #concepts/math/increment

Python does not have an increment/decrement operator like most languages.

```python
x = x + 1  ## this is okay, I guess
x += 1     ## this is better

x++        ## nope
++x        ## still nope
```

(TODO: find the source) This was a design decision by the creators of Python due to hidden bugs which can occur from a typo.