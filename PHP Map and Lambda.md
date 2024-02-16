#languages/PHP #concepts/map-function #concepts/lambda

In the `array_map` documentation, you pass a `Callable`.

```php
// Flip 1s and 0s in an array.
// As of 7.4.0
return array_map(fn($cell) => 1-$cell, $row);
```

In older code (before PHP 7.4 came out in 2019), you would have to write an entire function.

```php
// Before 7.4
$oldeInvertLambda = function($cell) {
	return 1 - $cell;
}
return array_map($oldeInvertLambda, $row);

// As of PHP 7.4
$newInvertLambda = fn($cell) => 1-$cell;
return array_map($newInvertLambda, $row);

```
