#languages/PostgreSQL 

```postgresql
SELECT visitor_id, COUNT(visitor_id)
FROM Transactions
GROUP BY visitor_id
```