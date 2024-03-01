#languages/PostgreSQL #concepts/conditional/ternary 

Some online sources inaccurately claim...

> "...you don't need `ELSE 0` in a `CASE` statement!"

In some cases, that's fine. In other cases, it'll cause problems.

Because of the [[PostgreSQL Truthiness of NULL]] there is a substantial difference between using `ELSE 0` and omitting it. There could be some downstream code which discards `NULL` data.

```postgresql
-- when there are no approved funds, return NULL --
SUM(CASE WHEN (state = 'approved') THEN amount END)
> null

-- when there are no approved funds, return 0 --
SUM(CASE WHEN (state = 'approved') THEN amount ELSE 0 END)
> 0
```