#languages/PostgreSQL #concepts/math/minmax 

When someone says "how do I get the maximum XYZ", that could mean a lot of things. Here are three examples.
## Max Value in Column
> "**What** is the score of the post with the most likes?
> "I don't care who made it or what the post is, I just want the score."
```postgresql
SELECT MAX(likes)
FROM Posts
> 110
```
## Row with Max Value in Column
> "What is the most liked post **in general**?
> "I need to know who it is and what it is."
```postgresql
SELECT post_id, author_id, score FROM Players
FROM Posts
ORDER BY score DESC
LIMIT 1
> [post_id=11, author_id=15, score=110]
```
## Max Value in Grouping
> "What is the most liked post **for each author**?
> "I want to get everyone's best post."
```postgresql
SELECT DISTINCT ON (author_id)
	post_id, author_id, score
FROM Posts
ORDER BY author_id, score DESC
```
### Tips for "Max Value in Grouping"

The criteria used in the `DISTINCT ON` must *also* be the first ORDER BY, or you'll get an error.
```postgresql
-- max value for each author
SELECT DISTINCT ON (AUTHOR_ID)
	post_id, author_id, score
FROM Posts
ORDER BY AUTHOR_ID, score DESC

-- max value for each author/category pairing
-- a.k.a.
-- max value in each category for each author
--
SELECT DISTINCT ON (AUTHOR_ID, CATEGORY_ID)
	post_id, author_id, score
FROM Posts
ORDER BY AUTHOR_ID, CATEGORY_ID, score DESC
```

The secondary `ORDER BY` criteria needs to be `DESC` if you want the **maximum** value.

```postgresql
-- max value for each author
SELECT DISTINCT ON (author_id)
	post_id, author_id, score
FROM Posts
ORDER BY author_id, score DESC

-- min value for each author
-- (could be deliberate, or could be a mistake)
SELECT DISTINCT ON (author_id)
	post_id, author_id, score
FROM Posts
ORDER BY author_id, score -- no DESC
```