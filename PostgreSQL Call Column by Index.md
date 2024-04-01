#languages/PostgreSQL 

```postgre
SELECT location_id, COUNT(player_id)
FROM PlayerData
GROUP BY 1 --in this case, 1 is `location_id`.
```
