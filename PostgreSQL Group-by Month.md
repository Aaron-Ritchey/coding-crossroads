#languages/PostgreSQL #concepts/datetime #concepts/datetime/format

Requires using `TO_CHAR` to convert dates into a specific format, and using `DATE_TRUNC` to... well, truncate the date.

```postgresql
-- Quick Example --
SELECT
	TO_CHAR(
		DATE_TRUNC('month', trans_date),
		'YYYY-MM'
	) AS month_range,
	COUNT(trans_date)
FROM
	Transactions
GROUP BY
	v
```

## Read More

- [How to Group by Month - LearnSQL.com](https://learnsql.com/cookbook/how-to-group-by-month-in-postgresql/)