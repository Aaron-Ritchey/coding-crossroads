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

## window "table_name" does not exist

(The following is unofficial.)
When using `AGG-OVER-WINDOW`, if you *don't* want to group, you don't have to `PARTITION`

```postgresql
--- THIS GETS THE DIFF OF TIMES BETWEEN EACH PLAYER'S ACTION ---
--- DOES A "GROUP BY" on player_id --
SELECT player_id, event_date
	, LEAD(event_date) OVER (
		PARTITION BY player_id
		ORDER BY event_date
	) next_event_date
FROM Activity

--- THIS GETS THE DIFF OF TIMES BETWEEN _ANY_ EVENTS --
--- DOES AN "ORDER BY" FOR YOU --
SELECT event_id
	, LEAD(event_date) OVER (
		ORDER BY event_date
	) next_event_date
FROM Activity
```