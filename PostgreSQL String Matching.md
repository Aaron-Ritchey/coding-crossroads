#languages/PostgreSQL #concepts/string/match

Use can do basic regex stuff

```postgre
-- contains "ABC" anywhere in the string
username LIKE "%ABC%"
username ~ 'ABC'

-- start with "ABC"
username LIKE "ABC%"
username ~ '^ABC'

-- a word starts with "ABC"
username LIKE 'ABC%' OR username LIKE '\sABC'
username ~ '\mABC'
```