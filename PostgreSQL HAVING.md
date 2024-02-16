#languages/PostgreSQL 

A handy way of conditionally filtering a grouping

```postgresql
SELECT managerId, count(managerId) AS direct_reports
FROM Employee
GROUP BY managerId
HAVING count(managerId) >= 5
```

## Read More

- [PostgreSQL HAVING | PostgreSQL Tutorials](https://www.postgresqltutorial.com/postgresql-tutorial/postgresql-having/)
