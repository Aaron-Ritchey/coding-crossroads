When programmers are trained to use `==` (or `===` for JavaScript/TypeScript programmers) for equality checks, database administrators only need to use `=`.

```postgresql
-- this is correct --
SELECT * FROM some_table WHERE id_column = 5

-- this is wrong --
SELECT * FROM some_table WHERE id_column == 5
> operator does not exist: integer == integer
> LINE 1: WHERE id_column == 5
>                         ^
```