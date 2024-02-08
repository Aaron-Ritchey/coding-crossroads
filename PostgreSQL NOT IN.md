#languages/PostgreSQL 

```postgresql
SELECT customer_id
FROM Visitors
WHERE visitor_id NOT IN (
	SELECT DISTINCT visitor_id FROM Purchases
)
```