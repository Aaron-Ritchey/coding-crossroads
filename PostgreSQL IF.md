#languages/PostgreSQL #concepts/conditional 

```postgresql
SELECT player_id, level, xp_current, xp_to_level

	-- using IF() --
	, IF (xp_current >= xp_to_level) AS ready_to_level
	-- using CASE WHEN THEN ELSE
	, CASE
		WHEN (xp_current >= xp_to_level)
		THEN true
		ELSE false
	END
```

## Read More
- [[PostgreSQL CASE-WHEN-ELSE]]