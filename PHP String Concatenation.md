#languages/PHP #concepts/string/concat

PHP has a unique way of concatenating strings:

```
echo ("taco" . "cat");
> "tacocat"
```

If you try to add strings, you'll *usually* get an error

```
echo ("taco" + "cat");
> PHP Fatal error: Uncaught TypeError: Unsupported operand types: string + string
```

But sometimes, PHP will type-juggle it for you to hilarious effect.

```
echo ("2 tacos" + "1 cat");
> 3
```


