#languages/PostgreSQL #errors/runtime #unique 

Table names and column names are *technically* case sensitive in PostgreSQL, but PostgreSQL hides it by automatically converting names to lowercase.

When you write...
`SELECT id, columnName, Another_Column_Name FROM MyTable`

The database sees it as...
`SELECT id, columnname, another_column_name FROM mytable`
## Troubleshooting "Relation does not exist"

- Are you using quotes for table or column names?
	- If so, make sure the name within the quotes has the correct case as the table or column.
	- Also, consider removing the quotes. If you quoted the table because it was using what looked like a reserved word, you probably don't need to do that.
## Read More
- ["All unquoted identifiers are assumed ... to be lower case"](https://sql-info.de/postgresql/postgres-gotchas.html#1_2)
