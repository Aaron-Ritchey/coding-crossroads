#languages/PostgreSQL 

I've seen some posts say "you don't need `ELSE 0` in a `CASE` statement" but I've been bitten by this twice now so it's worth remembering "NULL != 0" [[PostgreSQL NULL]]

```postgresql
-- when there are no approved funds, return NULL --
SUM(CASE WHEN (state = 'approved') THEN amount END)
> null

-- when there are no approved funds, return 0 --
SUM(CASE WHEN (state = 'approved') THEN amount ELSE 0 END)
> 0
```