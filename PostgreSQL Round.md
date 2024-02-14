#languages/PostgreSQL #math/round

```postgresql
-- TODO: need to verify this code works --
SELECT racer_id,
	-- Rounds to 3 digits ---
	AVG(timestamp)::numeric(10,3) as runtime
FROM Racers
	WHERE racing_strip = true
ORDER BY runtime
```

The `ROUND()` function works for basic numbers, but throws some kind of error when using aggregation functions like `AVG`

Also, when dividing two `integer` numbers, you have to cast one of the numbers to `numeric` to avoid [[Integer Division]].

```postgresql
-- contrieved example --
SELECT
	Accounts.user_id,
	Countings.numerator,
	Countings.denominator,
	ROUND(Countings.numerator::numeric / Countings.denominator, 2) AS ratio
```