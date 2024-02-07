#languages/PHP #concepts/print 

PHP has the unquie `echo` ~~function~~ language construct. (*Not* a function.)

```PHP
echo "hello";
> "hello"

echo("hello");
> "hello"

print "hello";
> "hello"

print ("hello");
> "hello"
```

## Short Codes
Using `<?= ?>` could work, but from what I recall it went out of fashion around ...2005?

```php
// Not recommended
<?php
	$location = "at home";
?>
Don't try this <?=$location?>

```

## Printing Arrays

```php
## This is incorrect.
echo([1,2,3]);
> "Array"

## This is what to do.
print_r([1,2,3]);
> [1,2,3]
```