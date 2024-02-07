#languages/PHP #concepts/array/join

PHP doesn't `join`, in `implode`s.

```php

## Optional parameter as first value?
## Sure thing, captain.
echo implode(["a","b","c"]);
> "abc";

## PHP will figure out which parameter should join the other. Most languages would complain.
echo implode("-", ["a","b","c"]);
> "a-b-c";

## Life's too short to be consitent.
## (Actually, no, plaese be consistent.)
echo implode(["a","b","c"], "-");
> "a-b-c";
```