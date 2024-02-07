#languages/Pandas 

(Rough note, needs to be reviewed again.)

In Pandas, if you're working on a table with missing data, you'll need to spend extra effort to avoid losing those excluded rows.

Example:
```pseudocode
## SELECT all rows WHERE (email != "fred@example.com");
## > will also exclude rows where email == N/A
```

## DataFrame.dropna()

Most likely, you're using this to only drop rows where a specific column has missing data.

```python
## NOTE: it's not "columns=['name']"
students.dropna(subset=['name'])

## Alternatively:
students[~students["name"].isna()]
```

If you don't pass parameters, it'll remove any row with any `N/A` value, which isn't what you'll usually want

```python
## Takes away more rows than expected.
students.dropna()
```
