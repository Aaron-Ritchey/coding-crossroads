#languages/PostgreSQL #concepts/rdms/unpivot

The `unpivot` must be done column by column and combined using [[PostgreSQL UNION|UNION]]. (Not [[PostgreSQL JOIN|JOIN]]!)

```postgresql
'''
Input: (`Products` table)
+------------+--------+--------+--------+
| product_id | store1 | store2 | store3 |
+------------+--------+--------+--------+
| 0          | 95     | 100    | 105    |
| 1          | 70     | null   | 80     |
+------------+--------+--------+--------+
'''

'''
Output:
+------------+--------+-------+
| product_id | store  | price |
+------------+--------+-------+
| 0          | store1 | 95    |
| 0          | store2 | 100   |
| 0          | store3 | 105   |
| 1          | store1 | 70    |
| 1          | store3 | 80    |
+------------+--------+-------+
* strip away NULL values
'''

SELECT * FROM (

	-- Column #1 --
	SELECT product_id
		, 'store1' AS store
		, store1 AS price
	FROM Products
	
	UNION
	
	-- Column #2 --
	SELECT product_id
		, 'store2' AS store
		, store2 AS price
	FROM Products
	
	UNION
	
	-- Column #3 --
	SELECT product_id
		, 'store3' AS store
		, store3 AS price
	FROM Products
	
) WHERE price IS NOT NULL
```