#languages/PostgreSQL #concepts/array/list

While I don't know whether this is kosher or scuffed, in some cases a programmer will want to be able to add some static data to a database.

- Adding a ~~dummy~~ placeholder row to simplify a query.

## ERROR:  each UNION query must have the same number of columns

You're probably here because you wanted to create some static data for a query.

The TL;DR is that you're guessing for the syntax and it might *look* right but it isn't.

Below are code samples showing how create that static data.
## Vertical List

```postgresql
SELECT UNNEST(ARRAY['red', 'green', 'blue']) AS colors
-- | colors |
-- | ------ |
-- | red    |
-- | green  |
-- | blue   |
```

## Horizontal List

Good if you are going to `UNION` this data to the end of a query.
```postgresql
SELECT * FROM (VALUES ('red', 'green', 'blue'));
-- | column1 | column2 | column3 |  
-- | ------- | ------- | ------- |  
-- | red     | green   | blue    |
```

**NOTE:** It looks like for `asdf` you could use any other string. TODO: figure out why you have to put a string here. Is this the naming of a temporary table?

```postgresql

SELECT * FROM (
    VALUES ('red', 'green', 'blue')
) AS asdf("primary", "secondary", highlight);
-- | primary | secondary | highlight |  
-- | ------- | --------- | --------- |  
-- | red     | green     | blue      |
```


## Read More
- [SELECT Hard-coded Values without a Table - Stack Overflow](https://stackoverflow.com/q/15948614)