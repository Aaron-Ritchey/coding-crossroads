#languages/PostgreSQL #concepts/string/length

Nothing too exciting.

```
SELECT words
FROM dictionary
WHERE length(word) = 4
```