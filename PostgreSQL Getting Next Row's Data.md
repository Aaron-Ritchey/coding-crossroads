#languages/PostgreSQL 

Get the current date, previous date, and next date -- all in one query.

```postgresql
SELECT player_id, event_date
	, LEAD(event_date) OVER (
		PARTITION BY player_id
		ORDER BY event_date
	) next_event_date
	, LAG(event_date) OVER (
		PARTITION BY player_id
		ORDER BY event_date
	) last_event_date
FROM Activity
```