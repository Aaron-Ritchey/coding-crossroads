#languages/Swift #concepts/conditional/ternary

The following code is okay.

```
(acc==ele) ? 1 : 0
```

The following code results in an error

```
(acc==ele)?1:0
// swift expected ',' separator
```

This is because `(acc==ele)` is a `boolean`, but `(acc==ele)?` becomes an `optional boolean`. ...something to do with "unwrapping" variables.

https://stackoverflow.com/a/24122706