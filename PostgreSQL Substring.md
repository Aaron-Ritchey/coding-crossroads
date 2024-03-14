#languages/PostgreSQL #concepts/string/substring
## Quick Answer

`SUBSTRING` uses 1-offset!!!

```postgresql

--- | state_id | name       |
--- | -------- | ---------- |
--- | 1        | WASHINGTON |
--- | 2        | WISCONSIN  |
--- | 3        | WYOMING    |

---               1-OFFSET!!! ---\
---                              |
---                              V
SELECT state_id, SUBSTRING(name, 1, 2) AS abbrev FROM States
```

## More Samples
```postgresql
--                                             -- 1234567 --
SELECT 'ABCDEFG' AS original                   -- ABCDEFG --
  
	--- rightmost 3 characters ---
	, SUBSTRING('ABCDEFG', 4) AS wrong_1      -- DEFG     --
	, SUBSTRING('ABCDEFG', 5) AS okay_1       -- EFG      --
	, SUBSTRING('ABCDEFG' FROM 5) AS better_1 -- EFG      --
	  
	--- leftmost 3 characters ---
	, SUBSTRING('ABCDEFG', 0, 3) AS wrong_2   -- AB       --
	, SUBSTRING('ABCDEFG', 1, 3) AS okay_2    -- ABC      --
	, SUBSTRING('ABCDEFG' FOR 3) AS better_2  -- ABC      --

```

## SUBSTRING vs SUBSTR

PostgreSQL has both `SUBSTR` and `SUBSTRING`. From a quick read, `SUBSTR` is but `SUBSTRING` is preferred because it's part of the SQL standard.

(TODO: look into who included `SUBSTR` or why it was included).