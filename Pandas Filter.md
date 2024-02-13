#languages/Pandas 

```python
result = employees.query('primary_flag == "Y"')

## alternately
result = employees.loc[employees.primary_flag == 'Y']
```

## Don't use .where()

`DataFrame.where()` isn't SQL `WHERE` clause. Just avoid it. :-)

## Error: cannot assign without a target object

```python
## Note the single equal statement.
result = employees.query('primary_flag = "Y"')
```
