```postgresql
SELECT id AS Id

FROM (
	SELECT
	id,
	recordDate AS date_today,
	lag(recordDate) OVER (ORDER BY recordDate) AS date_yesterday,
	temperature AS temp_today,
	lag(temperature) OVER (ORDER BY recordDate) AS temp_yesterday
	FROM Weather
	ORDER BY recordDate
)

WHERE temp_today > temp_yesterday

AND date_today = date_yesterday+1
```

Related:
- [[PostgreSQL Date Comparison]]
## Read More

- [Window Functions | PostgreSQL Tutorial.com]