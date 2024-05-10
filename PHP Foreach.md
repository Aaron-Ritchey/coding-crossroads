#languages/PHP #concepts/foreach 

```php
// Used the current epoch time as a random set of numbers.
$numbers = [1,715,304,966];
$result = 0;

// Count multiples of three.
foreach ($numbers as $num) {
	if ($num % 3 == 0) {
		$result += 3
	}
}

echo $result;
> 1
```