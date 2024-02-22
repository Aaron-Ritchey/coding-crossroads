A contrived example of finding all users who completed some kind of "quest" within seven days.

```postgresql
-- TODO: verify this works
SELECT user_id, user_name
FROM some_table
WHERE quest_start+7 <= quest_finish
```