In PostgreSQL, use `rank()`

```postgresql
SELECT player_id
	, score
	, rank() OVER (ORDER BY score)
FROM
	PlayerData
```

The inner `ORDER BY` will also sort the data by rank